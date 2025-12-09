YOLOv12 para Detección de Personas en Escenarios de Incendio

Repositorio oficial del Trabajo de Integración Curricular – Jhandry David Tocto Barreto

Este repositorio contiene el código, los experimentos, las figuras, los modelos entrenados y la documentación asociada al desarrollo de un sistema de detección de personas en escenarios de incendio mediante YOLOv12, tomando como referencia un subconjunto del dataset C2A (Cut-and-Add).
El trabajo se enmarca en la línea de Visión por Computador aplicada a la gestión de riesgos y escenarios de desastre y fue desarrollado como parte del Trabajo de Integración Curricular (TIC) para obtener el título profesional correspondiente.

Objetivo General

Ajustar y evaluar el modelo YOLOv12 para la detección de personas en imágenes correspondientes a escenarios de incendio, utilizando un subconjunto del dataset C2A, verificando su estructura, realizando preprocesamientos específicos y analizando los resultados mediante métricas de evaluación y pruebas estadísticas.

Descripción del Proyecto

El proyecto se basa en:

✔ Verificación estructural del dataset C2A

Se inspeccionó la jerarquía del dataset mediante Python (os, pathlib), validando:

carpetas train/, val/, test/

subcarpetas images/ y labels/

consistencia entre nombres de imágenes y anotaciones

✔ Selección del subconjunto fire

Se extrajeron únicamente las imágenes correspondientes a escenarios de incendio, generando un subconjunto especializado para evaluar detección de personas en condiciones extremas.

✔ Preprocesamiento

Incluyó:

análisis de formato

verificación de anotaciones YOLO

letterboxing y normalización de dimensiones

reorganización de carpetas y estructuras YOLOv12

✔ Entrenamiento del modelo YOLOv12

Se entrenaron múltiples variantes de YOLOv12, ajustando:

hiperparámetros

transferencia de aprendizaje

tasas de aprendizaje

tamaño del batch

número de épocas

✔ Evaluación

Incluye:

precision

recall

AP por clase

mAP50 y mAP50-95

análisis individual por imagen

La evaluación estadística se realizó mediante la prueba de Friedman, comparando el rendimiento entre variantes del modelo.

✔ Interfaz de prueba

Se construyó una interfaz en Gradio para cargar imágenes o videos y observar la inferencia del modelo entrenado.

📊 Resultados Principales

Los resultados mostraron:

desempeño estable del modelo en condiciones de fuego y humo

precisión aceptable para entornos realistas

limitaciones debidas a:

tamaño reducido del subconjunto fire

variabilidad extrema entre imágenes

condiciones de iluminación y oclusiones fuertes

La prueba de Friedman confirmó diferencias estadísticamente significativas entre algunas variantes del modelo.

📦 Dataset C2A

El dataset NO se incluye directamente por restricciones de licencia.

Para obtenerlo:

Visitar la fuente oficial del dataset: https://www.kaggle.com/datasets/rgbnihal/c2a-dataset

