#  Portfolio — Diseño Gráfico y Visual

 **Deploy:**  
 https://carlotafdez7.github.io/portfolio/

---

## Descripción del proyecto

Este proyecto consiste en el desarrollo de mi **portfolio personal como diseñadora gráfica**, ilustradora y fotógrafa, construido íntegramente con **HTML, CSS y JavaScript vanilla**, sin frameworks ni librerías externas.

El objetivo principal ha sido crear una web **visual, coherente y profesional** que represente mi identidad como diseñadora, pero también demostrar de forma práctica los conocimientos adquiridos durante el curso en **diseño web, arquitectura CSS, animaciones, responsive design y control de versiones**.

El portfolio recoge distintos tipos de proyectos:

- Editorial  
- Ilustración  
- Fotografía  
- Motion graphics  
- Branding  

Todos ellos organizados por secciones, con especial atención al **ritmo visual**, la **jerarquía tipográfica** y la **experiencia de usuario**.

---

## Enfoque y objetivos de aprendizaje

Durante el desarrollo de este proyecto he trabajado especialmente:

- Diseño **mobile-first** y responsive  
- Arquitectura CSS modular y escalable  
- Uso de **CSS moderno** (`clamp()`, Grid, Flexbox, `backdrop-filter`, `animation-timeline`)  
- Animaciones ligadas al scroll con **IntersectionObserver**  
- Control de versiones profesional con **Git y GitHub**  
- Documentación del proceso de diseño y desarrollo  
- Uso responsable y documentado de **IA como apoyo**, no como sustituto  

---

## Stack tecnológico

- **HTML5 semántico**
- **CSS3 moderno**
  - CSS Custom Properties (design tokens)
  - Grid & Flexbox
  - Animaciones con `@keyframes`
  - Parallax con `animation-timeline: scroll()`
- **JavaScript Vanilla**
  - IntersectionObserver
  - Scroll suave
  - Menú hamburguesa accesible
- **Git & GitHub**
- **GitHub Pages** (despliegue)

---

## Estructura del proyecto
portfolio/
├── index.html
├── 404.html
├── assets/
│ ├── css/
│ │ ├── base/
│ │ ├── layout/
│ │ ├── components/
│ │ └── index.css
│ ├── js/
│ │ └── main.js
│ └── img/
│ ├── editorial/
│ ├── ilustracion/
│ ├── fotografia/
│ ├── branding/
│ └── motion-graphics/
├── docs/
│ ├── plan1.md
│ ├── plan2.md
│ └── plan3.md
├── README.md
├── LICENSE
└── .gitignore


---

##  Control de versiones y flujo de trabajo

Desde el inicio del proyecto he trabajado con un **repositorio en GitHub**, manteniendo un flujo de trabajo constante y organizado:

- Commits frecuentes y descriptivos  
- Separación por funcionalidades (estructura, secciones, animaciones, responsive, etc.)  
- Actualización continua del README para documentar decisiones y aprendizajes  
- Preparación del proyecto para una **release final (v1.0.0)**  

---

##  Uso de Inteligencia Artificial (IA)

Durante el desarrollo del proyecto he utilizado **IA (ChatGPT)** como **herramienta de apoyo**, principalmente para:

- Planificar soluciones antes de implementarlas  
- Resolver bloqueos técnicos complejos  
- Revisar arquitectura CSS y enfoque responsive  
- Comprender mejor conceptos avanzados (IntersectionObserver, parallax, mobile-first)  

 **La IA no ha generado el proyecto completo**, sino que se ha utilizado como un **asistente**, siguiendo siempre un flujo en dos fases:

### Fase 1 — Planificación
Antes de implementar cambios importantes, se solicitó a la IA un **plan de acción**, que quedaba documentado.

### Fase 2 — Implementación
Una vez entendido el plan, la implementación se realizó manualmente.

Esta planificación se recoge en los archivos:

- `docs/plan1.md`
- `docs/plan2.md`
- `docs/plan3.md`

---

##  Proceso de desarrollo (diario reflexivo)

### 1 Estructura inicial

El primer reto fue definir la estructura general del portfolio: qué secciones debía incluir y cómo organizar los proyectos.  
Decidí separar el contenido por **disciplinas**, ya que refleja mejor mi perfil como diseñadora multidisciplinar.

---

### 2 Diseño visual y tipografía

Uno de los aspectos clave fue el sistema tipográfico. Se implementó una **escala fluida con `clamp()`**, permitiendo que los textos se adaptaran de forma natural a distintos tamaños de pantalla sin depender de breakpoints rígidos.

---

### 3 Animaciones y scroll

Se trabajaron animaciones ligadas al scroll mediante **IntersectionObserver**. Al principio las animaciones no se activaban correctamente, lo que me obligó a entender mejor cómo funciona la detección de elementos en viewport y la relación entre JavaScript y CSS.

---

### 4 Carruseles, imágenes y vídeo

Se implementaron carruseles de imágenes y vídeos para mostrar proyectos de motion graphics.  
Aquí surgieron problemas especialmente en móvil:

- Imágenes recortadas  
- Vídeos mal escalados  
- Alturas inconsistentes  

Estos problemas se resolvieron ajustando `object-fit`, `aspect-ratio` y replanteando el layout desde un enfoque mobile-first.

---

### 5 Responsive design (el mayor reto)

Aunque el diseño funcionaba correctamente en desktop, en móvil aparecieron numerosos errores. Esto me obligó a:

- Replantear la arquitectura CSS  
- Simplificar layouts complejos  
- Forzar grids de una sola columna en móvil  
- Revisar desbordamientos horizontales  

Este proceso fue largo, pero fundamental para entender el **responsive design real**, más allá de la teoría.

---

### 6 Página 404 personalizada

Se creó una página **404 personalizada**, coherente con el estilo del portfolio, incluyendo:

- Mensaje claro de error  
- Tono cercano y creativo  
- Enlace de vuelta a la página principal  

---

## Accesibilidad y buenas prácticas

- HTML semántico  
- Jerarquía correcta de encabezados  
- Uso de `aria-label`  
- Menú hamburguesa accesible  
- Respeto a `prefers-reduced-motion`  

---

## 7 Aprendizajes principales

- La importancia de planificar antes de escribir código  
- La diferencia entre que algo “funcione” y que esté bien estructurado  
- El valor del control de versiones y la documentación  
- Cómo enfrentarse a bloqueos técnicos sin abandonar  
- Uso ético y consciente de la IA como apoyo al aprendizaje  

---

## 8  ©Licencia

Este proyecto está licenciado bajo la licencia **MIT**.  
Consulta el archivo `LICENSE` para más información.

---

## 9 Agradecimientos

Agradeimiento especial a ti Rubén porque nunca me habría visto capaz de hacerme un portfolio, programado por mi misma , de hecho una de las razones por las que me cambié de carrera fué la cantidad de programación que había, y realmente se me ha quitado el miedo al código este cuatri y lo estoy llegando a disfrutar jajajaja, puede llegar a ser divertido asi que gracias porque nunca lo habría imaginado y estoy muy contenta.


