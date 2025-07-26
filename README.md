# AluraChallengeTelecom

# Análisis de Churn de Clientes de Telecom

## Introducción

Este proyecto presenta un análisis exploratorio de los datos de clientes de una empresa de telecomunicaciones con el objetivo de identificar los factores clave que contribuyen a la evasión de clientes (Churn). Comprender por qué los clientes se van es fundamental para implementar estrategias de retención efectivas y mejorar la rentabilidad del negocio.

## Origen de los Datos

Los datos utilizados en este análisis fueron obtenidos de un archivo JSON disponible en la siguiente URL:
https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/refs/heads/main/TelecomX_Data.json 

## Limpieza y Tratamiento de Datos

El proceso de limpieza y preparación de los datos incluyó los siguientes pasos:

- Carga de los datos desde la URL utilizando la librería `requests`.
- Normalización de la estructura JSON anidada a un DataFrame plano utilizando `pandas.json_normalize()`.
- Exploración inicial de la estructura del DataFrame, tipos de datos y identificación de valores únicos y duplicados.
- Manejo de valores vacíos (`''`) en las columnas 'Churn' y 'account.Charges.Total'. Se eliminaron las filas con valores vacíos en 'Churn' y se convirtieron los valores de 'account.Charges.Total' a numérico, tratando los errores con `errors='coerce'`.

## Análisis Exploratorio de Datos 

Se realizaron diversas visualizaciones y análisis para explorar la relación entre las diferentes variables y el Churn de clientes. Los hallazgos clave incluyen:

- La distribución del Churn es similar entre géneros, pero los clientes Senior Citizen muestran una tasa de Churn más alta.
- Los clientes con menor antigüedad (tenure bajo) tienen una probabilidad significativamente mayor de hacer Churn.
- Existe una correlación entre altos cargos mensuales, baja antigüedad y una mayor tendencia al Churn.
- Los contratos mes a mes están fuertemente asociados con una alta tasa de Churn, mientras que los contratos de mayor duración actúan como factor de retención.
- Los clientes con servicio de internet de fibra óptica presentan una tasa de Churn más alta que aquellos con DSL.
- El método de pago "Electronic check" está relacionado con una mayor tasa de Churn.
- La adopción de servicios adicionales como seguridad online y soporte técnico parece estar asociada con una menor tasa de Churn.


## Archivos del Proyecto

- `TelecomX_Data.json`: Archivo de datos original.
- `notebook.ipynb`: Notebook de Jupyter/Colab con el código de análisis. (Puede ser este mismo notebook)

## Herramientas y Librerías

- Python
- pandas
- requests
- plotly

## Cómo Ejecutar el Análisis

Para replicar este análisis, puedes ejecutar el código contenido en el notebook `notebook.ipynb`. Asegúrate de tener instaladas las librerías necesarias (`pandas`, `requests`, `plotly`).
