# Central de Llamadas — Publicar como app instalable (PWA)

Esta carpeta contiene todo lo necesario. No necesitas Firebase ni base de
datos: los contactos se guardan en el propio navegador de tu celular
(`localStorage`), tal como ya funcionaba. GitHub Pages solo sirve para darle
una dirección `https://` a estos archivos — eso es lo único que exigen los
navegadores para permitir "Instalar app".

## Archivos de esta carpeta
- `index.html` — la app completa (incluye la librería para leer/escribir Excel)
- `manifest.json` — datos de la app (nombre, ícono, colores)
- `sw.js` — permite que funcione offline e instalada
- `icon-192.png`, `icon-512.png`, `icon-180.png` — íconos de la app

## Pasos para publicar (una sola vez)

### 1. Crear el repositorio en GitHub
1. Entra a https://github.com y crea una cuenta si no tienes.
2. Arriba a la derecha, toca el **+** → **New repository**.
3. Nombre sugerido: `central-llamadas`.
4. Marca **Public** (Pages gratis requiere que sea público, o privado si tienes plan Pro).
5. Toca **Create repository**.

### 2. Subir los archivos
1. Dentro del repo recién creado, toca **uploading an existing file**
   (o el botón **Add file → Upload files**).
2. Arrastra los 6 archivos de esta carpeta (`index.html`, `manifest.json`,
   `sw.js`, `icon-192.png`, `icon-512.png`, `icon-180.png`) — todos juntos,
   directo en la raíz del repo, sin meterlos en subcarpetas.
3. Abajo, toca **Commit changes**.

### 3. Activar GitHub Pages
1. En el repo, ve a la pestaña **Settings**.
2. En el menú de la izquierda, toca **Pages**.
3. En "Branch", elige **main** y la carpeta **/ (root)**.
4. Toca **Save**.
5. Espera 1-2 minutos. GitHub te va a mostrar un enlace tipo:
   `https://TU-USUARIO.github.io/central-llamadas/`

### 4. Instalar la app en tu celular
1. Abre ese enlace en Chrome (Android) o Safari (iPhone).
2. Android/Chrome: te va a aparecer un aviso o menú (⋮) → **"Instalar app"**
   o **"Agregar a pantalla de inicio"**.
3. iPhone/Safari: botón compartir (□↑) → **"Agregar a pantalla de inicio"**.
4. Listo — queda como ícono, pantalla completa, funciona sin internet una
   vez cargada la primera vez.

## Actualizar la app más adelante
Si en el futuro quieres cambiarle algo:
1. Vuelve al repo en GitHub.
2. Sube el nuevo `index.html` (Add file → Upload files, mismo nombre,
   reemplaza el anterior).
3. La próxima vez que abras la app con internet, se actualiza sola
   (el service worker detecta la versión nueva).

## Importante sobre tus datos
Los contactos que cargues y los resultados que registres viven **solo en
ese celular, en ese navegador**. Si desinstalas la app o borras datos del
navegador, se pierden. Por eso exporta tu Excel de resultados al final de
cada jornada desde la pestaña Reporte — ese es tu respaldo real.
