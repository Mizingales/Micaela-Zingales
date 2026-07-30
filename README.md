# Portfolio — Micaela Zingales

Sitio estático (HTML/CSS/JS puro, sin frameworks) listo para publicar gratis en GitHub Pages.

## Estructura

```
index.html              → Home + Proyectos (landing)
sobre-mi.html
investigacion.html
cv.html
contacto.html
proyecto-censo.html      → Caso de estudio: Censo Digital 2022
proyecto-brandvan.html   → Caso de estudio: Plataforma B2B
proyecto-freelance.html  → Caso de estudio: Freelance
css/style.css
js/main.js
assets/cv/CV_Micaela_Zingales.pdf
assets/img/              → acá van tus imágenes de proyectos
```

## Cómo publicarlo en GitHub Pages (gratis)

1. Creá un repositorio nuevo en GitHub (por ejemplo `micaela-zingales.github.io` para que quede en la raíz de tu usuario, o cualquier nombre si preferís que quede en una subcarpeta tipo `tuusuario.github.io/portfolio`).
2. Subí todo el contenido de esta carpeta a ese repositorio (podés arrastrar los archivos desde la web de GitHub, o con git):
   ```bash
   git init
   git add .
   git commit -m "Primer commit del portfolio"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
   git push -u origin main
   ```
3. En el repositorio, andá a **Settings → Pages**.
4. En "Source" elegí la rama `main` y la carpeta `/ (root)`.
5. Guardá. En unos minutos tu sitio va a estar disponible en:
   - `https://TU-USUARIO.github.io/` (si el repo se llama `TU-USUARIO.github.io`)
   - o `https://TU-USUARIO.github.io/TU-REPO/` (para cualquier otro nombre de repo)

## Cómo cargar tus imágenes

Cada proyecto tiene recuadros con borde punteado y un texto que indica la ruta esperada, por ejemplo `assets/img/censo-01.jpg`. Pasos:

1. Guardá tus imágenes dentro de `assets/img/` con esos nombres (o los que prefieras).
2. En el HTML, reemplazá el bloque:
   ```html
   <div class="project-visual">
     <span class="tag">Gob</span>
     <p class="placeholder-text">Reemplazar por captura del proyecto...</p>
   </div>
   ```
   por:
   ```html
   <div class="project-visual">
     <span class="tag">Gob</span>
     <img src="assets/img/censo-01.jpg" alt="Descripción de la imagen">
   </div>
   ```
   Los recuadros de `case-visual` y `project-hero-visual` funcionan igual.

## Cómo editar textos de cada proyecto

Cada archivo `proyecto-*.html` tiene tres bloques: **Contexto**, **Proceso** y **Resultado**. Son simples párrafos `<p>` — podés reemplazarlos o agregar más sin romper nada del diseño.

## Personalización rápida

- **Colores/tipografías:** todo está centralizado en `css/style.css`, en el bloque `:root` al principio del archivo.
- **Nuevo proyecto:** duplicá cualquier `proyecto-*.html`, cambiale el contenido, y agregá una nueva `<article class="project-row">` en `index.html` que apunte a él.
