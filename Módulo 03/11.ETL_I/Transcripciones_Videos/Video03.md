## Creando una aplicación de Spotify con Python en GitHub (Parte 2) - Markdown para GitHub

### Introducción

En este tutorial, vamos a continuar creando una aplicación de Spotify básica utilizando Python y GitHub. Aprenderemos a:

* **Escribir funciones en un archivo de soporte**
* **Extraer el ID de una URL de lista de reproducción**
* **Conectarse a la API de Spotify**

### Paso 1: Escribir funciones en un archivo de soporte

1. **Crear un archivo de soporte:**
    * Crea un archivo llamado `support.py` en la carpeta `src`.
    * Este archivo contendrá las funciones que utilizaremos en nuestro código principal.

2. **Importar bibliotecas:**
    * Al principio del archivo `support.py`, importa las bibliotecas necesarias:

    ```python
    import spotipy
    from spotipy.oauth2 import SpotifyOAuth
    import dotenv
    ```

3. **Cargar variables de entorno:**
    * Utiliza la biblioteca `dotenv` para cargar las variables de entorno (`CLIENT_ID` y `CLIENT_SECRET`) del archivo `.env`:

    ```python
    dotenv.load_dotenv('../.env')
    ```

4. **Definir funciones:**
    * Crea funciones para cada tarea que necesites realizar. Por ejemplo:

    ```python
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
    ```

### Paso 2: Extraer el ID de una URL de lista de reproducción

1. **Definir la función `prepare_url`:**
    * La función `prepare_url` recibe una URL de lista de reproducción como parámetro.
    * Divide la URL por '/' y toma el último elemento.
    * Divide el último elemento por '?' y toma el primer elemento.
    * Devuelve el ID de la lista de reproducción extraído.

2. **Probar la función `prepare_url`:**
    * Puedes probar la función `prepare_url` llamando a la función con una URL de lista de reproducción y verificando el resultado.

### Paso 3: Conectarse a la API de Spotify

1. **Definir la función `connect_to_spotify`:**
    * La función `connect_to_spotify` recibe el ID de cliente y el secreto de cliente como parámetros.
    * Crea un objeto `SpotifyOAuth` con el alcance especificado.
    * Crea un objeto `Spotify` utilizando el objeto `SpotifyOAuth`.
    * Devuelve el objeto `Spotify`.

2. **Llamar a la función `connect_to_spotify`:**
    * Puedes llamar a la función `connect_to_spotify` con las credenciales de Spotify obtenidas del archivo `.env` para obtener un objeto `Spotify`.

### Paso 4: Continuar con el desarrollo

1. **Crear el archivo `main.py`:**
    * Crea un archivo llamado `main.py` en la carpeta `src`.
    * Este archivo contendrá el código principal de tu aplicación.

2. **Importar módulos necesarios:**
    * Al principio del archivo `main.py`, importa los módulos necesarios:

    ```python
    from support import get_credentials, connect_to_spotify, prepare_url
    ```

3. **Obtener credenciales y conectarse a Spotify:**
    * Obtén las credenciales de Spotify utilizando la función `get_credentials`.
    * Conéctate a la API de Spotify utilizando la función `connect_to_spotify` y las credenciales obtenidas.

4. **Implementar la lógica de la aplicación:**
    * Utiliza el objeto `Spotify` para realizar las acciones deseadas, como obtener información de listas de reproducción o reproducir canciones.

5. **Ejecutar el código:**
    * Ejecuta el archivo `main.py` para ejecutar tu aplicación.