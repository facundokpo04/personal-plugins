---
name: ddd-con-ia
description: Aplica Domain-Driven Design con IA. El modelo del dominio en lenguaje natural (docs/) es la fuente de verdad; cada cambio pasa por entrevista, RFC aprobado, código y validación contra el modelo. Usala cuando se hable de DDD, lenguaje ubicuo, glosario, bounded contexts, agregados, invariantes, eventos de dominio, Event Storming, RFC o ADR, o para entender un proyecto, planificar un cambio o validar que el código respeta el dominio.
---

# DDD con IA

El modelo en lenguaje natural manda. Sin lenguaje ni framework asumido.

## Reglas

- Si código y modelo discrepan, informalo; no lo resuelvas en silencio.
- El modelo no lleva detalles técnicos (clases, tablas, endpoints).
- Mismos términos del glosario en documentos, código y tests.
- Un contexto por vez; entre contextos solo por lo definido en el context map.
- Las reglas de negocio son invariantes de un agregado, con test.
- Lo vago se pregunta; no completes huecos con conocimiento general. Lo no confirmado se marca "supuesto" y lo abierto va como pregunta al experto. La IA propone, el experto decide.
- Durante el modelado no se pide arquitectura técnica: se decide aparte, con el modelo aprobado.

## Modelo (`docs/`, plantillas en `references/plantillas.md`)

`vision.md` · `glosario.md` · `context-map.md` · `contextos/<nombre>.md` · `rfc/NNN-*.md` · `adr/NNN-*.md`

Si falta contexto, preguntá junto: qué hace, quién lo usa, quién valida.

Si `docs/` ya tiene otros documentos, creá el modelo en `docs/ddd/`; todas las rutas de esta skill son relativas a esa carpeta.

## Construir el modelo base

Un paso por vez, con contexto limpio (solo el material necesario). Cada paso usa `references/descubrir.md`.

1. **Preparar**: acotar el dominio, juntar material, crear `docs/` y `CLAUDE.md`.
2. **Descubrir**: Event Storming en texto. Con código existente, derivar el modelo y marcarlo "a validar".
3. **Lenguaje y contextos**: glosario, context map, visión. Revisar si unir o partir contextos.
4. **Modelar cada contexto**: agregados (borrador), invariantes, comandos, eventos, CRC. Cuestioná los agregados muy grandes o sin invariantes; si el experto los ve mal, redactalos con él.

Al cerrar cada paso: todo término usado está en el glosario y lo nuevo vuelve a los documentos previos.

## Cambio

1. **Entrevistar** (`references/descubrir.md`), proporcional al cambio.
2. **RFC** en `docs/rfc/`: qué se quiere y qué parte del dominio toca.
3. **Corregir hasta aprobar.** Sin código.
4. **Actualizar el modelo.**
5. **Implementar** (`references/implementar.md`): tests de invariantes primero, con nombre en lenguaje del dominio; luego código.
6. **Validar** (`references/validacion.md`).
7. **Cerrar**: modelo, código y tests coinciden; RFC marcado implementado.

Imprevisto: parar y actualizar RFC y modelo.
