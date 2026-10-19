# Implementar sobre el modelo

- Un contexto y una etapa del RFC por vez.
- El dominio no depende de infraestructura (base de datos, web, mensajería); los adaptadores dependen del dominio.
- Las reglas de negocio viven en el agregado que protege la invariante, no en controladores ni servicios de aplicación.
- Un agregado se guarda y se carga completo; se referencia a otros agregados por identidad.
- Cada caso de uso orquesta: carga, ejecuta el comando, guarda y publica eventos.
- Los errores de negocio son del dominio y llevan nombre del glosario.
- Nada de capas, factories o abstracciones que el RFC no pida.
