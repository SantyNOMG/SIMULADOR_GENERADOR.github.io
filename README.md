# Simulador de generador eléctrico de corriente alterna

Simulación 2D interactiva (p5.js) de un generador de CA: ley de Faraday, ley de Lenz, flujo magnético, voltaje, corriente y potencia en tiempo real. Funciona sin servidor ni internet (p5.js 1.9.4 está incluido en `js/lib/`).

## Importante
`index.html` es **autónomo**: lleva dentro el CSS, el JavaScript y p5.js, así que funciona aunque se suba solo. **Extrae el ZIP antes de abrirlo** (si abres `index.html` desde dentro del ZIP verás la página sin estilos).
La carpeta `src/` contiene la versión modular (archivos separados) para editar el proyecto; ábrela con `src/index.html`.

## Estructura (en src/)
`index.html` · `css/style.css` · `js/physics.js` (ecuaciones) · `js/generator.js` (estado y tiempo) · `js/animations.js` (dibujo p5.js) · `js/interface.js` (controles y lecturas) · `js/main.js` · `js/lib/p5.min.js` · `assets/icons/favicon.svg`

## Ejecutar localmente
Abre `index.html` con doble clic en tu navegador (Chrome, Edge, Firefox). Si tu navegador bloquea algo, en la carpeta ejecuta `python -m http.server 8000` y abre `http://localhost:8000`.

## Subir a GitHub
1. Descomprime el ZIP. Entra a github.com → **New repository**, ponle un nombre (por ejemplo `generador-electrico`) y créalo como **Public**.
2. En el repositorio: **Add file → Upload files**. Arrastra **el contenido** de la carpeta descomprimida (`index.html`, `css`, `js`, `assets`, `README.md`), no la carpeta contenedora. Pulsa **Commit changes**.

## Activar GitHub Pages
1. **Settings → Pages**. En *Build and deployment*, elige **Deploy from a branch**.
2. Rama **main**, carpeta **/ (root)** → **Save**.
3. Espera 1–2 minutos. La dirección será `https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`. Usa esa dirección para generar tu código QR.

Las rutas son relativas, así que funciona aunque el nombre del repositorio forme parte de la URL.

## Modelo físico
ε(t) = N·B·A·ω·sen(ωt) · ΦB = B·A·cos(ωt) · I = ε/R · P = ε²/R, con R = 50 Ω. Modelo ideal (sin pérdidas ni autoinductancia); ver la sección "Modelo ideal y limitaciones" en la app.
