# Predicción del Bienestar Físico del Recién Nacido (Cardiotocografía y Metadatos)

Este proyecto tiene como objetivo desarrollar un **modelo predictivo** utilizando datos de **Cardiotocografía (CTG)** intraparto y **metadatos maternos/fetales** tabulares para evaluar el bienestar físico de los recién nacidos. El modelo busca clasificar el estado de salud fetal, lo cual es vital para la toma de decisiones clínicas.

---

## Inicio Rápido

### 1. Requisitos

Asegúrate de tener instalado **Python 3.x** y las siguientes librerías. Para la gestión de archivos `.xlsx` y el entorno de desarrollo, se incluyen `openpyxl` y `jupyter`:

* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `scikit-learn`
* `openpyxl`
* `jupyter`

Puedes instalar todas las dependencias con `pip` (asegúrate de que el archivo `requirements.txt` esté actualizado con las librerías mencionadas):

```bash
pip install -r requirements.txt
2. Estructura del Proyecto
La estructura principal del repositorio es la siguiente:

.
├── Proyecto.ipynb             # Notebook principal con el análisis, preprocesamiento y modelo predictivo.
├── data/
│   ├── raw/                   # Directorio para almacenar los datos originales sin modificar.
│   └── data/                  # Directorio de trabajo para datos procesados e intermedios.
│       ├── signals/           # Contiene los archivos .csv con las señales CTG (Cardiotocografía).
│       └── ...                # Otros archivos de datos como 'train_data_cleaned.xlsx'.
├── Laboratorio 4.ipynb        # (Posiblemente otro análisis/notebook relacionado al curso de DSP).
└── README.md                  # Este archivo.
3. Ejecución
Clonar el repositorio:

Bash

git clone [URL_DEL_REPOSITORIO]
Abrir el Notebook: Inicia un servidor de Jupyter y abre el archivo principal.

Bash

jupyter notebook Proyecto.ipynb
Ejecutar celdas: Sigue las instrucciones dentro del Notebook y ejecuta las celdas secuencialmente para realizar la carga de datos, la limpieza, el preprocesamiento, el entrenamiento del modelo y la evaluación de resultados.

Metodología y Análisis
1. Preprocesamiento de Datos
El análisis inicia con la carga de múltiples archivos CSV de señales CTG y su posterior fusión con un conjunto de metadatos tabulares. La fase de preprocesamiento incluye:

Ingeniería de Características: Extracción de parámetros clave (estadísticos y específicos de CTG) de las series de tiempo para convertirlas en un formato tabular apto para el modelado.

Limpieza y Estandarización: Manejo de valores nulos, atípicos y conversiones de formato para garantizar la calidad del DataFrame final (train_data_cleaned.xlsx).

2. Modelado y Clasificación
El proyecto aborda un problema de Clasificación Multiclase sobre el estado de salud fetal.

Modelo: [Insertar aquí el algoritmo de Machine Learning específico utilizado (e.g., Random Forest, Gradient Boosting, SVM, etc.).]

Entrenamiento: El modelo se entrena en el conjunto de datos preprocesado para aprender a mapear las características maternas/fetales y de la señal CTG a la clase de bienestar fetal.

3. Evaluación
El rendimiento del modelo se valida utilizando métricas estándar para problemas de clasificación, con un énfasis particular en la precisión de la identificación de estados de riesgo:

Métricas Primarias: Accuracy, Precision, Recall y F1-Score.

Visualización: Se genera la Matriz de Confusión para una evaluación detallada de los resultados de clasificación por clase.

Tecnologías y Autores
1. Herramientas
Lenguaje: Python

Análisis y Datos: Pandas, NumPy

Visualización: Matplotlib, Seaborn

Machine Learning: Scikit-learn

Entorno: Jupyter Notebook

2. Autores
Julián David Quintero Medina (20191177171)
Daniel Enrique Perdomo Carvajal (20192183270)
