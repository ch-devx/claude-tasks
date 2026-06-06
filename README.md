# claude-tasks

Sistema personal de gestión de tareas con priorización asistida por IA.

## Cómo funciona

Cada archivo en `active/` es una tarea pendiente. Cuando se completa, se mueve a `done/`.
Cuando el usuario pregunta qué atacar, Claude lee todo el contenido de `active/`, pondera
prioridad en función de deadlines, consecuencias de no completar la tarea, dependencias
entre tareas y contexto descrito en cada una, y devuelve un orden de ataque con una razón
breve por cada ítem.

El usuario no define pesos ni prioridades manualmente — ese juicio le corresponde a Claude.

## Contexto del usuario

Carlos es estudiante de Ingeniería de Sistemas en UNEFA Maracay, cursando 7mo semestre
con 7 materias activas. Paralelamente opera un hustle de Reddit actualmente en fase de
reconstrucción tras un ban masivo. Entrena calistenia y corre de forma recreativa.
Maneja múltiples frentes simultáneos con deadlines académicos reales y presión de
reconstruir ingresos.

## Formato de cada tarea

Nombre del archivo: descripcion-corta.md

Contenido:
- Título
- Deadline (fecha concreta o "sin deadline" o "recurrente")
- Estado (Pendiente / En progreso / Bloqueada)
- Descripción libre con todo el contexto relevante: qué hay que hacer,
  consecuencias de no hacerlo, dependencias con otras tareas, qué tan avanzado está.