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

APUNTES EXAMEN 

 examen – Portfolio de Carlota Fernández
 
¿Para qué sirve Visual Studio Code?
Visual Studio Code es el programa que utilizo para escribir y organizar el código de mi
portfolio. Es un editor de código que me permite trabajar con HTML, CSS y JavaScript de
forma ordenada, ver errores, usar extensiones y mantener todos los archivos del proyecto
bien estructurados.

¿Qué es HTML?
HTML es el lenguaje que se utiliza para estructurar una página web. En mi portfolio lo uso
para definir qué es cada cosa: títulos, párrafos, secciones, imágenes o enlaces. No da
estilo, solo orden y significado al contenido.

¿Qué es un IDE?
Un IDE es un Entorno de Desarrollo Integrado. Es un programa que reúne herramientas
para programar en un mismo sitio. Visual Studio Code funciona como un IDE porque me
permite escribir código, organizar archivos y depurar errores.

¿Para qué sirve GitHub?
GitHub sirve para guardar el proyecto en la nube y llevar control de versiones. En mi
portfolio lo uso para guardar el historial de cambios, trabajar de forma ordenada y poder
desplegar la web en GitHub Pages.

¿Qué son los elementos semánticos de HTML?
Son etiquetas que describen el contenido que envuelven. En mi web uso elementos como
header, nav, main, section, article y footer para que la estructura sea clara, accesible y
mejor entendida por buscadores.

¿Qué es index.html?
index.html es la página principal del proyecto. Es la primera que se carga cuando alguien
entra a mi portfolio y desde ella se accede al resto del contenido.

¿Qué es DOCTYPE?
DOCTYPE indica al navegador qué tipo de documento está leyendo. En mi web uso
HTML5 para asegurar compatibilidad con navegadores modernos.
¿Qué es una ruta absoluta y una relativa?

Una ruta absoluta apunta a una dirección completa. Una ruta relativa depende del archivo
desde el que se llama. En mi portfolio uso rutas relativas para enlazar imágenes, CSS y
JavaScript.

¿Qué es Mobile First?
Mobile First significa diseñar primero para móvil y luego adaptar a pantallas grandes. En
mi web empecé pensando en móvil y después añadí media queries para tablet y desktop.

¿Qué son las media queries?
Las media queries permiten cambiar el diseño según el tamaño de la pantalla. Las uso
para reorganizar grids, carruseles y tamaños de texto en móvil, tablet y escritorio.

¿Qué estrategias de maquetación usas?
Utilizo Flexbox y CSS Grid. Flexbox me sirve para alinear elementos en filas o columnas y
Grid para crear estructuras más complejas como las tarjetas de proyectos.

¿Qué es una SPA?
Una SPA es una web de una sola página. Mi portfolio funciona así: todo el contenido está
en un único HTML y se navega mediante anclas.

¿Qué es un favicon?
Un favicon es el pequeño icono que aparece en la pestaña del navegador. En mi web lo
añadí para reforzar la identidad visual.

¿Qué es refactorizar?
Refactorizar es mejorar el código por dentro sin cambiar lo que se ve por fuera. En mi
proyecto lo hice al reorganizar el CSS en archivos más claros.

¿Qué parte del proyecto te hace sentir más orgullosa?
Me siento especialmente orgullosa de las secciones de editorial, fotografía e ilustración,
donde combiné diseño visual, carruseles, responsive y animaciones manteniendo
coherencia estética.

¿Qué tipo de web es tu portfolio?
Es una web 1.0 porque muestra información y trabajos, pero no permite que el usuario
interactúe más allá de navegar y contactar.

¿Qué es un CDN?
Un CDN es una red de servidores que sirve recursos más rápido. En mi web uso CDNs
para cargar tipografías de Google Fonts.

¿Qué es Markdown?
Markdown es un lenguaje sencillo para escribir documentación. Lo utilizo en el README
y los archivos de planificación del proyecto.

APUNTES TEORÍA PROGRAMACIÓN WEB EXTENDIDO


