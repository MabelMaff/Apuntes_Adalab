## Creando una aplicación de Spotify con Python en GitHub (Parte 3) - Markdown para GitHub

### Resumen

En esta parte, hemos creado dos archivos: `support.py` y `main.py`. En `support.py`, hemos definido funciones para:

* Obtener las credenciales de Spotify (`get_credentials`)
* Conectarse a la API de Spotify (`connect_to_spotify`)
* Preparar la URL de una lista de reproducción (`prepare_url`)
* Extraer canciones de una lista de reproducción (`extract_songs`)

En `main.py`, hemos llamado a estas funciones para:

* Obtener las credenciales de Spotify y conectarse a la API
* Extraer todas las canciones de una lista de reproducción
* Imprimir la información de las canciones

### Código

#### `support.py`

```python
import spotipy
from spotipy.oauth2 import SpotifyOAuth
import dotenv

def get_credentials():
    """
    Obtiene las credenciales de Spotify del archivo .env
    """
    client_id = os.getenv('CLIENT_ID')
    client_secret = os.getenv('CLIENT_SECRET')
    return client_id, client_secret

def connect_to_spotify(client_id, client_secret):
    """
    Se conecta a la API de Spotify utilizando las credenciales proporcionadas
    """
    scope = "user-library-read"
    sp = spotipy.Spotify(auth_manager=SpotifyOAuth(scope=scope, client_id=client_id, client_secret=client_secret))
    return sp

def prepare_url(playlist_url):
    """
    Extrae el ID de una URL de lista de reproducción de Spotify
    """
    playlist_id = playlist_url.split('/')[-1].split('?')[0]
    return playlist_id

def extract_songs(sp, playlist_uri):
    """
    Extrae todas las canciones de una lista de reproducción de Spotify
    """
    all_songs = []
    offset = 0

    while True:
        playlist_tracks = sp.playlist_tracks(playlist_uri, offset=offset, limit=100)
        items = playlist_tracks['items']

        if not items:
            break

        all_songs.extend(items)
        offset += len(items)

    return all_songs
```

#### `main.py`

```python
from src import get_credentials, connect_to_spotify, extract_songs

def main():
    # Obtener credenciales de Spotify y conectarse a la API
    client_id, client_secret = get_credentials()
    sp = connect_to_spotify(client_id, client_secret)

    # Extraer todas las canciones de una lista de reproducción
    playlist_uri = "spotify:playlist:37i9dQZF1DXcBWIGoYBM5m"  # Cambie por su ID de lista de reproducción
    songs = extract_songs(sp, playlist_uri)

    # Imprimir la información de las canciones
    for song in songs:
        print(song['track']['artists'][0]['name'], '-', song['track']['name'])

if __name__ == '__main__':
    main()
```

### Próximos pasos

En la próxima parte, vamos a:

* Filtrar las canciones extraídas para obtener solo las que nos interesen.
* Almacenar las canciones en un archivo o base de datos.
* Crear una interfaz de usuario para interactuar con la aplicación.

### Notas

* Asegúrese de reemplazar `spotify:playlist:37i9dQZF1DXcBWIGoYBM5m` con el ID de su propia lista de reproducción.
* Es importante reiniciar el kernel después de realizar cambios en `support.py` para que los cambios se reflejen.

### Recuerda

* Este código es solo un ejemplo y puede modificarse para adaptarse a sus necesidades específicas.
* Consulte la documentación de la API de Spotify para obtener más información sobre cómo usar las diferentes funciones.
* ¡No dude en hacer preguntas o dejar comentarios si tiene algún problema!