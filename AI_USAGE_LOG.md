# AI Usage Log — ADA-05

Este registro resume las interacciones de IA que influyen en el producto. Se ampliará durante las etapas siguientes.

## Entrada 01 — Requisitos (fase 1)

- **Interacción:** El estudiante pidió iniciar la fase 1 después de revisar el enunciado de ADA-05.
- **Propuesta de la IA:** Redactar la historia de usuario, seis requisitos funcionales, tres no funcionales, restricciones, supuestos y dos preguntas abiertas. Se propuso una CLI local con datos en memoria como alcance inicial.
- **Decisión del estudiante:** Primero solicitó un borrador y después pidió completar todo el ADA, delegando la elección de las opciones planteadas. No consta una revisión personal de cada requisito.
- **Cambio en el producto:** Se creó `REQUIREMENTS.md`; Q-01, Q-02 y A-01 quedaron definidos para esta entrega.
- **Seguimiento:** El estudiante debe revisar personalmente que este alcance representa su intención antes de entregar.

## Entrada 02 — Especificación y planificación (fases 2 a 6)

- **Interacción:** La IA convirtió los requisitos ya definidos en criterios de aceptación, reglas de búsqueda, arquitectura y seis tareas verificables.
- **Propuesta de la IA:** Usar una función pura con clientes inyectados, `casefold()` para comparar y una CLI que traduzca los errores a códigos de salida.
- **Decisión del estudiante:** Solicitó completar el ADA entero y delegó estas decisiones técnicas. No consta revisión personal detallada de los documentos.
- **Cambio en el producto:** Se añadieron `SPEC.md`, `ARCHITECTURE.md`, `TASKS.md`, `AGENTS.md`, `README.md` y la estructura inicial, antes de implementar la feature.
- **Seguimiento:** Validar que las pruebas y el código respeten los criterios de aceptación sin alterar los requisitos para acomodar la implementación.

## Entrada 03 — Implementación (T-01 a T-04)

- **Interacción:** Se pidió a Antigravity CLI (`agy`) realizar T-01 después del commit base. Los primeros intentos fallaron por permisos y el intento en sandbox agotó el tiempo de espera. Un borrador tardío de `README.md` apareció en el árbol, sin reporte completo. Codex continuó T-01 y realizó T-02 a T-04.
- **Propuesta de la IA:** Paquete Python instalable, datos ficticios, modelo inmutable, búsqueda pura y CLI con `argparse`.
- **Decisión del estudiante:** La instrucción de completar todo el ADA permitió continuar. No consta una selección manual entre alternativas técnicas ni revisión personal del código.
- **Cambio en el producto:** Se añadieron `pyproject.toml` y `src/customer_search/`; se corrigió el README para que sus comandos coincidan con el paquete final.
- **Seguimiento:** Verificar comportamiento con pruebas antes de marcar criterios como cumplidos.

## Entrada 04 — Pruebas y revisión (T-05 y T-06)

- **Interacción:** Codex comparó las reglas de `SPEC.md` con la implementación y preparó pruebas para búsqueda, validación y CLI.
- **Propuesta de la IA:** Pruebas de fragmentos, mayúsculas, orden, ausencia de duplicados, mensajes y códigos de salida; tabla de trazabilidad por requisito.
- **Decisión del estudiante:** No consta revisión personal de las pruebas. La aceptación académica de estas decisiones queda pendiente.
- **Cambio en el producto:** Se añadieron `tests/`, `docs/traceability.md`, `results/agent-report.md`, `docs/reflection.md` y documentación final. `pytest -v` aprobó 15 pruebas en la primera ejecución completa.
- **Seguimiento:** El estudiante debe ejecutar o revisar las pruebas, explicar las decisiones y actualizar el apartado de revisión humana con hallazgos propios antes de entregar.
