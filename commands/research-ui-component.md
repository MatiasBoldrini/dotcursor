# Research de componente UI (internet amplio + sitios sugeridos)

Actuá como si el usuario estuviera **antes de diseñar en código**: hay que **investigar en la web de forma amplia** si ya existe un patrón, componente o referencia sólida acorde al pedido. **No limites** la investigación a una lista cerrada de sitios.

## Componente o idea a cubrir

Usá **el resto del mensaje del usuario** (lo que escriba junto al comando) como descripción del componente, interacción o layout (nombre, referencia, “carousel de sponsors”, “bento con zoom al scroll”, etc.). Si falta detalle, formulá hasta **2 preguntas cortas** y seguí con hipótesis razonables.

## Cómo investigar (orden mental)

1. **Búsqueda abierta en internet**: usá herramientas de búsqueda y navegación (web, documentación, repos, demos). Explorá tantas fuentes útiles como hagan falta: otras UI kits, blogs técnicos, GitHub (`awesome-*`, ejemplos, starters), npm, CodePen / demos, documentación de librerías (p. ej. Motion, Radix), etc.

2. **Sitios sugeridos (no obligatorios)**: como **primeras paradas habituales** cuando el pedido encaja con componentes React + Tailwind listos para copiar o adaptar, **sugerí** revisar si aportan algo (búsqueda interna o términos en Google). Si no hay nada útil o el tipo de componente no existe ahí, **no pasa nada**: no inventes encaje; seguí con otras fuentes.
   - **Aceternity UI** — https://ui.aceternity.com/components  
   - **React Bits** — https://reactbits.dev  
   - **Magic UI** — https://magicui.design/docs/components  
   - **21st.dev** — https://21st.dev  
   - **shadcn/ui** y ecosistema de bloques / registries (p. ej. addons tipo `@magicui/*`) cuando encaje con el flujo “snippet de componente”

3. **Criterio**: priorizá **calidad y pertinencia** al pedido. Vale más un buen match en un repo random que forzar algo mediocre solo porque estaba en un sitio sugerido.

En sitios con muchos componentes: buscá con sinónimos en **inglés y español** si ayuda; no abras más de **2–4 candidatos** por fuente salvo que el pedido sea muy ambiguo.

## Qué entregar (salida obligatoria)

1. **Resumen del pedido** en una frase.
2. **Tabla o lista** de opciones candidatas (de cualquier fuente) con:
   - Nombre del componente / patrón  
   - Fuente y URL concreta  
   - Qué resuelve y qué **no** cubre  
   - Dependencias probables (p. ej. `motion`, GSAP, solo CSS)
3. **Recomendación** de 1 opción principal + 1 alternativa, justificando encaje con un sitio **profesional e interactivo** (p. ej. React + Tailwind).
4. **Riesgos**: accesibilidad, rendimiento, mobile vs desktop, mantenimiento (copiar vs paquete).
5. **Siguiente paso**: si conviene adaptar desde snippet, enlazá la fuente y listá archivos del proyecto que probablemente toque crear o tocar **sin implementar aún** a menos que el usuario lo pida.

Podés mencionar de paso si **miraste** alguno de los sitios sugeridos y no hubo match, **solo si es útil** para el usuario (no hace falta un informe por cada sitio).

## Cierre del flujo (obligatorio, al final)

Hacé esto **después** de entregar los puntos 1–5 anteriores, en este orden:

### 1) Abrir ejemplos en el navegador

- Usá la herramienta **AskQuestion** del agente (preguntas con opciones en el chat; en la API del agente suele llamarse `AskQuestion`) para preguntarle al usuario si quiere abrir en el navegador **todas las URLs concretas** de los ejemplos que listaste en la tabla de candidatas (demos, docs con preview, páginas del componente — lo que se pueda “ver en vivo”; no hace falta distinguir si es “imagen” o página).
- Opciones sugeridas: p. ej. **Sí, abrir todas** / **No**.
- Si el usuario elige **sí** (o equivalente): abrí **cada una** de esas URLs en el navegador predeterminado.
  - En **macOS**: ejecutá en terminal `open` con cada URL, por ejemplo `open "https://..." "https://..."` (varias en una sola llamada) o una por línea. En Windows sería `start`; en Linux `xdg-open` — adaptá solo si el entorno no es macOS.
- Si no hay URLs válidas para abrir (solo texto sin links), aclarálo y no ejecutes `open`.

### 2) Qué implementar (siempre)

- **Independientemente** de si abrió enlaces o eligió “No”, el siguiente paso es obligatorio: volvé a usar **AskQuestion** para preguntar **qué elemento quiere implementar** a continuación.
- Construí las opciones a partir de los **candidatos** que ya listaste (nombre corto + fuente, una opción por candidato relevante) y agregá siempre una opción del estilo **Otro — describir otro componente o variante en el chat**.
- No implementes código en este paso salvo que el usuario lo pida después; solo dejá elegido el camino.

### 3) Aprender fuentes nuevas (auto-actualización)

- Después de que el usuario elija qué implementar, compará la URL de la opción elegida contra los **sitios sugeridos** de la sección "Sitios sugeridos (no obligatorios)" de este mismo archivo (`~/.cursor/commands/research-ui-component.md`).
- Si la URL elegida **no pertenece** a ninguno de los dominios ya listados como sugeridos, **agregala** al final de la lista de sitios sugeridos usando el mismo formato (`- **Nombre del sitio** — URL base`).
- Usá como nombre el nombre del sitio/librería tal como aparece en su página, y como URL la raíz de su sección de componentes (no la URL específica del componente individual).
- No pidas confirmación: hacé la edición directamente en el archivo del slash command. Esto permite que futuras invocaciones incluyan esa fuente entre las primeras paradas habituales.
- Si la URL elegida **sí** pertenece a un sitio ya listado, no hagas nada.

## Restricciones

- No inventes URLs; si no encontrás match en una fuente, decilo.
- Preferí fuentes **autoritativas** (docs oficiales, repo del autor, demo del maintainer) antes que rewrites dudosos.
- Respondé en **español** salvo nombres técnicos en inglés.
