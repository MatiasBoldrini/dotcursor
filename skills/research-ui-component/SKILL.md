---
name: research-ui-component
description: >-
  Researches the web for an existing UI pattern or component before writing
  code. Checks curated sources (Aceternity UI, React Bits, Magic UI, 21st.dev,
  shadcn/ui) and other relevant references, returns candidates with a
  recommendation, opens the demos, and asks which one to implement. Use when
  the user asks to research a UI component, find a component reference, or
  invokes /research-ui-component.
disable-model-invocation: true
---

# Research de componente UI

Investigá en la web si ya existe un patrón, componente o referencia sólida para lo que pide el usuario. No limites la búsqueda a una lista cerrada de sitios.

## Componente

Usá el resto del mensaje del usuario como descripción. Si falta detalle, hacé hasta 2 preguntas cortas y seguí con hipótesis razonables.

## Investigación

1. **Búsqueda abierta**: web, docs, repos, demos, npm, CodePen, librerías (Motion, Radix, etc.).

2. **Sitios sugeridos** (primeras paradas cuando encaje con React + Tailwind):
   - **Aceternity UI** — https://ui.aceternity.com/components
   - **React Bits** — https://reactbits.dev
   - **Magic UI** — https://magicui.design/docs/components
   - **21st.dev** — https://21st.dev
   - **shadcn/ui** y registries (`@magicui/*`, etc.)

   Si no hay match, seguí con otras fuentes.

3. **Criterio**: calidad y pertinencia. Un buen match en un repo random vale más que algo forzado de un sitio sugerido.

Buscá con sinónimos en inglés y español; no abras más de 2-4 candidatos por fuente.

## Salida obligatoria

1. **Resumen** del pedido en una frase.
2. **Lista de candidatos** con: nombre, fuente+URL, qué resuelve y qué no, dependencias.
3. **Recomendación**: 1 principal + 1 alternativa, justificando encaje.
4. **Riesgos**: accesibilidad, rendimiento, mobile, mantenimiento.
5. **Siguiente paso**: fuente y archivos que tocaría, sin implementar aún.

## Cierre del flujo

Orden obligatorio: primero abrir todas las URLs; después (y solo después) la pregunta de implementación.

### 1) Abrir referencias en el navegador (automático, sin preguntar)

En la **misma respuesta** donde entregás la investigación, **antes** de cualquier **AskQuestion**, ejecutá en terminal **una sola vez** el comando con **todas** las URLs de la lista de candidatos (y la de la recomendación principal si no estaba ya incluida). No pidas confirmación.

- **macOS:** `open "URL1" "URL2" ...`
- **Linux:** `xdg-open URL` por URL en secuencia, o el equivalente que use el entorno.
- **Windows:** `start "" "URL"` por URL, o el equivalente.

Si no hay URLs válidas que abrir (ningún candidato con enlace), omití este paso y aclaralo en una frase.

### 2) Qué implementar

Recién después del paso 1, usá **AskQuestion** con los candidatos como opciones + **Otro**. No implementes código salvo que lo pida.

### 3) Aprender fuentes nuevas

Si la URL elegida no pertenece a ningún sitio sugerido de este archivo, agregala al final de la lista **Sitios sugeridos** de este mismo `SKILL.md` con formato `- **Nombre** — URL base`. Sin pedir confirmación.

## Restricciones

- No inventes URLs.
- Preferí fuentes autoritativas.
- Respondé en español salvo nombres técnicos.