1. ¿Qué es la Web?
La Web es una serie de recursos identificados mediante URI.
Un recurso puede ser:
● una página
● una imagen
● un vídeo
● un documento
● una sección concreta dentro de una página
Estructura de una dirección web
● URL:
Está formada por:
○ esquema (https)
○ host (github.io)
○ path (/portfolio/...)
● URI:
Incluye el URL y la parte específica del recurso:
○ lo que va después de #
○ identifica un recurso concreto dentro de una página
👉 Una página puede tener muchos recursos, cada uno con su URI.
Origen
● TCP/IP: 1969
● Web: 1989

2. Tipos de Web
Web 1.0
● Comunicación unidireccional
● Del servidor al usuario
● El usuario no interactúa

● No hay backend
● Es la web que estamos haciendo en clase
Web 2.0
● El usuario interactúa
● Puede crear contenido
● Formularios, comentarios, perfiles
● Necesita backend
Web 3.0
● Integración con servicios externos
● APIs, sistemas inteligentes, automatización
● Intervienen más agentes además del usuario y el servidor
👉 Nuestro proyecto es Web 1.0 porque:
● solo hacemos frontend
● no hay backend
● no se procesan formularios

3. Web Semántica
La web semántica es aquella cuya estructura da información sobre el contenido.
Esto permite:
● indexación semántica
● mejor posicionamiento
● mejor accesibilidad
Se consigue mediante:
● HTML semántico (header, nav, main, section, article, etc.)
● meta-etiquetas
● buena jerarquía de contenido

4. ¿Qué es una aplicación web?
Una aplicación web es una aplicación cliente-servidor que utiliza un navegador web
como cliente.
Funciona mediante:

● request (petición)
● response (respuesta)

5. Protocolo de comunicación
¿Qué protocolo sigue tu página web?
● HTTP / HTTPS
Diferencia entre HTTP y HTTPS
● HTTPS es HTTP cifrado
● Forma parte de la familia TCP/IP
● Aporta seguridad
Puerto
● HTTP → 80
● HTTPS → 443
👉 Nuestra web funciona en 443 porque usamos HTTPS (GitHub Pages).

6. Cliente – Servidor
● El cliente hace una request
● El servidor devuelve una response
● No hay comunicación directa sin protocolo

7. ¿Dónde está alojada nuestra web?
● En GitHub Pages
● GitHub actúa como servidor web
● No hay backend

8. Lenguajes que usamos en el proyecto
● HTML
● CSS

● JavaScript
● Markdown (MD) → README
HTML
● Lenguaje de marcación
● Usa elementos y atributos
● Tiene:
○ <head>
○ <body>

HTML5
● Versión moderna
● Se independizó de versiones anteriores
● Permite:
○ geolocalización
○ cámara
○ recursos avanzados
● Es el que usamos
CSS
● Usamos CSS3
● Controla el diseño visual
JavaScript
● Interactividad
● Lógica
● Animaciones

9. Git y control de versiones
Git:
● Sistema de control de versiones
● Guarda cambios
● Permite volver atrás
● Organiza versiones
GitHub:
● Aloja repositorios
● Permite despliegue
● Trabajo colaborativo

10. CDN (Content Delivery Network)
Un CDN es un tipo de servidor optimizado para distribuir contenido multimedia.
Ejemplo:
● ImageKit.io
Ventajas:
● mayor velocidad
● servidores distribuidos
● mejor rendimiento

11. APIs
Una API permite que distintos servicios de software se comuniquen.
Todas las máquinas necesitan APIs.
Ejemplos que usamos:
● Adobe Fonts
● ImageKit.io
Funcionamiento:
● hablamos con su API
● mediante HTTP
● nos devuelven recursos desde su CDN

12. Responsive Design (Responsabilidad)
El responsive no es automático, es responsabilidad del desarrollador.
Técnicas que usamos
Viewport
● Meta etiqueta obligatoria
● Sin viewport no hay responsive

Media Queries
● Adaptan el diseño a distintos tamaños
Clamp()
● Tamaños fluidos
● Escalan según el dispositivo
Grid y Flexbox
● Estructuración en filas y columnas
● Diseño adaptable

13. Media Queries
Sirven para:
● cambiar estilos según tamaño
● adaptar layout
● mejorar experiencia
👉 En el examen:
● qué son
● cómo las usas
● dónde las aplicas

