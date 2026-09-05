# REHAB - Clasificación de Movimientos de Rehabilitación

Proyecto de Machine Learning basado en el dataset **REHAB**, un conjunto de datos cinemáticos obtenidos mediante sensores portátiles para el análisis de movimientos de rehabilitación en pacientes que han sufrido un accidente cerebrovascular (ACV).

## Objetivo

Desarrollar un modelo capaz de **clasificar movimientos de rehabilitación** a partir de la información registrada por los sensores.

El proyecto sigue las principales etapas de **CRISP-DM**:

1. Exploración y comprensión de los datos.
2. Limpieza y preparación de los datos.
3. Extracción de características.
4. Entrenamiento y evaluación del modelo.

## Estructura del repositorio

* `Data/` → Dataset original y documentación de los datos.
* `EDA_Report/` → Análisis exploratorio de datos.
* `ETL_Cleaning/` → Limpieza y preprocesamiento.
* `Model_from_scratch/` → Dataset de características e implementación manual del modelo.
* `utils/` → Funciones auxiliares utilizadas durante el procesamiento.

## Modelo

Para la clasificación se implementó **Softmax Regression (Regresión Logística Multiclase) desde cero**, sin utilizar frameworks de Machine Learning como Scikit-learn, TensorFlow o PyTorch.

El modelo utiliza características estadísticas extraídas de las señales de los sensores para predecir el movimiento realizado.
