# REHAB Dataset

Esta carpeta contiene los datos utilizados para el proyecto **REHAB**, un dataset cinemático obtenido mediante sensores portátiles durante un programa de rehabilitación de pacientes que han sufrido un accidente cerebrovascular (ACV).

El dataset original fue recopilado a partir de **120 pacientes post-ACV** durante un programa de rehabilitación de dos semanas. Para este proyecto se utiliza únicamente la sección **`Rehab_exercise`**, correspondiente a **16 movimientos de entrenamiento de rehabilitación**. La sección `Rehab_assessment` del dataset original no se incluye en este repositorio.

## Sensores

Los movimientos fueron registrados mediante una red de sensores que incluye:

* **4 sensores IMU** colocados en diferentes partes de las extremidades.
* **1 guante de rehabilitación** con un IMU y sensores de flexión para los dedos.
* Frecuencia de muestreo de **50 Hz**.

Los datos incluyen información de orientación (`pitch`, `yaw`, `roll`) y flexión de los dedos.

## Estructura de los datos

Los archivos se encuentran en formato `.npy` y siguen la nomenclatura:

`<movementID>_<sensorID>.npy`

* `movementID`: identifica uno de los 16 movimientos (`000`–`015`).
* `sensorID = 1`: información de los sensores colocados en las extremidades.
* `sensorID = 2`: información del guante de rehabilitación.

Cada archivo tiene una estructura:

`(d, 880, 6)`

donde:

* `d` = número de muestras del movimiento.
* `880` = número máximo de pasos de tiempo.
* `6` = canales registrados por el grupo de sensores.

El identificador del movimiento incluido en el nombre del archivo funciona como la **clase o etiqueta** utilizada posteriormente para entrenar el modelo de clasificación.

## Carpetas

* `d01_raw_data/` → Datos originales utilizados como punto de partida.
* `d02_processed_data/` → Datos procesados proporcionados por los autores del dataset.
* `d03_clean_data/` → Datos después de nuestro proceso de limpieza.
* `d04_transformed_data/` → Datos limpios y transformados utilizados para el análisis y extracción de características.
* `manifest.csv` → Información de cada muestra, incluyendo movimiento, índice y longitud válida de las señales.

A partir de estos datos se realiza la extracción de características para generar `features.csv`, utilizado posteriormente para entrenar el modelo de clasificación.
