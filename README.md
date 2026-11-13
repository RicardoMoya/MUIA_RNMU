# Redes Neuronales Multicapa (RNMU)

Material práctico de la asignatura **Redes Neuronales Multicapa** del Máster Universitario en Inteligencia Artificial (MUIA). El repositorio reúne notebooks para estudiar el aprendizaje supervisado paso a paso, junto con ejercicios complementarios de evaluación, preparación de datos y regularización.

## Contenido del repositorio

### Tema 1 · Modelos lineales y gradiente descendente

| Notebook | Contenido |
| --- | --- |
| [1.1 · Regresión lineal simple interactiva](1_01_Regresion_Lineal_Simple_Gradiente_Descendente_Interactivo.ipynb) | Ajuste de una recta mediante gradiente descendente, avanzando una época cada vez. |
| [1.2 · Regresión lineal simple: calorías](1_02_Regresion_Lineal_Simple_Gradiente_Descendente_Calorias.ipynb) | Predicción de calorías a partir del tiempo de carrera. |
| [1.3 · Regresión lineal múltiple: calorías](1_03_Regresion_Lineal_Multiple_Gradiente_Descendente_Calorias.ipynb) | Predicción con tiempo, peso y velocidad; ajuste de varios parámetros. |
| [1.4 · Clasificación con regresión logística](1_04_Clasificacion_Regresion_Logistica_Gradiente_Descendente_Interactivo.ipynb) | Clasificación binaria y evolución de la frontera de decisión durante el entrenamiento. |

### Bonus Track · Conceptos complementarios

| Notebook | Contenido |
| --- | --- |
| [01 · Técnicas de evaluación](BonusTrack_01_Tecnicas_de_Evaluacion.ipynb) | Partición de datos y validación de modelos. |
| [02 · Evaluación de regresión](BonusTrack_02_Evaluacion_Modelos_Regresion.ipynb) | Métricas para comparar predicciones continuas. |
| [03 · Evaluación de clasificación](BonusTrack_03_Evaluacion_Modelos_Clasificacion.ipynb) | Matriz de confusión y métricas de clasificación. |
| [04 · Ingeniería de características](BonusTrack_04_Ingenieria_de_Caracteristicas.ipynb) | Preparación y transformación de variables. |
| [05 · Correlación de datos](BonusTrack_05_Correlacion_de_Datos.ipynb) | Análisis de relaciones entre variables. |
| [06 · Regularización](BonusTrack_06_Regularizacion_L1_L2_ElasticNet.ipynb) | Comparación de L1, L2 y Elastic Net. |

Los archivos de ejemplo están en [`datasets/`](datasets/) y las imágenes utilizadas por los notebooks en [`imgs/`](imgs/). Las dependencias se encuentran en [`requirements.txt`](requirements.txt).

## Instalación

Los ejemplos se pueden ejecutar en Windows, macOS y Linux. Se recomienda **Python 3.11** y [`uv`](https://docs.astral.sh/uv/getting-started/installation/) para crear el entorno e instalar las librerías.

### 1. Instalar `uv`

En Windows, con PowerShell y WinGet:

```powershell
winget install --id=astral-sh.uv -e
```

En macOS o Linux:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Abre una terminal nueva y comprueba la instalación con `uv --version`.

### 2. Crear el entorno e instalar las dependencias

Desde la carpeta raíz del repositorio:

```bash
uv python install 3.11
uv venv --python 3.11 .venv
uv pip install --python .venv -r requirements.txt
```

### 3. Abrir los notebooks

En Windows (PowerShell):

```powershell
.\.venv\Scripts\Activate.ps1
jupyter notebook
```

En macOS o Linux:

```bash
source .venv/bin/activate
jupyter notebook
```

Selecciona el kernel del entorno `.venv` en Jupyter. Si PowerShell impide la activación, puedes usar CMD con `.venv\Scripts\activate.bat`. Para salir del entorno, ejecuta `deactivate`.

## Orden recomendado

Comienza por los notebooks **1.1 a 1.4**, en ese orden: primero se ajusta una recta, después un modelo con varias entradas y, por último, un clasificador. Los notebooks **Bonus Track** amplían los métodos de evaluación y la preparación de datos; puedes consultarlos cuando aparezcan esos conceptos en los ejercicios principales.

## Librerías

El entorno incluye NumPy, pandas, SciPy, Matplotlib, Seaborn, scikit-learn y Jupyter. [`requirements.txt`](requirements.txt) también incorpora TensorFlow/Keras, TensorBoard, Optuna y otras herramientas para los siguientes temas de la asignatura. Una GPU es opcional; si quieres utilizarla, consulta los [requisitos de instalación de TensorFlow](https://www.tensorflow.org/install/pip).

## Autor

**Ricardo Moya**
