# Calculadora de cambio CLP ↔ multi-moneda

Prototipo conectado en tiempo real a Binance P2P.

## Qué hay en esta carpeta

- `index.html` → la calculadora (lo que ve el usuario).
- `api/binance-price.js` → la función que consulta Binance P2P (el "proxy").
- `package.json` → archivo de configuración mínimo que necesita Vercel.

## Pasos para publicarlo

### 1. Crear un repositorio en GitHub

1. Entra a github.com y entra a tu cuenta.
2. Haz clic en "New repository" (Nuevo repositorio).
3. Ponle un nombre, por ejemplo: `calculadora-cambio`.
4. Déjalo en "Public" o "Private", como prefieras.
5. Crea el repositorio (sin agregar README, .gitignore, etc. — vacío).

### 2. Subir los archivos

1. Dentro del repositorio recién creado, busca el botón "Add file" → "Upload files".
2. Arrastra estos 3 elementos manteniendo la misma estructura de carpetas:
   - `index.html`
   - la carpeta `api` completa (con `binance-price.js` adentro)
   - `package.json`
3. Confirma la subida ("Commit changes").

Importante: la carpeta `api` debe quedar en la raíz del repositorio, al mismo nivel que `index.html` — Vercel la detecta automáticamente por su nombre.

### 3. Conectar con Vercel

1. Entra a vercel.com con tu cuenta.
2. Haz clic en "Add New..." → "Project".
3. Elige "Import Git Repository" y selecciona el repositorio `calculadora-cambio` que acabas de crear.
4. Déjalo con la configuración por defecto (no hace falta cambiar nada) y haz clic en "Deploy".
5. Espera unos segundos — Vercel te dará una URL como `calculadora-cambio.vercel.app`.

### 4. Probar

1. Abre la URL que te dio Vercel.
2. La calculadora debería mostrar "Consultando precios en Binance P2P..." y luego actualizar los precios automáticamente.
3. Si algo falla, el mensaje de estado debajo del botón "Actualizar precios" mostrará el motivo (y mientras tanto puedes seguir usando la calculadora editando los precios a mano).

## Actualizaciones futuras

Cada vez que edites un archivo directamente en GitHub (por ejemplo, desde el navegador, con el lápiz de "editar"), Vercel detecta el cambio y vuelve a publicar automáticamente en unos segundos — no hay que repetir el proceso de importar el proyecto.
