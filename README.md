# 🧹Agente IA para Mantener un Cuarto Ordenado 
Este proyecto implementa un agente inteligente con Google Gemini (Vertex AI) que simula el proceso de razonar y actuar para ordenar un cuarto.
El agente observa el estado actual del entorno (ropa, libros, tacho de basura) y decide qué acción realizar en cada ciclo hasta dejar todo en orden.

---


## 🚀 Descripción
- Utiliza el modelo Gemini para generar acciones en formato JSON.
- Implementa un entorno simulado con elementos básicos de un cuarto.
- Aplica un bucle de razonamiento y acción (ReAct) donde la IA:
- Observa el estado del cuarto.
- Elige una acción.
- Modifica el entorno según la acción.
- Itera hasta que el cuarto quede ordenado o se cumpla un máximo de ciclos.

## 📂 Funcionalidades principales
- Inicialización del modelo Gemini
  * Configuración de parámetros como **max_output_tokens**, **temperature**, **top_p**.
  * Reglas de seguridad para bloquear contenido dañino.
- Definición del entorno del cuarto
  * Estado inicial con ropa en el piso, libros desordenados y un tacho vacío.
  * Funciones que permiten al agente guardar ropa, ordenar libros y vaciar el tacho.
- Bucle principal de ejecución
  * Observa el estado actual.
  * Genera la próxima acción en JSON.
  * Aplica la acción en el entorno.
  * Repite hasta que todo esté en orden.
- Resultados esperados
  * El programa imprime las acciones ejecutadas paso a paso.
  * Al finalizar, muestra si el cuarto quedó completamente ordenado.

## 🛠️ Tecnologías utilizadas
- Python 3
- Vertex AI (Google Gemini)

## 📋 Ejemplo de salida esperada
```bash

🔄 Ciclo #1  
📦 Gemini respondió: {"next_action": "guardar_ropa", "rationale": "Primero debemos recoger la ropa del piso"}  
➡️ Acción sugerida: guardar_ropa  
🧠 Razonamiento: Primero debemos recoger la ropa del piso  

🔄 Ciclo #2  
📦 Gemini respondió: {"next_action": "ordenar_libros", "rationale": "Después organizamos los libros"}  
➡️ Acción sugerida: ordenar_libros  
🧠 Razonamiento: Después organizamos los libros  

✅ El cuarto está completamente ordenado.  
```
