## Creando una aplicación de Spotify con Python en GitHub

### Introducción

En este tutorial, vamos a crear una aplicación de Spotify básica utilizando Python y GitHub. Aprenderemos a:

* Configurar el proyecto en GitHub
* Instalar las dependencias necesarias
* Escribir código Python para interactuar con la API de Spotify
* Almacenar contraseñas de forma segura

### Estructura del proyecto

* **Carpeta src:**
    * `main.py`: Aquí escribiremos el código principal de la aplicación.
    * `.gitignore`: Este archivo indicará a Git que ignore las contraseñas sensibles.
* **Archivo .gitignore:** Este archivo indicará a Git que ignore las contraseñas sensibles.

### Paso 1: Crear el repositorio de GitHub

1. Crea un nuevo repositorio en GitHub y dale un nombre adecuado.
2. Clona el repositorio en tu ordenador local.

### Paso 2: Instalar dependencias

1. Abre una terminal y navega hasta la raíz del repositorio clonado.
2. Ejecuta el siguiente comando para instalar la biblioteca de Spotify:

```bash
pip install spotipy
```

### Paso 3: Almacenar contraseñas de forma segura

1. Crea un archivo llamado `.gitignore` en la raíz del repositorio.
2. Añade la siguiente línea al archivo `.gitignore`:

```
src/.env
```

3. Crea un archivo llamado `.env` en la carpeta `src`. Este archivo no se subirá a GitHub.
4. En el archivo `.env`, almacena tus credenciales de Spotify de la siguiente manera:

```
CLIENT_ID=<tu_client_id>
CLIENT_SECRET=<tu_client_secret>
```

### Paso 4: Escribir código Python

1. Abre el archivo `main.py` en un editor de código.
2. Importa las bibliotecas necesarias:

```python
import spotipy
from spotipy.oauth2 import SpotifyOAuth
```

3. Configura la autenticación de Spotify:

```python
scope = "user-library-read"

sp = spotipy.Spotify(auth_manager=SpotifyOAuth(scope=scope))
```

4. Obtiene la información de tu biblioteca de Spotify:

```python
current_user = sp.current_user()
print(f"Nombre de usuario: {current_user['display_name']}")

playlists = sp.current_user_playlists()
for playlist in playlists['items']:
    print(f"Playlist: {playlist['name']}")
```

5. Guarda el archivo `main.py`.

### Paso 5: Ejecutar el código

1. Puedes ejecutar el código Python de dos maneras:

    **a) Desde la terminal:**

    1. Abre una terminal y navega hasta la carpeta `src`.
    2. Ejecuta el siguiente comando:

    ```bash
    python main.py
    ```

    **b) Desde Jupyter Notebook:**

    1. Abre el archivo `main.py` en Jupyter Notebook.
    2. Ejecuta las celdas de código una a una.

### Paso 6: Subir el código a GitHub

1. Agrega los cambios al repositorio local:

```bash
git add .
```

2. Commite los cambios con un mensaje descriptivo:

```bash
git commit -m "Primer commit"
```

3. Sube los cambios al repositorio remoto:

```bash
git push origin main
```

### Conclusión

¡Felicidades! Has creado una aplicación de Spotify básica utilizando Python y GitHub. Puedes seguir aprendiendo a desarrollar aplicaciones más complejas con la API de Spotify.
