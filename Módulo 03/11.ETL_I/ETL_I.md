# 🌟 ETL I: Extracción, Transformación y Carga

![ETL Process](https://github.com/MabelMaff/Apuntes_Adalab/blob/main/M%C3%B3dulo%2003/11.ETL_I/Imagenes/ETL_I.webp)

## 🧐 ¿Qué es ETL?
ETL significa "Extracción, Transformación y Carga" (Extraction, Transformation, and Loading). Este proceso es esencial en el análisis y la gestión de datos, facilitando la consolidación, limpieza, transformación y carga de datos en sistemas de análisis.

### 🔍 Extracción
Recogemos datos de fuentes diversas como bases de datos, archivos, sistemas en línea y APIs. Estos datos se preparan en su formato original para el siguiente paso.

### 🔧 Transformación
Aquí los datos se limpian, organizan y transforman. Incluye convertir datos de un formato a otro y aplicar reglas de negocio para hacer los datos útiles y coherentes.

### 📦 Carga
Finalmente, los datos transformados se almacenan en una base de datos de análisis, donde se crean y actualizan tablas.

## ✨ Importancia del ETL
- **Consolidación de datos:** Unifica datos de múltiples fuentes en un solo lugar.
- **Limpieza y preparación:** Automatiza la limpieza y preparación de datos crudos.
- **Transformación y enriquecimiento:** Adapta y enriquece los datos para análisis.
- **Mantenimiento de la calidad:** Implementa reglas de validación y corrección.
- **Automatización y eficiencia:** Reduce tiempo y errores en la gestión de datos.
- **Escalabilidad:** Adapta el proceso a grandes volúmenes de datos según las necesidades organizativas.

## 📈 Por qué el ETL es importante
- **Toma de decisiones informadas:** Facilita el acceso a datos listos para análisis.
- **Eficiencia en el proceso:** Ahorra recursos y mejora la productividad.
- **Consistencia y calidad:** Garantiza datos consistentes y de alta calidad.
- **Historial de datos:** Permite el análisis de tendencias a lo largo del tiempo.
- **Integración de sistemas:** Facilita la unión de datos de diversas fuentes.

# 🎵 Caso Práctico: ETL Spotify

## 🚀 Crear proyecto de Spotify
Usaremos el API de Spotify para demostrar el proceso de ETL.

### 📘 Documentación necesaria:
- **Spotipy:** [Documentación de Spotipy](https://spotipy.readthedocs.io/en/2.22.1/)
- **Token de Spotify:** [Cómo crear un token](https://developer.spotify.com/)

### 🎥 Videos explicativos:
- **Video 1:** [Introducción al API de Spotify](https://www.youtube.com/watch?v=rf8y-Heq8Wo)
- **Video 2:** [Configuración del proyecto](https://www.youtube.com/watch?v=BOerjavSMh4)

### 🔧 Configuración del proyecto:
1. **Crea una carpeta `src`** y dentro:
   - `main.py`: Importa `spotipy` y la función para obtener token.
   - `api_spotify_soporte.py`: Contiene la función para obtener el token.
   - `.env`: Almacena las credenciales.
   - `.gitignore`: Asegura que `.env` no se suba a GitHub.

#### Código para configuración del entorno y ejecución:
```python
# main.py
import spotipy
from spotipy.oauth2 import SpotifyClientCredentials

print("Hola mundo")

# .env
client_id=your_client_id
client_secret=your_client_secret

# Ejecución desde la terminal
python main.py
```

### 🔗 Conexión con el API de Spotify:
- **Video 3:** Mira cómo [Conectarse con el API de SPOTIFY](https://www.youtube.com/watch?v=7vftn1yxYRQ)
- **Código para obtener el token y conectar con Spotify:**
```python
# api_spotify_soporte.py
import os
import spotipy
from spotipy.oauth2 import SpotifyClientCredentials
from dotenv import load_dotenv

# Cargar variables de entorno
load_dotenv()
CLIENT_ID = os.getenv("client_id")
CLIENT_SECRET = os.getenv("client_secret")

# Verificar que las variables de entorno se han cargado correctamente
print("Contenido del archivo .env:")
with open('.env', 'r') as f:
    print(f.read())
print(f"CLIENT_ID: {CLIENT_ID}")
print(f"CLIENT_SECRET: {CLIENT_SECRET}")

```

### 📛 Si las variables de entorno no se cargaron correctamente, cargar manualmente
```
if CLIENT_ID is None or CLIENT_SECRET is None:
    from dotenv import dotenv_values
    config = dotenv_values(".env")
    CLIENT_ID = config.get("client_id")
    CLIENT_SECRET = config.get("client_secret")
    print("Carga manual:")
    print(f"CLIENT_ID: {CLIENT_ID}")
    print(f"CLIENT_SECRET: {CLIENT_SECRET}")

def credenciales():
    # Configurar las credenciales con los valores cargados
    credenciales = SpotifyClientCredentials(CLIENT_ID, CLIENT_SECRET)
    sp = spotipy.Spotify(client_credentials_manager=credenciales)
    return sp

# Uso de la función para establecer conexión
sp = credenciales()
```
### 📛 Ajuste del Path de Python

Si Python no se ejecuta correctamente desde tu entorno deseado, puedes ajustar el path para asegurarte de que el sistema utiliza la versión correcta de Python:

```markdown
Si tienes problemas para ejecutar Python o si los scripts no reconocen tu instalación de Python, asegúrate de ajustar el path del sistema para incluir el directorio donde Python está instalado. Esto es especialmente útil si tienes múltiples versiones de Python instaladas o si tu sistema operativo no está configurado para usar la versión deseada por defecto:

```bash
export PATH="/ruta/a/tu/python:$PATH"
```

Reemplaza `/ruta/a/tu/python` con la ruta actual a la instalación de Python que deseas utilizar. Este paso es crucial para asegurar que los comandos y scripts de Python se ejecuten con la configuración correcta.

## 🎶 ETL sobre Spotify:
### **Extraer canciones:**
- **Video 4:** [Conectar ficheros del proyecto](https://www.youtube.com/watch?v=Kya3Hfey924)
- **Código para extraer canciones de una playlist:**
```python
def extraer_canciones(conexion, playlist_URI):
    numero_canciones = conexion.playlist_tracks(playlist_URI, limit=1)["total"]
    offset = 0
    all_data = []
    for _ in range((numero_canciones // 100) + 1):
        batch_data = conexion.playlist_tracks(playlist_URI, offset=offset)["items"]
        all_data.extend(batch_data)
        offset += 100
    return all_data
```

### **Limpiar datos de canciones:**
- **Video 5:** [Extraer canciones de una lista de reproducción](https://www.youtube.com/watch?v=KjFtm3Jrr_A&t=3s)
- **Video 6:** [Extraer información específica de una canción](https://www.youtube.com/watch?v=DKBi5AuzhYk&t=135s)
- **Código para limpiar y organizar datos de canciones:**
```python
def limpiar_datos(all_data):
    basic_info = {"song": [], "artist": [], "date": [], "explicit": [], "uri_cancion": [], "popularity": [], "usuario": [], "links": [], 'uri_artista': [], "duracion": []}
    for cancion in all_data:
        basic_info["song"].append(cancion["track"]["name"])
        basic_info["date"].append(cancion["added_at"])
        basic_info["explicit"].append(cancion["track"]["explicit"])
        basic_info["uri_cancion"].append(cancion["track"]["uri"])
        basic_info["popularity"].append(cancion["track"]["popularity"])
        basic_info["usuario"].append(cancion["added_by"]["id"])
        basic_info["links"].append(cancion["track"]["external_urls"]["spotify"])
        basic_info["duracion"].append(cancion["track"]["duration_ms"])
        lista_artistas = []
        lista_uris = []
        for artista in cancion["track"]["artists"]:
            lista_artistas.append(artista["name"])
            lista_uris.append(artista["id"])
        basic_info["artist"].append(lista_artistas)
        basic_info["uri_artista"].append(lista_uris)
    df_canciones = pd.DataFrame(basic_info)
    return df_canciones
```

### **Extraer 'features' de una canción:**
- **Video 7:** [Extracción de 'features' de canciones](https://www.youtube.com/watch?v=OoxQ4bH-Oyw)
- **Código para extraer características y fusionarlas con datos básicos:**
```python
def sacar_caracteristicas(dataframe_canciones, conexion):
    lista_uri_canciones = dataframe_canciones["uri_cancion"].unique().tolist()
    features = []
    for uri in lista_uri_canciones:
        features_data = conexion.audio_features(uri)
        features.extend(features_data)
    df_features = pd.DataFrame(features)
    final = dataframe_canciones.merge(df_features, left_on="uri_cancion", right_on="uri", how="inner")
    return final
```

### **Jupyter Notebooks**
- [modulo-3-leccion-11-ETL-main.py](https://github.com/MabelMaff/Apuntes_Adalab/blob/main/M%C3%B3dulo%2003/11.ETL_I/Jupyters/modulo-3-leccion-11-ETL-main.py)
- [api_spotify_soporte.py](https://github.com/MabelMaff/Apuntes_Adalab/blob/main/M%C3%B3dulo%2003/11.ETL_I/Jupyters/api_spotify_soporte.py)
