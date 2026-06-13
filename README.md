# claude-tasks

Sistema personal de gestión de tareas con priorización asistida por IA.

## Cómo funciona

Cada archivo en `active/` es una tarea pendiente. Cuando se completa, se elimina.

Cuando el usuario pregunta qué atacar, Claude lee dos fuentes:
1. Los archivos en `active/` — tareas sin deadline o con subtareas que vale la pena rastrear individualmente
2. Google Calendar — eventos con fecha concreta (parciales, entregas, Ruta Nocturna, cumpleaños, cualquier deadline)

Claude pondera ambas fuentes, infiere prioridad según urgencia, consecuencias y dependencias, y devuelve una tarea top con razonamiento breve y una alternativa. No una lista rankeada.

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
- Descripción libre con todo el contexto relevante: qué hay que hacer,
  consecuencias de no hacerlo, dependencias con otras tareas, qué tan avanzado está.