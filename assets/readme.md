# Portfolio de Diseño Gráfico

Portfolio personal desarrollado con **HTML, CSS y JavaScript vanilla**, partiendo de una plantilla base y adaptándola progresivamente hacia un portfolio profesional de diseño gráfico.

Este repositorio se documenta con un **enfoque académico**, registrando errores, aprendizajes y soluciones técnicas en cada etapa del desarrollo.

> Nota:  
> El portfolio (interfaz y contenidos) está en **inglés** por motivos profesionales.  
> La documentación se presenta en **español** con fines académicos.

---

## Objetivos del proyecto

- Construir un portfolio web moderno, accesible y responsive.
- Aplicar principios de **diseño de sistemas** mediante CSS Custom Properties.
- Implementar animaciones performantes y accesibles.
- Utilizar buenas prácticas de Git con commits claros y documentados.
- Reflexionar sobre errores y decisiones técnicas durante el proceso.

---

## Tecnologías utilizadas

- HTML5 semántico
- CSS3 (Custom Properties, Grid, Flexbox, clamp)
- JavaScript Vanilla
- IntersectionObserver API
- Visual Studio Code
- Git

---

## Estructura del proyecto
assets/
├── css/
│ ├── reset.css
│ ├── base.css
│ ├── theme.css
│ ├── layout.css
│ ├── navigation.css
│ ├── components.css
│ └── index.css
└── js/
└── main.js
index.html
README.md


## Registro académico del desarrollo

### Commit 1 — Establecimiento de la línea base del proyecto

**Qué se hizo**
- Limpieza y adaptación del HTML base.
- Corrección del idioma del documento y título del sitio.
- Aplicación del atributo `defer` al script principal.
- Definición de un sistema de diseño con CSS Custom Properties.
- Corrección y mejora de estilos base y accesibilidad.
- Integración coherente de componentes visuales con tokens de diseño.

**Errores o problemas detectados**
- Uso incorrecto del selector `body body`, lo que impedía que los estilos se aplicaran.
- Intento de anidar `:focus-visible` dentro de otro selector, lo cual no es válido en CSS plano.
- Uso de valores “hardcodeados” (px fijos) que rompían la coherencia visual.

**Aprendizajes**
- Los selectores CSS no se anidan de forma nativa.
- `:focus-visible` debe declararse como regla independiente.
- El atributo `defer` permite cargar JavaScript sin bloquear el parseo del HTML.
- Los design tokens permiten un diseño más escalable y mantenible.
- Accesibilidad y rendimiento deben considerarse desde el inicio, no al final.

**Soluciones aplicadas**
- Corrección del selector a `body`.
- Reubicación correcta de `:focus-visible`.
- Sustitución de valores fijos por variables CSS.
- Implementación de un sistema de tokens para tipografía, espaciado, color y superficie.
- Mejora de estados `hover` y `focus-visible` en componentes interactivos.

---

## Convención de commits

Se utiliza una convención inspirada en **Conventional Commits**:

- `chore:` tareas de configuración o base del proyecto
- `style:` cambios visuales (CSS)
- `fix:` corrección de errores
- `feat:` nuevas funcionalidades
- `docs:` documentación

> Regla del proyecto:  
> A partir del **commit 3**, cada commit incluye una actualización del README documentando el proceso.

---

## Próximos pasos

- Definir layout y ritmo vertical del sitio.
- Ajustar navegación y jerarquía visual.
- Convertir proyectos en **casos de estudio**.
- Optimizar accesibilidad y experiencia de usuario.