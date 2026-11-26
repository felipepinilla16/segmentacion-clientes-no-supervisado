# Segmentación de Clientes mediante Aprendizaje No Supervisado

Proyecto académico de analítica de datos orientado a identificar grupos o perfiles de clientes de tarjetas de crédito a partir de su comportamiento financiero, utilizando técnicas de aprendizaje no supervisado sobre un conjunto de más de 8,900 registros con variables numéricas y sin variable objetivo previa.

## Enfoque metodológico
Al tratarse de un problema no supervisado, no se emplean etiquetas conocidas ni métricas de clasificación o regresión supervisada. El flujo de trabajo se estructura en las siguientes etapas:
- **Análisis exploratorio de datos (EDA):** revisión de tipos de variables, valores faltantes, estadísticos descriptivos, asimetría y correlaciones.
- **Preprocesamiento y limpieza:** tratamiento de valores nulos y atípicos, selección de variables relevantes y escalado numérico.
- **Modelamiento y evaluación estructural:** determinación del número óptimo de grupos (método del codo y coeficiente de silueta), entrenamiento de algoritmos de agrupamiento (*clustering*) y caracterización de cada segmento de clientes.

## Estructura del repositorio
```text
segmentacion-clientes-no-supervisado/
├── data/
│   ├── raw/                 # Conjunto de datos original sin modificar (CC GENERAL.csv)
│   └── processed/           # Datos depurados, escalados y listos para el modelado
├── notebooks/
│   ├── 01_exploracion.ipynb               # Análisis exploratorio, distribuciones y correlaciones
│   ├── 02_limpieza.ipynb                  # Limpieza, tratamiento de nulos/atípicos y escalado
│   └── 03_modelamiento_segmentacion.ipynb # Selección de k, clustering y perfilamiento de grupos
├── src/
│   ├── __init__.py
│   ├── preprocessing.py     # Funciones reutilizables de limpieza y transformación
│   ├── clustering.py        # Entrenamiento y predicción de modelos de agrupamiento
│   └── evaluation.py        # Cálculo de métricas internas y validación de clústeres
├── models/                  # Modelos y escaladores serializados
├── deployment/
│   └── app.py               # Prototipo o aplicación de visualización de segmentos
├── presentation/            # Diapositivas y material de apoyo para la sustentación
├── requirements.txt         # Dependencias del proyecto en Python
└── README.md                # Documentación principal del repositorio
```
## Fuente de datos
- **Archivo en repositorio:** `data/raw/CC GENERAL.csv`
- **Enlace original:** [Credit Card Dataset for Clustering en Kaggle](https://www.kaggle.com/datasets/arjunbhasin2013/ccdata/data)
- **Alcance:** Registros de uso de tarjetas de crédito de aproximadamente 8,950 clientes activos durante un periodo de 6 meses (saldos, frecuencia de compras, avances en efectivo, límite de crédito y pagos).
