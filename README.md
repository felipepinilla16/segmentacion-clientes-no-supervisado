# Segmentación de Clientes mediante Aprendizaje No Supervisado

Proyecto académico de analítica de datos orientado a identificar grupos o perfiles de clientes a partir de un conjunto de más de 8,000 registros con variables numéricas, sin variable objetivo previa.

## Enfoque metodológico
Al tratarse de un problema no supervisado, no se utiliza partición supervisada de entrenamiento/prueba contra etiquetas conocidas ni métricas de clasificación/regresión supervisada. El flujo se centra en:
- Análisis exploratorio de datos (tipos de datos, estadísticos descriptivos, asimetría y correlaciones).
- Limpieza, selección de variables relevantes y escalado numérico.
- Agrupamiento (clustering) y evaluación estructural (por ejemplo, método del codo y coeficiente de silueta) para interpretar cada segmento.

## Estructura del repositorio
- `data/raw/`: Conjunto de datos original sin modificar.
- `data/processed/`: Datos depurados y transformados listos para el modelado.
- `notebooks/`:
  - `01_exploracion.ipynb`: Análisis exploratorio, distribuciones, asimetrías y matriz de correlación.
  - `02_limpieza.ipynb`: Limpieza, tratamiento de valores atípicos/nulos y preparación de variables.
  - `03_modelamiento_segmentacion.ipynb`: Selección de número de grupos, entrenamiento de modelos no supervisados y perfilamiento de segmentos.
- `src/`: Módulos reutilizables de Python (`preprocessing.py`, `clustering.py`, `evaluation.py`).
- `models/`: Modelos o transformadores serializados.
- `deployment/`: Prototipo o aplicación de visualización/consulta (`app.py`).
- `presentation/`: Material de apoyo para la sustentación.

## Datos
- Archivo original en `data/raw/` (incluir el nombre del archivo o enlace de origen si el tamaño supera el límite de GitHub).
