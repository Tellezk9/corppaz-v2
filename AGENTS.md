# Reglas de Interacción con el Asistente AI (Optimización de Cuota)

Este archivo contiene las directrices para interactuar con la IA en este proyecto. El objetivo es maximizar la eficiencia, evitar errores y reducir el consumo innecesario de tokens/cuota.

## 1. Agrupación de Peticiones (Batching)
- **Instrucción:** El usuario agrupará múltiples tareas en un solo mensaje. 
- **Acción IA:** La IA debe resolver todos los puntos listados en una sola respuesta o bloque de ejecución, evitando pedir confirmación paso a paso para tareas simples.

## 2. Contexto Estricto y Delimitado
- **Instrucción:** El usuario indicará exactamente qué archivos analizar o modificar.
- **Acción IA:** La IA **NO debe** realizar búsquedas globales en el proyecto a menos que sea absolutamente necesario. Debe enfocarse estrictamente en los archivos mencionados en el prompt para no consumir tokens leyendo código irrelevante.

## 3. Planificación antes de Ejecución (Planning Mode)
- **Instrucción:** Para características nuevas o refactorizaciones de más de un archivo.
- **Acción IA:** La IA debe utilizar su modo "Planning". Primero debe analizar, luego escribir un documento de plan (`implementation_plan.md`) y **detenerse** a esperar la aprobación del usuario antes de empezar a modificar el código fuente.

## 4. Ediciones Quirúrgicas y Respuestas Concisas
- **Instrucción:** La IA debe evitar reescribir archivos completos cuando no es necesario.
- **Acción IA:** Utilizar preferentemente las herramientas de edición y reemplazo de texto (`replace_file_content` o `multi_replace_file_content`) en lugar de sobreescribir todo el archivo. Si muestra código en el chat, debe mostrar solo el fragmento modificado.

## 5. Reinicio de Contexto (Nuevos Chats)
- **Instrucción:** Las conversaciones no deben eternizarse.
- **Acción Usuario/IA:** Al terminar una tarea lógica (ej. "Crear endpoint de Vehículos"), se da por concluido el chat. El usuario abrirá una nueva conversación para la siguiente tarea.

# 6. Archivos no modificables 
- **Instrucción:** El dominio, y los modelos no son modificables, de eso me encargo yo, a no ser que te lo pida explicitamente



# 7. Relacion aspecto del figma
- **Instrucción:** Los diseños del figma están hechos en una pantalla de 1440 x 834 de altura,  cuando vayas a diseñar ten esto en cuenta ,ya quiza las instrucciones como "no se ve como en el figma" pueden generar confusion  Aclaro que el figma tiene una pantalla de 1440 de 

# 8. NO HAGAS BUILD
- **Instrucción:** No realices el comando "npm run build", solo úsalo si te lo pido explicitamente