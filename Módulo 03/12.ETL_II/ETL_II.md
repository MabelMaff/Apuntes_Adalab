# 🎼 Creación de Esquemas y BBDD para Datos de Spotify

## 🌟 Introducción
Para avanzar en este módulo, es necesario tener el proyecto de la clase anterior, donde extrajimos información de la API de Spotify. Ahora vamos a aprender a almacenar esos datos de manera estructurada en MySQL.

## 📚 Lección 12.1: Creación de Esquemas y BBDD

### 📹 Video 1: Introducción a Esquemas en MySQL
Aprende a crear una base de datos en MySQL utilizando MySQL Workbench:
- [Ver Video 1](https://www.youtube.com/embed/-5y_Vj-gSuU "1- ETL II: Creación esquemas y BBDD")

#### 🔍 Detalles del Video:
- Se crea una base de datos en MySQL usando MySQL Workbench.
- Se incluyen tres tablas: `canciones`, `artistas` y `características`.
- Se muestra cómo crear un modelo entidad-relación.

### 🖥️ Creación de Bases de Datos y Tablas Desde Python
Aprende a implementar bases de datos y tablas desde Python:
- [Ver Video 2](https://www.youtube.com/embed/4xkuUNUq8M4 "3 - ETL II: Consultas SQL en Python")

#### 📄 Explicación del Video:
- **Archivo Clave:** `bbdd_spotify_soporte.py`
- **Función Importante:** `creacion_bbdd_tablas`

```python
# bbdd_spotify_soporte.py
import mysql.connector

def creacion_bbdd_tablas():
    try:
        cnx = mysql.connector.connect(
            user='tu_usuario', 
            password='tu_contraseña', 
            host='127.0.0.1'
        )
        cursor = cnx.cursor()
        cursor.execute("CREATE DATABASE IF NOT EXISTS SpotifyDB")
        cursor.execute("USE SpotifyDB")
        cursor.execute("CREATE TABLE IF NOT EXISTS canciones (id INT AUTO_INCREMENT PRIMARY KEY, nombre VARCHAR(255), artista VARCHAR(255))")
        cnx.commit()
    except mysql.connector.Error as err:
        print("Ha ocurrido un error:", err)
    finally:
        if cnx.is_connected():
            cursor.close()
            cnx.close()

```

### 📑 Creación de Consultas SQL
Prepara consultas SQL para la creación de tablas específicas:
- [Ver Video 3](https://www.youtube.com/embed/LewUMKsVgFE "2 - ETL II: Función de creación de BBDD y tablas")

```python
# queries_creacion_bbd_tablas.py
query_canciones = """
CREATE TABLE IF NOT EXISTS canciones (
    id INT AUTO_INCREMENT PRIMARY KEY,
    titulo VARCHAR(255) NOT NULL,
    duracion INT,
    fecha_lanzamiento DATE
);
"""
query_artistas = """
CREATE TABLE IF NOT EXISTS artistas (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(255) NOT NULL
);
"""
```

### 🧩 Jupyter Notebooks y Archivos de Soporte
Accede a los archivos relevantes para usar las funciones y ejecutar consultas:
- **Main Notebook:** [Descargar modulo-3-leccion-12-ETL-main.py](https://1907341338-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2xM6eba0rsw3ijtXv8rf%2Fuploads%2Fgit-blob-09178d359fabad7f7698c44365d0357a0b94f1ef%2Fmodulo-3-leccion-12-ETL-main.py?alt=media)
- **Soporte BBDD:** [Descargar bbdd_spotify_soporte.py](https://1907341338-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2xM6eba0rsw3ijtXv8rf%2Fuploads%2Fgit-blob-a7e6ae289ff39240ff10c13728cb228085383221%2Fbbdd_spotify_soporte.py?alt=media)
- **Consultas SQL:** [Descargar queries_creacion_bbd_tablas.py](https://1907341338-files

