# Descubrir: entrevista y Event Storming

## Entrevista
1. Leé visión, glosario, context map, contextos afectados y ADR. Si no está claro el contexto, preguntalo.
2. Lo que se pueda hallar en código o documentos, buscalo; no lo preguntes.
3. Preguntá por rondas: todas las preguntas cuyas dependencias están resueltas, numeradas, cada una con tu respuesta recomendada ("sí" la acepta).
4. Marcá los términos demasiado genéricos para el negocio. Con cada respuesta: contrastá con el glosario, proponé un término preferido para lo vago, probá con un caso límite, cruzá con el código y mostrá contradicciones.
5. Actualizá el glosario apenas se resuelve cada término.
6. Terminá sin ramas abiertas ni supuestos silenciosos: resumí y esperá confirmación. Sin código ni RFC antes.

## Event Storming en texto
Salida en `docs/event-storming/<fecha>.md`: eventos, fuera del relato principal, políticas, dudas, contextos candidatos y granularidad.
1. **Eventos** en pasado y en orden. Luego preguntá por casos límite, fallas, cancelaciones, tareas operativas y hechos técnicos que afectan al negocio.
2. **Comandos y actores** de cada evento.
3. **Agregados** que reciben los comandos y reglas que protegen. Siempre borrador.
4. **Políticas**: cuando X, entonces Y.
5. **Dudas** para el experto.
6. **Contextos candidatos**: una palabra con otro significado marca otro contexto. Revisá si unir (cambian juntos, mismo lenguaje) o partir.

## ADR
Solo si la decisión es difícil de revertir, sorprendente sin contexto y fruto de un compromiso real. Incluye "no" explícitos y alternativas rechazadas no obvias.
