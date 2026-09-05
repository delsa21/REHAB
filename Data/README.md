# Data
Esta carpeta contiene los datos utilizados para el proyecto **REHAB**.

El dataset contiene información cinemática obtenida mediante sensores portátiles durante la realización de movimientos de rehabilitación asociados a pacientes que han sufrido un accidente cerebrovascular (ACV).

Para este proyecto se utilizan los **16 movimientos de entrenamiento de rehabilitación**.

## Contenido

* `Rehab_exercise/` → Archivos con los registros de los movimientos de rehabilitación.
* `Article.pdf` → Artículo científico que describe el dataset REHAB.
* `README.md` → Documentación de los datos.

Los archivos `.npy` contienen las señales registradas por los sensores para cada movimiento.

Posteriormente, estos datos son procesados para extraer características estadísticas y generar el dataset `features.csv`, utilizado para entrenar el modelo de clasificación.
