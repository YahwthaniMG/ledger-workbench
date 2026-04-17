# Ledger Workbench

Interfaz web para ejecutar instrucciones SQL contra una base de datos PostgreSQL remota.
Se comunica con el Ledger API mediante peticiones HTTP y presenta los resultados
en una tabla dinámica con tema oscuro estilo editor de código.

Desplegado en Vercel como sitio estático.

## Funcionalidades

- Editor SQL con números de línea sincronizados y tipografía monoespaciada
- Ejecución con `Ctrl+Enter` o botón Run
- Sidebar con lista de tablas cargada dinámicamente desde el API
- Schema explorer: al hacer clic en una tabla muestra sus columnas, tipos y etiquetas PK/FK
- Historial de las últimas 10 queries guardado en `localStorage`
- Exportar resultados a CSV con un clic
- Indicador de estado de conexión a la base de datos en tiempo real
- Renderizado inteligente por tipo de dato: UUIDs abreviados, números en ámbar, nulls en gris
- Mensajes de error descriptivos con feedback visual

## Stack

- HTML + CSS + JavaScript (vanilla)
- Sin dependencias externas ni frameworks
- Desplegado en Vercel (sitio estático)

## Configuración

La URL del API está definida al inicio del script en `index.html`:

```javascript
const API = 'https://ledger-api-svvr.onrender.com';
```

Si despliegas tu propia instancia del API, cambia este valor por tu URL de Render.

## Instalación local

```bash
git clone https://github.com/YahwthaniMG/ledger-workbench
cd ledger-workbench
```

No requiere servidor ni dependencias. Abre `index.html` directamente en el browser
o usa cualquier servidor estático:

```bash
npx serve .
```

## Deployment

El proyecto se despliega en Vercel conectando el repositorio de GitHub.
Vercel detecta automáticamente que es un sitio estático y no requiere configuración adicional.

## Estructura del proyecto
```
ledger-workbench/
└── index.html    # Aplicacion completa en un solo archivo
```
## Repositorio relacionado

El API que consume este Workbench vive en:
[ledger-api](https://github.com/YahwthaniMG/ledger-api)
