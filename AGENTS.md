# Google Antigravity Agent Rules - Book Store (Cozy & Indie Style)

## 1. Contexto del Proyecto & Rol del Agente
- **Proyecto:** Sitio web frontend para una librería online (**Book Store**) con temática cálida, acogedora e independiente (*cozy / indie-looking*).
- **Rol del Agente:** Actuar como desarrollador Frontend Senior y Diseñador UI/UX especializado en interfaces acogedoras e intuitivas.
- **Flujo de Ejecución:** Ante cambios complejos, seguir el ciclo: **Explorar -> Planificar (Implementation Plan) -> Ejecutar -> Verificar**.

---

## 2. Estructura y Organización del Proyecto (ESTRICTO)
Es obligatorio mantener y respetar exactamente la siguiente estructura de archivos y carpetas:

```text
/
├── index.html            # Página principal de la tienda (Catálogo/Productos)
├── pages/
│   └── contacto.html     # Página de contacto con formulario (Integración con Formspree)
├── css/
│   └── styles.css        # Archivo CSS externo principal
├── img/                  # Carpeta contenedora de imágenes de productos y assets
└── AGENTS.md             # Reglas globales de Antigravity
```

### Prohibiciones de Estructura:
- ⛔ **NO** crear archivos HTML en la raíz distintos de `index.html`.
- ⛔ **NO** modificar los nombres de las carpetas (`css`, `img`, `pages`).
- ⛔ **NO** crear múltiples archivos CSS; toda la estilización debe ir en `css/styles.css`.

---

## 3. Directivas Técnicas HTML & CSS

### 3.1. Estilos y CSS Externo
- ⛔ **Prohibido CSS Inline:** No utilizar el atributo `style="..."` dentro de ninguna etiqueta HTML.
- ⛔ **Prohibido CSS Interno:** No incluir la etiqueta `<style>` dentro del `<head>` o `<body>` de ningún archivo HTML.
- All styles MUST be contained inside `css/styles.css` and linked using `<link rel="stylesheet" href="...">`.

### 3.2. Semántica HTML5
- Utilizar adecuadamente las etiquetas semánticas: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, y `<footer>`.
- En `index.html`, representar las tarjetas de los libros dentro de un contenedor `<section>` utilizando elementos `<article>` para cada producto.
- En `pages/contacto.html`, el formulario debe estructurarse con `<form action="https://formspree.io/f/..." method="POST">`, `<label>`, `<input>`, `<textarea>`, y `<button type="submit">`.

### 3.3. Posicionamiento y Layout (Flexbox)
- **Flexbox Mandatory:** Utilizar `display: flex`, `flex-wrap`, `justify-content`, `align-items` y `gap` para el maquetado del catálogo, encabezados y formulario.
- **Diseño Responsivo:** Prohibido el desborde horizontal (*overflow-x* / scroll lateral no deseado) en pantallas pequeñas o al achicar la ventana.
- Las tarjetas de productos deben reacomodarse de forma fluida conforme varíe el ancho del viewport.

---

## 4. Guía de Estilo y UI/UX (Cozy & Indie Theme)
- **Paleta de Colores:** Tonos cálidos y naturales. Cremas, beiges, terracota suave, verde oliva, madera y café.
- **Tipografía:** Usar Google Fonts (combinación de una fuente Serif o Handwritten para títulos y Sans-serif limpia para lectura general).
- **Componentes Visuales:** Tarjetas de libros con bordes ligeramente redondeados (`border-radius`), sombras suaves (`box-shadow`), e interacciones `:hover` sutiles.

---

## 5. Verificación & Sandboxing
- **Verificación Visual (Browser Sub-Agent):** Utilizar las capacidades de visión para revisar que el diseño se vea correctamente alineado y sin desbordes.
- **Pruebas Responsivas:** Simular resoluciones móviles y de escritorio para confirmar el ajuste adecuado de los elementos mediante Flexbox.
- **Seguridad:** Solicitar confirmación antes de ejecutar comandos destructivos o modificar rutas fuera de la raíz del workspace.
