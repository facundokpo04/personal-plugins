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
