# Escuela Politécnica Nacional  
## Métodos Numéricos  
Nombre: Erick Cuichan 

Curso: GR1CC

## Tema: Costos relacionados a los modelos de lenguaje  

## ¿Qué es inferencia y entrenamiento?

El **entrenamiento** es la etapa en la que un modelo de lenguaje aprende a partir de grandes cantidades de datos. Durante este proceso, ajusta sus parámetros internos y requiere una gran cantidad de recursos computacionales, como GPUs o TPUs, además de un alto consumo energético.

La **inferencia** ocurre cuando el modelo ya entrenado se utiliza para responder preguntas, generar texto o realizar tareas. En esta fase el modelo no aprende, sino que aplica lo que ya conoce para producir una respuesta.

### Palabras clave

- **Entrenamiento = Aprender**
- **Inferencia = Usar lo aprendido**

---

## Tabla resumen de modelos de lenguaje comerciales

| Modelo | GPU o acelerador utilizado | Costo del hardware | Tiempo de entrenamiento | Consumo energético en entrenamiento | Consumo energético en inferencia |
|---|---|---|---|---|---|
| **GPT-4 — OpenAI** |GPUs NVIDIA A100 y H100| Se estima que se usaron unas 25 000 GPUs A100, con un costo aproximado de $700 millones solo en hardware.| No divulgado; su entrenamiento principal finalizó en agosto de 2022 |  No divulgado. Debido a su escala, habría requerido un consumo muy alto durante el entrenamiento. | Menor que el entrenamiento por consulta individual, pero elevado a gran escala por la cantidad de usuarios. |
| **Claude Opus 4 / Sonnet 4 — Anthropic** |Estimación similar a A100 o H100| No divulgado oficialmente, pero se calcula que el gasto estuvo en decenas de millones de dólares.| No divulgado. Probablemente **varios meses**, incluyendo preentrenamiento y ajuste posterior. | No divulgado oficialmente. | No divulgado; depende del tamaño del modelo y del volumen de consultas atendidas. |
| **Gemini 2.5 Pro — Google** | TPUs desarrolladas por Google v4 o v5| No divulgado oficialmente | No divulgado oficialmente. Se estima que requirió **meses** de entrenamiento. | No divulgado. Google no publica el consumo total en watts. | Google enfatiza eficiencia en sus modelos, pero no reporta watts exactos de inferencia. |
| **Llama 3.1 405B — Meta** | NVIDIA H100 de 80 GB | Meta no publicó el costo total del hardware | 39.3 millones de horas-GPU | Las GPUs H100 pueden alcanzar hasta 700 W por unidad | No divulgado oficialmente |
| **DeepSeek-V3 — DeepSeek** | NVIDIA H800 | Costo de cómputo estimado: **US$ 5.576 millones** | 2.788 millones de horas-GPU | No divulgado en watts totales | No divulgado oficialmente |