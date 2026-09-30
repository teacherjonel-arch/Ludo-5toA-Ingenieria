# Ludo Matemático — 5.º A Ingeniería

Juego de Ludo Matemático del Colegio San Pío X preparado para funcionar en línea con **Node.js + Express + Socket.IO**.

## Estructura

```text
.
├── public/
│   └── index.html
├── data/
│   └── questions.json
├── server.js
├── package.json
├── render.yaml
├── .gitignore
└── README.md
```

## Probar en la computadora

```bash
npm install
npm start
```

Luego abrir `http://localhost:3000`.

## Subir a GitHub

1. Crear un repositorio nuevo.
2. Subir **todos los archivos y carpetas** de este proyecto.
3. Verificar que `package.json`, `server.js`, `public/index.html` y `data/questions.json` estén en el repositorio.

## Publicar en Render

En Render: **New → Web Service → conectar el repositorio de GitHub**.

- Environment: `Node`
- Build Command: `npm install`
- Start Command: `npm start`

El proyecto también incluye `render.yaml` con esa configuración.

## Juego en red

- El creador escribe su nombre y elige 2, 3 o 4 equipos.
- Los demás jugadores escriben su nombre y usan el código de 6 caracteres.
- La partida puede iniciarse por el anfitrión cuando estén completos los equipos seleccionados.
- El estado del tablero se sincroniza mediante Socket.IO.

## Preguntas

Las preguntas iniciales están en `data/questions.json`. El servidor las carga al iniciar. En Render, el almacenamiento local puede ser efímero; si se necesita conservar cambios del administrador después de reinicios o nuevos despliegues, conviene conectar una base de datos o almacenamiento persistente.
