# Portfolio — Carlota Fernández  
**Sitio en vivo:** https://carlotafdez7.github.io/portfolio/

---

## Descripción del proyecto
Este proyecto es un portfolio personal diseñado para mostrar mi trabajo como diseñadora gráfica, ilustradora y creadora visual, con especial atención al diseño editorial, la fotografía, los motion graphics y el branding.

El objetivo no es solo presentar los proyectos de forma visual, sino también demostrar un flujo de trabajo profesional en front-end, utilizando HTML semántico, CSS moderno y JavaScript en estado puro (vanilla).

---

## Stack tecnológico
- **HTML5** — estructura semántica y accesibilidad
- **CSS3** — Grid, Flexbox, tipografía fluida con `clamp()`, animaciones modernas
- **JavaScript (Vanilla)** — IntersectionObserver, scroll suave, estados activos de navegación
- **Git & GitHub** — control de versiones y despliegue

---

## Diario de desarrollo

Esta sección documenta el proceso de desarrollo de forma académica y reflexiva, incluyendo errores, aprendizajes y soluciones.

### Día 1 — Configuración inicial y estructura
**Qué hice**
- Creación de la estructura base del HTML usando etiquetas semánticas.
- Organización de carpetas (`assets/css`, `assets/js`, `assets/img`).
- Inicialización del repositorio en GitHub.

**Problemas**
- Dudas sobre cómo estructurar correctamente los archivos CSS.
- Confusión inicial sobre el orden de carga del JavaScript.

**Qué aprendí**
- Una buena estructura de carpetas facilita el mantenimiento y la escalabilidad.
- El uso del atributo `defer` permite que el JavaScript se cargue sin bloquear el HTML.

**Cómo lo resolví**
- Separé el CSS en secciones lógicas.
- Añadí `defer` al archivo `main.js`.

---

### Día 2 — Layout y diseño responsive
**Qué hice**
- Construcción de las secciones Hero, About y Work.
- Implementación de layouts con CSS Grid y Flexbox.
- Aplicación de tipografía fluida con `clamp()`.

**Problemas**
- Falta de espacio vertical entre secciones.
- Algunos layouts se rompían en pantallas pequeñas.

**Qué aprendí**
- El ritmo vertical es clave en el diseño web.
- Pensar mobile-first reduce problemas posteriores.

**Cómo lo resolví**
- Ajusté los márgenes y paddings usando variables CSS.
- Añadí breakpoints progresivos.

---

### Día 3 — Animaciones e interacción
**Qué hice**
- Implementación de animaciones al hacer scroll usando IntersectionObserver.
- Uso de parallax con CSS moderno (`animation-timeline`).
- Micro-interacciones en tarjetas y botones.

**Problemas**
- Las animaciones no se activaban inicialmente.
- Algunos efectos resultaban demasiado bruscos.

**Qué aprendí**
- Es importante separar responsabilidades entre JavaScript (lógica) y CSS (animación).
- Las animaciones sutiles funcionan mejor a nivel profesional.

**Cómo lo resolví**
- Inicialicé correctamente los observers en `main.js`.
- Ajusté distancias y duraciones de las animaciones.

---

### Día 4 — Contenido y refinamiento visual
**Qué hice**
- Desarrollo de secciones específicas: Editorial, Fotografía, Ilustración, Motion Graphics y Branding.
- Implementación de carruseles de imágenes y vídeos.
- Refinamiento de tipografía, color y jerarquía visual.

**Problemas**
- Desalineación entre secciones.
- Ajuste fino del comportamiento de los carruseles.

**Qué aprendí**
- Mantener anchos coherentes entre secciones mejora la consistencia visual.
- Los carruseles en CSS requieren cálculos precisos.

**Cómo lo resolví**
- Unifiqué contenedores y anchos.
- Reescribí las animaciones de los carruseles.

---

### Mejoras en curso
- Optimización de accesibilidad
- Mejora del rendimiento
- Limpieza de código y documentación

---

## Política de uso de IA (obligatoria)
Este proyecto se ha desarrollado con ayuda de asistentes de IA siguiendo un flujo en **dos fases**:

### Fase 1 — Planificación
Antes de implementar cualquier funcionalidad, se solicitó a la IA un plan de desarrollo.

### Fase 2 — Implementación
Solo tras documentar dicho plan se procedió a la implementación del código.

Los planes se documentan en la carpeta `docs/`:
- `docs/plan1.md`
- `docs/plan2.md`
- `docs/plan3.md`

---

## Desarrollo en local

### Opción A — Live Server (recomendado)
1. Abrir el proyecto en VS Code
2. Instalar la extensión **Live Server**
3. Clic derecho en `index.html` → **Open with Live Server**

### Opción B — Apertura directa
Abrir `index.html` en el navegador.

---

## Personalización
- **Contenido:** editar `index.html`
- **Imágenes:** reemplazar archivos en `assets/img/`
- **Colores y tipografía:** modificar variables en `:root`
- **Enlaces:** actualizar links de contacto y redes sociales

---

## Licencia
MIT License — ver archivo `LICENSE`.
