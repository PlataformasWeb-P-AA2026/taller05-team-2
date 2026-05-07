# Taller 05 - Integración de Datos con CouchDB

## 1. Clonar el repositorio

```bash
git clone <[URL_DEL_REPOSITORIO](https://github.com/PlataformasWeb-P-AA2026/taller05-team-2.git)>
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

Tener CouchDB ejecutándose en:

```text
http://localhost:5984 
```

Luego ejecutar:

```bash
python cargar_couchdb.py
```

Este script crea la base de datos:

```text
jugadores
```

y carga los documentos del archivo `mundial_2026.json`.

## 4. Crear vistas en CouchDB

Design Document:

```text
_design/losjugadores
```

Vista `por_club`:

```javascript
function(doc) {
  if (doc.club_actual) {
    emit(doc.club_actual, doc);
  }
}
```

Vista `por_goles`:

```javascript
function(doc) {
  if (doc.goles) {
    emit(doc.goles, doc);
  }
}
```

Vista `por_partidos`:

```javascript
function(doc) {
  if (doc.partidos) {
    emit(doc.partidos, doc);
  }
}
```

## 5. Ejecutar frontend

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

Abrir en el navegador:

```text
http://localhost:5173
```

## 6. Evidencias

### Base de datos en CouchDB

<img width="1848" height="1046" alt="image" src="https://github.com/user-attachments/assets/9d319ad5-0a61-4338-87b3-e963cfbc0318" />


### Frontend funcionando

<img width="1919" height="1136" alt="image" src="https://github.com/user-attachments/assets/4dcdb0d9-e42c-4df2-a8af-aa995e424ca0" />


