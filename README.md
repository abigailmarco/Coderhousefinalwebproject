(https://sparkly-selkie-ea34ae.netlify.app)
# Impact Logic™

Proyecto final del curso: un sitio web estático de 5 páginas para Impact Logic, una empresa que diseña productos para prevenir lesiones y golpes de calor en deportistas. Elegí este tema porque conozco el proyecto de cerca y me pareció un buen desafío armar un sitio real, con contenido de verdad, en lugar de uno de prueba.

**Sitio online:** (https://6adfa4aaa4ab4e7a67a4dea3--sparkly-selkie-ea34ae.netlify.app/pages/cryo-chair)

## Qué hay en el sitio

- **Inicio (`index.html`)**: presentación de la marca, por qué elegirla, un resumen de los tres productos y un estudio de la Universidad de Texas sobre cascos de espuma.
- **The Vortex (`pages/the-vortex.html`)**: el forro de casco con cápsulas de gel que enfría la cabeza, con los estudios científicos en los que se basa.
- **NekProTek (`pages/nekprotek.html`)**: el protector de cuello, en su versión para hockey y para ciclismo.
- **Cryo Chair (`pages/cryo-chair.html`)**: la silla portátil para bajar la temperatura de los jugadores.
- **Nosotros (`pages/about.html`)**: la historia del fundador, la misión y su investigación.

El formulario de contacto está en el footer de todas las páginas, así que el link "Contact Us" del menú baja directamente hasta ahí.

## Cómo lo hice

**HTML:** usé etiquetas semánticas (`header`, `nav`, `main`, `section`, `article`, `footer`, etc.). Cada página tiene su propio `title`, `meta description` y `meta keywords`, y todas las imágenes tienen `alt`.

**Bootstrap:** el menú es la navbar de Bootstrap, con el botón hamburguesa para mobile y un desplegable para los productos. Lo estilé desde SCSS para que mantenga los colores de la marca y no se vea como la navbar por defecto.

**SCSS:** todos los estilos están en la carpeta `scss/`, divididos en partials. El `main.scss` solamente tiene los `@use`. Trabajé con:
- variables para colores, tipografía, espaciados y breakpoints
- mixins con parámetros, por ejemplo `respond()` para las media queries y `grid-cols()` para las grillas
- `@extend` con placeholders (`%panel`, `%muted-text`, `%list-reset`)
- nesting en todos los componentes

El CSS compilado queda en `styles/main.css`.

**Responsive:** lo armé mobile first, con media queries en 768px (tablet) y 992px (desktop). Lo probé en los tres tamaños y no aparece scroll horizontal en ninguna página.

**Animaciones:** por un lado hice animaciones propias con `@keyframes` (el título y la imagen del inicio) y `transition` en botones, tarjetas y links del menú. Por otro lado usé la librería AOS para que las secciones aparezcan a medida que se hace scroll.

## Estructura de carpetas

```
├── index.html
├── pages/
├── scss/
│   ├── main.scss
│   ├── abstracts/
│   ├── base/
│   ├── components/
│   ├── layout/
│   └── pages/
├── styles/
└── assets/
    ├── images/
    └── icons/
```

## Para compilar el SCSS

```bash
npm install
npm run sass
```

Con eso queda escuchando cambios y recompila solo cada vez que guardo.

---

Hecho por Abigail Marco
