# Transformación de informes médicos en escalas funcionales.

Este repositorio contiene los recursos utilizados para el ajuste fino de un modelo de lenguaje (LLM) con el objetivo de evaluar entrevistas médicas basadas en la escala de discapacidad de Oswestry.

##  Estructura del Repositorio
    ```
    .
    ├── Codigos
    │   ├── ajuste_fino.ipynb
    │   └── scripts_precision.ipynb
    ├── resultados_comparativos
    │   ├── Modelo Base Mistral
    │   │   ├── precision_entrevista.pdf
    │   │   └── precision_item.pdf
    │   └── Modelo Especializado
    │       ├── precisión_entrevista.pdf
    │       └── precisión_item.pdf
    ├── estadisticas_precision.pdf
    └── conjunto_entrenamiento.json
    ```
## Descripción de Archivos

### Codigos
- `ajuste_fino.ipynb`: Cuaderno Jupyter con el proceso de ajuste fino del modelo de lenguaje utilizando el conjunto de entrenamiento.
- `scripts_precision.ipynb`: Análisis de precisión del modelo para cada ítem de la escala Oswestry y desempeño general en entrevistas.

### resultados_comparativos

Contiene resultados de precisión de dos variantes del modelo:

#### Modelo Base Mistral
- `precision_entrevista.pdf`: Resultados globales del modelo sin ajuste en la evaluación de entrevistas.
- `precision_item.pdf`: Análisis detallado por ítem de la escala.

#### Modelo Especializado
- `precisión_entrevista.pdf`: Evaluación de entrevistas posterior al ajuste fino.
- `precisión_item.pdf`: Resultados por ítem del modelo especializado.

### Archivos varios
- `estadisticas_precision.pdf`: Estadísticas comparativas generales de precisión entre modelos.
- `conjunto_entrenamiento.json`: Conjunto de datos utilizados para el ajuste fino. Incluye entrevistas anotadas con referencia a los ítems de la escala Oswestry.

## Objetivo del Proyecto

El objetivo es mejorar la capacidad del modelo de lenguaje para interpretar entrevistas médicas y clasificar correctamente los niveles de discapacidad según los criterios de la **Escala Oswestry**, contribuyendo así a herramientas automáticas de apoyo diagnóstico.

## Requisitos

- Python 3.10+
- Transformers (Hugging Face)
- Jupyter Notebook
- PyTorch
- scikit-learn
- pandas, matplotlib

> Consulta el notebook `ajuste_fino.ipynb` para más detalles sobre las dependencias y la configuración del entorno.
---
> El modelo ya especializado se encuentra en su repositorio en [HuggingFace](https://huggingface.co/DrAleML/Oswestry-Instruct).
