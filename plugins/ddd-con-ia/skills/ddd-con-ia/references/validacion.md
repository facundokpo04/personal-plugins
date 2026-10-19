# Validar código contra el modelo

## Revisar
1. Cada invariante del alcance tiene test con nombre del dominio y el código la cumple.
2. Toda decisión de negocio del código figura en el modelo; si no, "comportamiento no especificado".
3. El código no contradice el modelo.
4. Eventos publicados y consumidos coinciden con el contexto y el context map.
5. No hay llamadas entre contextos fuera del context map.
6. Los nombres coinciden con el glosario.
7. Las reglas viven en el dominio, no en controladores, adaptadores ni base de datos.

Corré los tests. Sin modelo para el alcance: decilo y proponé construirlo antes.

## Informe
```markdown
# Validación: <alcance> (<fecha>)
Invariantes con test: X de Y. Discrepancias: A. No especificado: B.
## Discrepancias
- <modelo> vs <código> → corregir el código o cambiar el modelo (con RFC)
## No especificado
- <qué hace el código> → agregarlo al modelo (con RFC) o eliminarlo
## Eventos, fronteras y lenguaje
```
No modifiques código ni decidas entre código y modelo: presentá ambas opciones.
