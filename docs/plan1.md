# Plan 1 — Personalización del sistema de diseño (CSS variables) y estructura CSS

## Contexto de la tarea

Partí de una plantilla/estructura base proporcionada por el profesor (HTML + CSS + JS ya organizados).  
Mi objetivo NO era “inventar un proyecto desde cero”, sino **entender la estructura existente** y empezar a personalizar el portfolio de forma consciente:

- Cambiar paleta de color y aspecto visual sin romper el layout
- Entender para qué sirve cada bloque de CSS (variables, reset, layout, componentes)
- Evitar “parches” y aprender a tocar primero lo importante: **design tokens (custom properties)**
- Mantener el comportamiento del sitio y la consistencia visual entre secciones

La prioridad fue **hacer cambios con intención**, no solo “que se vea diferente”.

---

## Fase 1 — Planificación (uso de IA)

### Prompt enviado a la IA

> Tengo un portfolio con una estructura base del profesor.  
> Ya existen archivos CSS separados y variables en :root.  
> Quiero personalizarlo bien (colores, tipografía, radios, sombras, spacing) sin romper nada.  
>  
> Necesito un plan paso a paso para:
> - Entender qué hace cada parte del CSS
> - Decidir qué variables cambiar primero
> - Evitar tocar cosas “de layout” cuando solo quiero cambiar estética
> - Mantener consistencia en todo el sitio
>  
> Explícamelo como si fuese una alumna, con razonamiento, no solo “copia y pega”.

---

### Respuesta de la IA (plan propuesto)

La IA propuso un enfoque “de fuera hacia dentro”, para no romper el proyecto:

1. **Leer el CSS como un sistema**
   - Identificar dónde están las variables (tokens)
   - Distinguir: base/reset vs layout vs componentes vs secciones

2. **Cambiar primero variables globales**
   - Colores: `--color-bg`, `--color-bg-alt`, `--color-text`, `--color-accent`
   - Tipografía: `--font-sans`, escalas con `--text-*`
   - Espaciado: `--space-*`
   - Superficies: `--radius-*`, `--shadow-*`

3. **Evitar tocar reglas de layout al principio**
   - No cambiar grids/columns hasta tener definida la estética
   - Mantener estructura para poder comparar “antes/después”

4. **Probar cambios de forma controlada**
   - Cambiar 1–2 variables
   - Revisar todo el sitio
   - Documentar qué cambió y qué efecto tuvo

5. **Personalización por capas**
   - Capa 1: tokens (variables)
   - Capa 2: componentes (cards, botones, links)
   - Capa 3: secciones (covers, proyectos, carruseles)

6. **Refuerzo de comprensión**
   - Entender qué hace cada token para que las decisiones sean intencionales

---

## Fase 2 — Implementación real

### Qué se implementó finalmente

En esta fase me centré en lo más importante: **tocar variables antes que “CSS suelto”**.

#### 1) Paleta y contraste (custom properties)
Se ajustaron variables en `:root` para que el portfolio reflejara un tono más personal:

- `--color-bg` y `--color-bg-alt` para definir el fondo general y las superficies
- `--color-text` y `--color-text-muted` para jerarquía de lectura
- `--color-accent` y `--color-accent-hover` para CTA, links y estados activos

**Qué aprendí aquí:**  
Si cambio `--color-bg-alt`, no estoy “pintando una sección”: estoy cambiando **todas las superficies** que usen ese token. Es más limpio y escalable.

---

#### 2) Tipografía: tocar tokens, no cada elemento
En vez de cambiar `font-size` por todo el CSS, mantuve el sistema fluido con `clamp()` y ajusté:

- `--text-base` y `--text-lg` para lectura y jerarquía
- `--font-sans` como stack principal

**Qué aprendí aquí:**  
`clamp()` no es solo “responsive”: es una forma de mantener **consistencia** sin mil media queries.

---

#### 3) Superficies: radios y sombras (consistencia visual)
Se reforzó el estilo de “card” y superficies mediante tokens:

- `--radius-sm`, `--radius-md`, `--radius-lg`
- `--shadow-sm`, `--shadow-md`

**Qué aprendí aquí:**  
Si las cards tienen radios diferentes sin sistema, todo se siente “inestable”.  
Con tokens, puedo decidir un lenguaje visual: suave / duro / editorial / futurista.

---

#### 4) Microinteracciones sin romper layout
En lugar de modificar estructuras, los cambios se enfocaron en “capas seguras”:

- hover en cards (transform + sombra)
- hover de links (color accent)
- ajustes de fondo tipo glassmorphism donde tenía sentido

**Qué aprendí aquí:**  
Para evitar bugs, primero mejoro “sensación” (hover, sombras, blur) y dejo grids/columnas para después.

---

## Guía mental que seguí para razonar cambios (lo importante del plan)

### Cómo decidía “dónde tocar” el CSS

1. **¿Esto es global?**
   - Sí → `:root` (tokens)
   - No → componente o sección

2. **¿Esto es estética o estructura?**
   - Estética → color, tipografía, sombras, radios
   - Estructura → grid, widths, columnas, breakpoints

3. **¿Estoy repitiendo valores?**
   - Si repetía un color 3 veces → lo convertía en variable
   - Si un padding se repetía → revisaba el scale de `--space-*`

---

## Qué NO hice a propósito (y por qué)

- No cambié el JavaScript base del profesor porque ya venía integrado y funcionando
- No rehice grids grandes en la misma fase porque todavía estaba definiendo la identidad visual
- No intenté “solucionar todo de golpe” porque eso me llevaba a parches y confusión

---

## Reflexión personal

Esta fase me sirvió para dejar de “tocar CSS por intuición” y empezar a entender el proyecto como un sistema.

Lo más útil fue separar mentalmente:
- **Tokens (variables) = decisiones**
- **Componentes = implementación**
- **Secciones = composición**

Al final, pude empezar a personalizar con más seguridad, porque ya no estaba editando “a ciegas”, sino entendiendo qué efecto tenía cada cambio.

---



