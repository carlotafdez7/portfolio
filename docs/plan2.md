# Plan 2 — Responsive mobile-first + carruseles (imágenes/vídeo) + accesibilidad básica

## Contexto (dónde estaba el proyecto)

En esta segunda fase el proyecto ya tenía:

- Secciones principales montadas: **Hero / About / Work (tarjetas) / Secciones de detalle (Editorial, Photography, Illustration, Motion, Branding) / Contact / Footer**
- Estructura CSS modular con imports en `assets/css/index.css` (base / layout / components / secciones)
- Efectos visuales (glassmorphism, covers, carruseles CSS)
- Animaciones on-scroll ya integradas por la plantilla (IntersectionObserver + clases)

El problema real apareció al probar en móvil:

- Algunas secciones generaban **scroll horizontal**
- Cards horizontales quedaban raras en pantallas pequeñas
- **Imágenes y vídeos** dentro de tarjetas no se ajustaban bien (recorte, alturas descompensadas)
- Había dudas sobre “dónde pegar qué” en una arquitectura CSS modular
- Quería ser mobile-first pero **sin cambiar el diseño desktop** que ya me gustaba

---

## Objetivo de esta fase

1. Hacer que la web sea **mobile-first responsive** (sin romper desktop)
2. Normalizar el comportamiento de **media** (imágenes, carruseles, vídeo) dentro de cards
3. Ordenar la lógica de media queries: **base para móvil + mejoras progresivas**
4. Reforzar accesibilidad básica (foco, navegación por teclado, reduced motion, estructura semántica)

---

## Fase 1 — Planificación (uso de IA)

### Prompt enviado a la IA

> Mi web se ve bien en desktop pero en móvil se rompe: cards y carruseles se desajustan y hay scroll horizontal.  
> Quiero un plan mobile-first que no cambie el diseño de escritorio.  
>  
> Mi estructura CSS está separada en base/layout/components y por secciones (editorial, photography, etc.).  
> Quiero que me digas:
> - Qué reglas van en cada archivo
> - Qué media queries añadir y dónde
> - Cómo ajustar carruseles e imágenes/vídeo para que encajen sin recortes raros
> - Qué revisar de accesibilidad (foco, alt, teclado, reduced motion)
>  
> Explícamelo como alumna: qué cambia, por qué, y cómo comprobarlo.

---

### Respuesta de la IA (plan propuesto)

La IA propuso un método de “estabilización” por capas, priorizando móvil:

1. **Primero eliminar scroll horizontal**
   - Revisar widths con `vw`, `100vw` dentro de wrappers
   - Asegurar `img, video { max-width: 100% }`
   - Usar `overflow-x: hidden` con cuidado solo si la causa está identificada

2. **Mobile-first: layout base en 1 columna**
   - Cards horizontales en móvil → pasar a `grid-template-columns: 1fr`
   - Luego, en breakpoints, reactivar layout horizontal

3. **Normalizar media dentro de tarjetas**
   - Un patrón para imágenes y vídeos:
     - altura consistente en móvil
     - `object-fit` según necesidad (cover vs contain)
   - Para vídeos: añadir `controls` si quiero “ver entero” sin recortar o usar `object-fit: contain`

4. **Carruseles CSS**
   - Hacer el track proporcional al número de imágenes (5, 6, 7, 10…)
   - Ajustar keyframes para que el slide sea predecible en móvil
   - Pausar en hover solo desktop; en móvil no existe hover

5. **Accesibilidad**
   - Focus visible (`:focus-visible`)
   - Alt text significativo
   - `prefers-reduced-motion`
   - Semántica: un `h1`, secciones con `id`, `nav` correcto
   - Tap targets grandes en móvil

---

## Fase 2 — Implementación real

### 1 Entender y fijar la estructura HTML que tenía pensada

#### About (estructura que seguí)
- Un contenedor general `.about-grid`
- Dentro:
  - `.about-intro` (fila superior): **texto + foto**
  - `.skills-grid` (fila inferior): **barras de habilidades**

**Por qué esta estructura:**  
Me permite alinear el ancho de “arriba” (texto+foto) con el ancho de “abajo” (skills) sin crear contenedores distintos.

---

#### Work / Projects (estructura que seguí)
- `#projects` muestra tarjetas “categoría” (Editorial / Photography / etc.)
- Cada tarjeta enlaza a su sección de detalle con `href="#editorial"` etc.
- Cada sección de detalle tiene:
  - un **cover** (título + subtítulo)
  - una o varias **cards horizontales** con:
    - texto a la izquierda (columna estrecha)
    - carrusel / media a la derecha (columna ancha)

