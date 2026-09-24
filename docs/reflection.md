# Reflexión ADA-05 — borrador para revisión personal

Estas respuestas describen el trabajo observado en el repositorio. El estudiante debe revisarlas y adaptarlas a su propia experiencia antes de entregarlas como reflexión personal.

1. **Requirement, specification y prompt:** El requisito expresa una necesidad con ID estable; la especificación define reglas y criterios verificables; el prompt indica a un agente qué trabajo ejecutar en un momento concreto.
2. **Información indispensable antes de programar:** Historia de usuario, campos de cliente, alcance local, búsqueda por nombre o correo y comportamiento esperado para entradas inválidas y sin coincidencias.
3. **Decisiones previas:** CLI en vez de HTTP, datos ficticios en memoria, orden de entrada, normalización del término y salida de errores.
4. **Errores evitados por SPEC.md:** Evitó tratar la ausencia de coincidencias como error, duplicar un cliente que coincide en ambos campos y dejar indefinidos los códigos de salida.
5. **Separación de REQUIREMENTS.md y SPEC.md:** Impide mantener dos definiciones distintas de un requisito. SPEC referencia IDs y explica cómo comprobarlos.
6. **Papel de AGENTS.md:** Ordena leer los documentos y trabajar por tareas, con pruebas y sin alterar requisitos para acomodar el código.
7. **Cambios durante revisión humana:** No consta todavía una revisión personal del estudiante. Codex corrigió el README tardío de `agy` para que usara el extra `test` real y describiera la CLI implementada.
8. **Arquitectura y código final:** Coinciden los módulos de datos, modelo, búsqueda y CLI; la búsqueda no imprime y la CLI no contiene reglas de coincidencia.
9. **Requisito más difícil de probar:** NFR-02, porque demostrar ausencia de dependencia de red combina una prueba de ejecución con inspección de dependencias y código.
10. **Mejora del proceso:** Dar a `agy` un entorno interactivo con permisos claros y comprobar su salida antes de avanzar a la tarea siguiente.
11. **SPEC.md como contrato:** Sus criterios de aceptación y escenarios permiten comprobar cada ID sin copiar la definición del requisito.
12. **Decisiones del AI Usage Log:** Se pasó de un alcance abierto a CLI en memoria; después se eligieron función pura y `casefold()`. La revisión de pruebas corrigió la documentación y dejó explícito qué aportó `agy` y qué realizó Codex.
