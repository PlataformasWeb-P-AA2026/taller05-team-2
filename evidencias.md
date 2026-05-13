# Taller 05 - Integración de Datos con CouchDB

## 1. Clonar el repositorio

```bash
git clone https://github.com/PlataformasWeb-P-AA2026/taller05-team-2.git
cd taller05-team-2
```

## 2. Generar el archivo JSON

Entrar a la carpeta donde están los scripts:

```bash
cd formato-json
```

Instalar dependencias de Python:

```bash
pip install beautifulsoup4 pypdf requests
```

Ejecutar el script que genera el JSON:

```bash
python generar_json.py
```

Esto crea el archivo:

```text
mundial_2026.json
```

## 3. Cargar datos en CouchDB

Tener CouchDB ejecutándose y editar el archivo credenciales.py con sus credencias 

Luego crear la base de datos "jugadores":


Ejecutar el archivo que sube el json a la base de datos

```bash
python cargar_couchdb.py
```

y carga los documentos del archivo `mundial_2026.json`.

## 3.1 Quitar Permiso a la base de datos en CouchDB

## 4. Ejecutar frontend

Regresar a la raíz del proyecto:

```bash
cd ..
```

Entrar a la carpeta del frontend:

```bash
cd frontend
```

Instalar dependencias:

```bash
npm install
```

Ejecutar el proyecto:

```bash
npm run dev
```



## 5. Evidencias

### Base de datos en CouchDB

<img width="1848" height="1046" alt="image" src="https://github.com/user-attachments/assets/9d319ad5-0a61-4338-87b3-e963cfbc0318" />


### Frontend funcionando

<img width="1919" height="1136" alt="image" src="https://github.com/user-attachments/assets/4dcdb0d9-e42c-4df2-a8af-aa995e424ca0" />


