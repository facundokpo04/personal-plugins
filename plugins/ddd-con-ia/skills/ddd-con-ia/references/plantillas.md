# Plantillas

Lenguaje natural, sin detalles técnicos. Crear cada archivo cuando haya algo que escribir.

## CLAUDE.md
```markdown
# Dominio
<qué hace el sistema, una frase>
- Fuente de verdad: docs/. Leer docs/vision.md primero.
- Sin RFC aprobado en docs/rfc/ no se codifica.
- Si código y modelo discrepan, informar.
- Si cambia una regla, término o frontera, actualizar docs/ en el mismo cambio.
- Un contexto por vez; tests de invariantes primero.
```

## docs/vision.md
```markdown
# <Proyecto>
## De qué trata
## Quiénes lo usan
- <Rol>: <qué hace>
## Contextos
- <Contexto>: <responsabilidad> (contextos/<nombre>.md)
## Estado
```

## docs/glosario.md
```markdown
**<Término>**: <qué es, 1-2 frases>. Contexto: <contexto>. No usar: <sinónimos>.
```

## docs/context-map.md
```markdown
| Origen | Destino | Integración | Evento o contrato |
| --- | --- | --- | --- |
```

## docs/contextos/<nombre>.md
```markdown
# <Contexto>
Estado: borrador | validado por <experto> | implementado
## Responsabilidad
## Agregados
### <Agregado>
- Invariantes:
- Comandos:
- Eventos que publica:
## Eventos que consume
## Casos de uso
## Tarjetas CRC
Clase / Responsabilidades / Colaboradores
## Preguntas abiertas
```

## docs/rfc/NNN-titulo.md
Cambio chico: secciones 1 a 4.
```markdown
# RFC NNN: <título>
Estado: borrador | en revisión | aprobado | implementado | rechazado
## 1. Qué se quiere y por qué
## 2. Qué parte del dominio toca
| Elemento (agregado, invariante, evento, término) | Contexto | nuevo / modificado / eliminado | Documento |
## 3. Cómo queda el modelo
## 4. Cómo se valida
- Invariantes con test (nombre en lenguaje del dominio):
- Lo que confirma el experto y quién: <situación concreta del negocio que debe comportarse así>
- Lo que revisa `/ddd-validar`: <contextos, eventos y términos del alcance>
## 5. Alternativas
## 6. Riesgos
## 7. Plan por etapas
## 8. Preguntas abiertas
```
La sección 4 se acuerda con el experto antes de aprobar; es el cierre del RFC: se cumple cuando el experto confirma y `/ddd-validar` no marca discrepancias.

## docs/adr/NNNN-titulo.md
1 a 3 párrafos: contexto, decisión y por qué. Opcional: alternativas, consecuencias.
