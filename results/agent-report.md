# Agent Report

## Agent / Version

- Codex (GPT-6 en esta sesión): implementación, pruebas y verificación.
- Antigravity CLI `agy` (servidor 1.2.10 mostrado al iniciar): se invocó para T-01.

## Initial Context

Directorio vacío, sin repositorio Git. El enunciado exigía documentar requisitos, especificación, arquitectura y tareas antes de implementar. Se adoptó una CLI con datos ficticios en memoria.

## Task Sequence

### T-01 Project setup

- What the agent did: Se invocó `agy` para T-01. Los primeros intentos fallaron por permisos; el intento en su sandbox agotó el tiempo de espera, pero dejó un borrador de `README.md` en el árbol. Codex integró y corrigió ese borrador, y completó `pyproject.toml` y los datos de ejemplo.
- Human review: El estudiante solicitó completar el ADA; no consta una revisión personal de este paso.
- Tests: Instalación editable y CLI verificadas en un entorno virtual con Python 3.12; `pytest -v` aprobó 15 pruebas.

### T-02 Domain model

- What the agent did: Codex creó `Customer` inmutable y registros con ID, nombre y correo.
- Human review: Pendiente de revisión personal del estudiante.
- Tests: `test_model_has_required_fields` pasó.

### T-03 Search logic

- What the agent did: Codex creó búsqueda por subcadena en nombre o correo, con `casefold()` y orden de entrada.
- Human review: Pendiente de revisión personal del estudiante.
- Tests: Pruebas de fragmentos, mayúsculas, orden y no duplicación pasaron.

### T-04 Validation and errors

- What the agent did: Codex añadió CLI, mensajes y códigos de salida.
- Human review: Pendiente de revisión personal del estudiante.
- Tests: Pruebas de entradas inválidas y salida pasaron.

### T-05 Tests

- What the agent did: Codex añadió 15 casos automatizados de comportamiento.
- Human review: Pendiente de revisión personal del estudiante.
- Tests: `pytest -v`: 15 aprobadas, 0 fallidas.

### T-06 Documentation

- What the agent did: Codex completó README, trazabilidad, log de IA, este informe y reflexión.
- Human review: Pendiente de revisión personal del estudiante.
- Tests: Revisión de documentos y comandos finales.

## Problems Encountered

`agy` no completó T-01 de forma verificable dentro del tiempo disponible. En aislamiento no pudo abrir su registro ni un puerto local; en modo no interactivo sin sandbox se denegó un comando; en su sandbox agotó tres minutos. Apareció un borrador tardío de README, pero no un reporte de ejecución. Por ello no se atribuyen a `agy` las tareas T-02 a T-06.

## Human Interventions

El estudiante indicó primero avanzar por fases y luego solicitó completar el ADA. No se registró inspección manual del código por parte del estudiante.

## Requirement / Specification Changes

Antes del commit base se resolvieron Q-01 y Q-02 según las opciones del borrador. No se cambiaron `REQUIREMENTS.md` ni `SPEC.md` para hacer pasar pruebas.

## Final Verification

`pytest -v`: 15 aprobadas. Instalación editable y `customer-search ana` verificados en un entorno virtual con Python 3.12; ejecución directa de la CLI verificada con Python 3.13. La revisión académica personal del estudiante y una ejecución completa de las tareas por `agy` siguen pendientes.

## Lessons Learned

Los IDs y criterios de aceptación permitieron convertir el alcance en pruebas concretas. Registrar las fallas del agente evita atribuirle código que no escribió. La revisión humana debe documentar decisiones reales, no suponerse a partir de pruebas aprobadas.
