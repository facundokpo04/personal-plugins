# ddd-con-ia

Skill y comandos para aplicar Domain-Driven Design con IA. El modelo del dominio, escrito en lenguaje natural, manda; el código se valida contra él.

## Ciclo de un cambio

Entrevista → RFC → aprobación → actualizar el modelo → implementar (tests de invariantes primero) → validar contra el modelo.

Solo los cambios que tocan el negocio pasan por RFC; el resto sigue su flujo habitual. Un ADR se escribe únicamente si la decisión es difícil de revertir, sorprendente sin contexto y fruto de un compromiso real.

## Comandos

| Comando | Para qué |
| --- | --- |
| `/ddd-init` | Prepara la carpeta del modelo (`docs/`, o `docs/ddd/` si ya hay documentos) |
| `/ddd-descubrir` | Entrevista y Event Storming en texto; glosario, context map y contextos |
| `/ddd-rfc <cambio>` | Entrevista y RFC de un cambio, antes de tocar código |
| `/ddd-validar` | Chequea que código y tests respeten el modelo |

No asume lenguaje ni framework.

## Referencias

- Evans, E. *Domain-Driven Design: Tackling Complexity in the Heart of Software*. Addison-Wesley, 2003. Lenguaje ubicuo, bounded contexts, agregados, context map.
- Brandolini, A. *Introducing EventStorming*. Leanpub. Base del Event Storming en texto.
- Beck, K. y Cunningham, W. "A Laboratory for Teaching Object-Oriented Thinking". OOPSLA, 1989. Tarjetas CRC.
- Nygard, M. "Documenting Architecture Decisions", 2011. Origen de los ADR.
- Pocock, M. [`mattpocock/skills`](https://github.com/mattpocock/skills): `grill-with-docs`, `grilling` y `domain-modeling`. Entrevista por rondas con respuesta recomendada y las tres condiciones para escribir un ADR.
- Eisenreich, T., Jusic, S. y Wagner, S. "Automating Domain-Driven Design: Experience with a Prompting Framework". [arXiv:2603.26244](https://arxiv.org/abs/2603.26244), 2026. Pasos encadenados de DDD con LLM y dónde falla, de donde salen varios ajustes de la skill.

Las ideas están reescritas con palabras propias; no se copia texto de estas fuentes.
