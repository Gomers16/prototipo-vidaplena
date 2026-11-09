# VidaPlena – Prototipo navegable

Prototipo de una página de recomendaciones saludables, desarrollado para la Actividad de Construcción Aplicada (ACA) de Ingeniería Web, CUN Digital.

**Prototipo en línea:** https://gomers16.github.io/prototipo-vidaplena/

## Qué es

Un único archivo `index.html` (HTML, CSS y JavaScript, sin librerías externas) que simula la experiencia de una página con recomendaciones de cuatro temas: alimentación, actividad física, descanso y bienestar. No tiene servidor ni base de datos: los datos de demostración (12 recomendaciones) están dentro del archivo y las preferencias de la persona se guardan solo en su navegador (`localStorage`).

## Pantallas

1. Inicio (categorías, recomendaciones populares o personalizadas)
2. Explorar (búsqueda, filtros por tema, nivel, tiempo y objetivo, orden)
3. Detalle de una recomendación
4. Ingresar / Registrarse
5. Perfil de salud
6. Mi espacio (favoritos y seguimiento semanal de hábitos)

## Cómo probarlo

1. Abrir el enlace del prototipo.
2. Buscar una recomendación (por ejemplo, «respiracion»; la búsqueda ignora tildes) o usar los filtros en Explorar.
3. Abrir el detalle y pulsar el corazón para guardarla. Si no hay sesión, se pide ingresar y, al terminar, la acción pendiente se completa sola.
4. Completar el perfil de salud y volver al inicio: aparece «Recomendado para ti» según el objetivo declarado.
5. En «Mi espacio», marcar los días de cumplimiento de un hábito.

## Requerimientos que cubre

| Requerimiento | Dónde se ve |
|---|---|
| RF1 Usuarios y perfil de salud | Pantallas de acceso y perfil |
| RF2 Contenidos saludables | Tarjetas con la misma plantilla y pantalla de detalle |
| RF3 Búsqueda y filtrado | Buscador del encabezado y panel de filtros en Explorar |
| RF4 Personalización | Sección «Recomendado para ti» (coincide el objetivo; si el nivel de actividad es bajo, solo nivel fácil) |
| RF5 Favoritos y hábitos | «Mi espacio» |
| RNF Rendimiento, escalabilidad, seguridad, UX, compatibilidad | Ver el informe en PDF (secciones de análisis) |

## Decisiones de diseño

- Estilo sobrio de referencia comercial (fondo claro, tipografía condensada en mayúsculas para títulos, mucho espacio en blanco). Referencia visual: sitio de Nike Colombia.
- Tipografías: Barlow Condensed y Barlow, incluidas dentro del archivo.
- Tema claro y oscuro según la preferencia del sistema.
- Diseño adaptable a móvil (puntos de quiebre en 1000, 700 y 420 px).

## Proceso y por qué

1. **Análisis de requerimientos.** Se identificaron tres perfiles de uso (visitante que busca ideas rápidas, persona con un objetivo concreto, persona constante que quiere registrar su avance) para decidir qué debía poder hacerse sin cuenta y qué no.
2. **Mapa de pantallas.** Seis pantallas conectadas por un menú fijo. La cuenta se pide solo cuando hace falta (guardar un favorito o abrir «Mi espacio»), para no frenar a quien solo explora; al registrarse, la acción pendiente se completa sola.
3. **Wireframe.** En escala de grises, con recuadros cruzados para imágenes y marcas numeradas, para decidir estructura y jerarquía antes de pensar en el color. Se comprobó que cada requerimiento funcional tuviera un lugar en alguna pantalla.
4. **Mockup.** Estilo sobrio y de alto contraste: fondo claro, un solo color de acción, títulos condensados en mayúsculas y bloques grises en lugar de fotos, para mantener la página ligera. El contraste de los textos y de los bordes de los formularios se calculó con las pautas WCAG 2.2.
5. **Prototipo.** Se programó (en lugar de enlazar imágenes) para que la búsqueda, los filtros, los favoritos y los hábitos funcionen de verdad y se pueda comprobar el flujo completo.
6. **Revisión.** Se consultó la documentación de MDN sobre accesibilidad; de ahí se retiró `aria-pressed` de los botones cuya etiqueta cambia y se mantuvo `aria-checked` en las casillas del seguimiento semanal.

## Limitaciones

- No hay servidor: no se almacenan contraseñas ni datos reales.
- No se hicieron pruebas con usuarios reales ni mediciones formales de rendimiento.
- Se revisó en un navegador basado en Chromium; no se probó en dispositivos físicos.

Autor: Diego Mauricio Gómez Rodríguez · Docente: Sergio Alexander Mora Novoa · Ingeniería Web, ficha 55564.