**Por qué así:**  
Me crea una navegación clara: el usuario ve categorías → entra en una sección → consume el proyecto de forma editorial.

---

### 2 Mobile-first sin tocar desktop: estrategia de media queries

Mi regla de oro aquí fue:

- **Base (sin media query) = móvil**
- Breakpoints = mejoras progresivas (tablet / desktop)

Lo que implementé como criterio:

- En móvil:
  - cards horizontales → 1 columna
  - alturas más bajas de carousels/vídeos
  - tipografía ligeramente más compacta
- En desktop:
  - vuelven las 2 columnas (texto / media)
  - carousels más altos
  - gaps mayores

---

### 3 Normalizar imágenes y vídeos dentro de cards

Este fue el punto que más me costó porque “funciona” en desktop pero en móvil:

- los vídeos se cortaban raro
- las imágenes se veían estiradas o fuera de lugar
- parecía que “no cargaban” pero era más bien un problema de proporción

#### Decisiones que tomé (razonadas)

- Para **fotografía** y carousels: `object-fit: cover` suele verse más “pro”, aunque recorte un poco.
- Para **vídeo** cuando quiero “ver entero” (sin recorte): `object-fit: contain` + fondo para que no se vea feo el espacio sobrante.

Esto es importante:  
`cover` = estética / recorta  
`contain` = fidelidad / no recorta

---

### 4 Carruseles CSS: hacerlos consistentes por cantidad de imágenes

Yo estaba usando carruseles de 5 y de 10 imágenes.

Lo que aprendí:
- El `width` del track debe ser proporcional:
  - 5 imágenes → `width: 500%`, cada slide `20%`
  - 6 imágenes → `width: 600%`, cada slide `16.666%`
  - 7 imágenes → `width: 700%`, cada slide `14.285%`
  - 10 imágenes → `width: 1000%`, cada slide `10%`

Si esto no cuadra, el carrusel “se va a lo loco”.

Además:
- `pause on hover` solo tiene sentido en escritorio.
- En móvil, es mejor que el movimiento sea más lento o que el componente sea más bajo.

---

### 5 Accesibilidad: checklist básico aplicado a mi caso

Cosas que revisé o dejé preparadas:

- **Focus visible** en links y botones:
  - `:focus-visible { outline: ... }`
- Navegación con teclado:
  - los links y botones funcionan sin ratón
- `prefers-reduced-motion`:
  - si el usuario lo pide, desactivar animaciones y dejar visible el contenido
- Alt text:
  - no dejar `alt=""` salvo imágenes decorativas
- Jerarquía de headings:
  - un solo `<h1>` en hero
  - covers como `<h2>` de sección
  - títulos de proyecto como `<h3>`

---

## Qué problemas aparecieron (y cómo los resolví)

### Problema 1: “No sé dónde pegar el CSS”
Me pasaba porque en `index.css` solo veía imports.

**Cómo lo resolví mentalmente:**
- `base.css` = tokens, reset, elementos globales (body, img, a)
- `layout.css` = container, grid helpers, secciones
- `components.css` = cards, botones, nav, carruseles reutilizables
- `sections/*.css` = reglas específicas de editorial/photography/etc.

Así evitaba duplicar cosas y saber dónde buscar después.

---

### Problema 2: Desktop bien, móvil fatal
Lo típico: el CSS “nació” en desktop.

**Cómo lo afronté:**
- En móvil, forzar **1 columna** en cards horizontales
- Reintroducir 2 columnas SOLO a partir de `min-width: 900px` aprox.

---

### Problema 3: Media (img/video) “no encaja”
No era un bug, era “falta de reglas claras”.

**Solución mental:**
- Todo media necesita:
  - `width: 100%`
  - una altura definida (aunque sea por `aspect-ratio` o `height`)
  - `object-fit` decidido con intención

---


## Notas de implementación (lo que efectivamente toqué)

- Añadí media queries para que cards horizontales pasen a 1 columna en móvil
- Ajusté alturas de carruseles en móvil
- Revisé `object-fit` para que vídeos se vean enteros cuando lo necesito
- Consolidé reglas para evitar scroll horizontal
- Reforcé el foco visible y la lógica de reduced motion

---

## Mini checklist de prueba (cómo comprobé que funcionaba)

- Móvil 320px: no hay scroll horizontal
- Móvil 480px: texto legible + carousels no se salen
- Tablet 768px: layout mejora sin romper
- Desktop 1024px+: se mantiene tal cual lo tenía
- Teclado: tab funciona y se ve el foco
- Reduced motion: el contenido sigue apareciendo sin depender de animaciones

