IFTS N°29
Tecnicatura Superior en Desarrollo de Software
Materia Desarrollo de Sistemas Web (Front End)
Practica formativa obligatoria N°1

Landing de una página que presenta mi perfil, mis habilidades y una vía de contacto.



## Enlaces
**Repositorio:** [https://github.com/otra-tecla/portafolio]
**Despliegue:** [https://portafolio-dun-two-32.vercel.app/]


## Tecnologías

- **HTML5 semántico:** Estructura limpia y accesible (`<header>`, `<nav>`, `<main>`, `<section>`, `<form>`, `<aside>`, `<footer>`).
- **CSS3:**
  - Variables CSS (Custom Properties) para paleta de colores y fuentes.
  - **Flexbox exclusivo:** Maquetación completa en una y dos dimensiones con `display: flex`, `flex-wrap`, `gap` y alineaciones flexibles (sin CSS Grid).
  - Media queries progresivas y escalonadas (cortes en 960px, 768px, 600px y 480px).
  - Animación `@keyframes fadeUp` al cargar las secciones y micro-interacciones suaves (`:hover`, `:focus-visible`).
  - Tipografía y espaciados fluidos mediante la función `clamp()`.
- **Google Fonts:**
  - **Outfit:** Encabezados (`h2`, `h3`), enlaces de navegación (`.nav-link`), etiquetas y botones.
  - **Inter:** Cuerpo de texto general (`p`), inputs y detalles de contacto.
  - **Fira Code:** Monograma e isotipo técnico (`</EA>`).
- **Ícono SVG:** Logotipo oficial de GitHub incrustado de forma inline con atributos de accesibilidad.
- **Sin JavaScript:** 100% de la funcionalidad, estilos y adaptabilidad resueltos de forma nativa con HTML y CSS.

---

## Estructura del proyecto


PortafolioAG/
├── index.html          
├── README.md            
├── css/
│   └── styles.css      
└── assets/
    ├── icons/          
    └── images/
        └── desarrollador.jpg 
```

---


## Decisiones de diseño y desarrollo

### Estructura
- El encabezado (`<header>`) aloja exclusivamente la marca personal (`</EA>`) y la navegación principal (`.menu-nav`).
- Todo el contenido temático reside dentro del contenedor `<main>`, distribuido en cuatro secciones con identificador único para scroll suave: Inicio (`#inicio`), Habilidades (`#habilidades`), Espacio personal (`#espacio-personal`) e Información de contacto (`#contacto`).
- En la sección Inicio, el texto precede a la imagen en el marcado HTML semántico; en pantallas de escritorio se distribuyen horizontalmente en paralelo, mientras que en pantallas móviles el CSS invierte el orden visual (`flex-direction: column-reverse`) para priorizar la fotografía de perfil de forma centrada.

### Maquetación (Flexbox exclusivo)
- Se utilizó **Flexbox en el 100% de la arquitectura** del sitio:
  - `body` con `display: flex; flex-direction: column; min-height: 100vh` para implementar un pie de página *sticky* natural sin trucos de posicionamiento absoluto.
  - Barra de navegación elástica con `justify-content: space-between` y `flex-wrap: wrap`.
  - Contenedor de contacto (`.contact-wrapper`) con `flex-wrap: wrap; gap: 1.5rem`: el formulario y los datos de contacto ocupan columnas proporcionales en escritorio (`flex: 1 1 320px`) y pasan a una columna única fluida en pantallas medianas y móviles.
  - La lista de datos de contacto (`.contact-info ul` y `.contact-info li`) utiliza Flexbox para alinear etiquetas y valores con saltos de línea automáticos (`word-break`).

### Estilización y Tipografía
- Sistema unificado de variables CSS (`:root`): paleta basada en tonos pizarra/azul noche (`#18212f`), acentos en índigo y violeta (`#4f46e5`, `#a78bfa`) y fondo descansado (`#f4f7fb`).
- Tipografía moderna con Google Fonts conectada mediante `preconnect`: contraste nítido entre la modernidad de `Outfit` para títulos/interacción y la legibilidad de `Inter` para los párrafos de lectura.
- Escalado fluido mediante `clamp()`: los tamaños de fuente de títulos y párrafos, así como los rellenos (`padding`), se recalculan dinámicamente según el ancho del viewport en lugar de depender únicamente de saltos estáticos.

### Accesibilidad
- Selectores `:focus-visible` aplicados a todos los elementos interactivos (enlaces, campos de texto y botón) con anillos de enfoque contrastados.
- El ícono SVG de GitHub cuenta con `aria-hidden="true"` y texto visible adyacente para no depender exclusivamente de gráficos.
- Objetivos táctiles mínimos (mínimo 44px de altura) en enlaces del menú y botones para facilitar la navegación en dispositivos táctiles.
- Atributos semánticos `aria-label` en la barra de navegación y enlaces clave.

### Imágenes
- La imagen de perfil (`assets/images/desarrollador.jpg`) se controla con `aspect-ratio: 1 / 1`, `object-fit: cover` y anchos flexibles acotados mediante `clamp()`, previniendo saltos de diseño (*Cumulative Layout Shift*). Dicha magen fue generada a partir del texto del portafolio.

---



## Uso de IA (Gemini 3.8 flash high)

Se incorporaron herramientas de Inteligencia Artificial (asistentes conversacionales y de código) como apoyo durante el proceso de desarrollo para:
- Consulta y discusión de buenas prácticas en arquitectura CSS y estándares de maquetación responsiva con Flexbox.
- Validación de accesibilidad web (foco visible, áreas táctiles mínimas y contraste).
- Revisión de sintaxis y optimización de código.

Todas las propuestas generadas por IA fueron evaluadas, adaptadas y depuradas manualmente. La estructura del documento, las decisiones estéticas, la selección tipográfica y el código final implementado son propios y responden a los criterios del trabajo práctico.