14. Modales
Un modal es una ventana emergente que:
● aparece sin cambiar de página
● mantiene el contexto
Formas de implementar modales
CSS (:target)
● Tiene limitaciones
● No se puede cerrar con esc
● Pierde foco
JavaScript

● Más control
● Accesibilidad
● Bloqueo del fondo
● Cierre con esc
Nativo (dialog)
● Soporte del navegador
● Gestión automática del foco

15. GSAP
● Librería de JavaScript
● Animaciones
● Transiciones suaves
● Control avanzado del movimiento

16. Respuestas directas a TODAS las preguntas
¿Qué protocolo usa tu web?
Mi web utiliza HTTPS, que es la versión segura del protocolo HTTP.

Diferencia entre HTTP y HTTPS
HTTP transmite la información en texto plano, mientras que HTTPS cifra la comunicación,
haciendo la conexión segura. HTTPS forma parte de la familia de protocolos TCP/IP.

¿Qué es TCP/IP?
TCP/IP es el conjunto de protocolos que permite la comunicación entre dispositivos en
Internet. Es la base sobre la que funciona la Web y otros servicios de red.

¿En qué puerto funciona tu web?
Mi web funciona en el puerto 443, que es el puerto estándar del protocolo HTTPS.

Diferencia entre URL y URI
La URL indica la dirección de un recurso (esquema, host y path).
La URI identifica un recurso concreto, incluyendo fragmentos como lo que va después del
símbolo #.

¿Qué tipo de web estás haciendo?
Estoy haciendo una Web 1.0, ya que es una web unidireccional que va del servidor al
usuario y no permite interacción ni backend.

¿Por qué no es Web 2.0?
No es Web 2.0 porque el usuario no puede crear contenido ni interactuar con el servidor
mediante formularios o sistemas de autenticación. No existe backend.

¿Qué lenguajes usas?
Utilizo HTML, CSS, JavaScript y Markdown para la documentación (README).

¿Qué versión de HTML usas?
Utilizo HTML5, la versión más reciente del lenguaje de marcación, que permite
funcionalidades modernas como acceso a dispositivos y APIs del navegador.

¿Qué es una API?
Una API es una interfaz que permite la comunicación entre distintos servicios de software.
Permite solicitar y recibir datos o recursos de otros sistemas.

¿Qué es un CDN?
Un CDN es una red de servidores optimizada para distribuir contenido, especialmente
multimedia, de forma más rápida y eficiente. Un ejemplo es ImageKit.

¿Cómo haces responsive?
Hago responsive la web utilizando:
● meta viewport
● media queries
● tamaños fluidos con clamp
● sistemas de layout como Flexbox y Grid

¿Qué es viewport?
El viewport es la zona visible de la página en el navegador. Se define mediante una
meta-etiqueta y es imprescindible para que el diseño responsive funcione.

¿Qué son media queries?
Las media queries son reglas CSS que permiten aplicar estilos distintos según el tamaño o
las características del dispositivo.

¿Qué es clamp?
Clamp es una función de CSS que permite definir tamaños fluidos con un valor mínimo, uno
ideal y uno máximo, adaptándose al tamaño de pantalla.

¿Flexbox o Grid?
Uso ambos:
● Flexbox para alineación y elementos en una sola dimensión
● Grid para estructurar layouts en filas y columnas

¿Qué es un modal?
Un modal es una ventana emergente que aparece sobre la página sin cambiar de contexto y
bloquea la interacción con el fondo.

¿Cómo implementas modales?
Los modales se implementan principalmente con JavaScript, ya que permite un mayor
control, mejor accesibilidad y cierre mediante teclado.

¿Dónde está alojada tu web?
La web está alojada en GitHub Pages, que actúa como servidor web.

¿Qué es Git?
Git es un sistema de control de versiones que permite registrar, organizar y gestionar los
cambios realizados en un proyecto.

¿Para qué sirve GitHub?
GitHub sirve para alojar repositorios Git, colaborar en proyectos, gestionar versiones y
desplegar sitios web como GitHub Pages.


