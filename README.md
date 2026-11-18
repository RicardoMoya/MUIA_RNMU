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

### Tema 2 · Redes neuronales multicapa

Entrenamiento de perceptrones multicapa para regresión y clasificación: preparación de datos, arquitectura, función de pérdida, optimizador, hiperparámetros y evaluación. Los últimos ejemplos incorporan regularización L2, Batch Normalization y Dropout.

| Notebook | Contenido |
| --- | --- |
| [2.1 · Perceptrón multicapa: XOR](2_01_Perceptron_XOR.ipynb) | Red 2–2–1 implementada con NumPy. Entrenamiento interactivo por épocas, regiones de clasificación, evolución de la pérdida y diagrama con los pesos y sus cambios. |
| [2.2 · Entrenamiento de una red para regresión](2_02_Entrenamiento_Red_Neuronal_Regresion.ipynb) | Predicción de calorías a partir de tiempo, peso y velocidad. Escalado de entradas, entrenamiento, gráficas de pérdida, MAE y MSE en una fila de tres columnas y predicción para una nueva observación. |
| [2.3 · Ejercicio de regresión: grasa corporal](2_03_ejercicio_entrenamiento_red_neuronal_regresion.ipynb) | Plantilla para predecir el porcentaje de grasa corporal (BFP). Carga de datos implementada y tareas pendientes de preparación, diseño, entrenamiento y evaluación. |
| [2.4 · Clasificación binaria: abandono de clientes](2_04_Clasificacion_Binaria_Churn.ipynb) | Predicción de `Exited` con salida sigmoide y binary crossentropy. Tratamiento del desbalance con `class_weight`, calculado solo con entrenamiento. |
| [2.5 · Clasificación multiclase: precio de smartphones](2_05_Clasificacion_Multiclase_Precio_Smartphones.ipynb) | Clasificación en cuatro categorías de precio mediante una red 20–32–16–4, salida softmax y sparse categorical crossentropy. Revisión de la distribución del target y evaluación multiclase. |
| [2.6 · Smartphones con L2 y Batch Normalization](2_06_Regularizacion_Normalizacion_Clasificacion_Smartphones.ipynb) | El mismo ejemplo de smartphones con un único modelo que añade regularización L2 (Ridge) en los kernels ocultos y Batch Normalization antes de cada ReLU. |
| [2.7 · Smartphones con Dropout](2_07_Clasificacion_Smartphones_Dropout.ipynb) | Continuación del ejemplo 2.6: conserva L2 y Batch Normalization y añade Dropout con tasa 0,20 después de cada ReLU oculta. |
| [2.8 · Ejercicio final de clasificación multiclase](2_08_ejercicio_entrenamiento_red_neuronal_clasificacion_multiclase.ipynb) | Plantilla sin resolver para clasificar objetos astronómicos como galaxias, estrellas o cuásares. Estudio del desbalance, comparación con y sin pesos de clase y evaluación con métricas macro. |

Los ejemplos con TensorFlow/Keras separan los datos en **entrenamiento y test** antes de ajustar el escalado o la codificación. El preprocesado se aprende solo con entrenamiento y se reutiliza en test.

En clasificación, durante el entrenamiento se muestra **accuracy**. Después se representan pérdida, accuracy, precision, recall y F1, junto con las barras de métricas finales y las matrices de confusión de entrenamiento y test. En multiclase, precision, recall y F1 se calculan con promedio **macro**. Las curvas de test tienen una finalidad didáctica: no deben utilizarse para elegir hiperparámetros y presentar después ese mismo test como evaluación final independiente.

Los notebooks **2.3 y 2.8 son ejercicios para completar**, con la carga implementada. Los notebooks **2.6 y 2.7 se entregan sin ejecutar**; sus resultados y gráficas se generarán al ejecutar las celdas en orden.

#### Datasets del tema 2

| Archivo | Problema |
| --- | --- |
| [calories_time_weight_speed.csv](datasets/calories_time_weight_speed.csv) | Regresión: predecir calorías con tiempo, peso y velocidad. |
| [men_body_fat_precentage.csv](datasets/men_body_fat_precentage.csv) | Ejercicio de regresión: predecir `BFP`. Se conserva la grafía `precentage` del archivo original. |
| [Churn.csv](datasets/Churn.csv) | Clasificación binaria desbalanceada: `Exited = 0` permanece y `Exited = 1` abandona. |
| [Mobile_Price_Classification.csv](datasets/Mobile_Price_Classification.csv) | Clasificación de smartphones: 20 características y cuatro clases balanceadas de `price_range`. |
| [star_classification.csv](datasets/star_classification.csv) | Ejercicio multiclase: 100.000 observaciones, clases `GALAXY`, `STAR` y `QSO` desbalanceadas. Se eliminaron las columnas terminadas en `_ID` y se dejó `class` como última columna. |

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

Comienza por los notebooks **1.1 a 1.4**, en ese orden: primero se ajusta una recta, después un modelo con varias entradas y, por último, un clasificador.

Continúa con el **tema 2**: XOR con NumPy (2.1), regresión y su ejercicio (2.2–2.3), clasificación binaria y multiclase (2.4–2.5), regularización y normalización (2.6) y Dropout (2.7). El **ejercicio 2.8** cierra la unidad y permite aplicar lo aprendido a un problema multiclase desbalanceado.

Los notebooks **Bonus Track** amplían los métodos de evaluación y la preparación de datos. Consulta los Bonus Track 01 y 04 al preparar los datos; 02 y 03 al evaluar regresión y clasificación; 05 al estudiar correlaciones y 06 al revisar L1, L2 y Elastic Net.

## Tema 3 · Contenidos previstos

El tema 2 está completo. Para la siguiente unidad quedan previstos:

1. **Checkpoints:** guardar y recuperar el estado de entrenamiento de una red.
2. **Complejidad de los modelos y bias–variance:** capacidad, infraajuste y sobreajuste.
3. **Optimización de hiperparámetros con Optuna:** búsqueda de configuraciones de arquitectura y entrenamiento.
4. **Otras familias de redes, a nivel conceptual:** qué hacen y para qué se utilizan las redes convolucionales, recurrentes, GAN y otras arquitecturas, sin desarrollar su implementación técnica.
5. **GPUs, si da tiempo:** funcionamiento, características relevantes y utilidad para entrenar redes neuronales.

Estos contenidos todavía no tienen notebooks del tema 3 en el repositorio.

## Librerías

El entorno incluye NumPy, pandas, SciPy, Matplotlib, Seaborn, scikit-learn y Jupyter. [`requirements.txt`](requirements.txt) también incorpora TensorFlow/Keras, TensorBoard, Optuna y otras herramientas para los siguientes temas de la asignatura. Una GPU es opcional; si quieres utilizarla, consulta los [requisitos de instalación de TensorFlow](https://www.tensorflow.org/install/pip).

## Autor

**Ricardo Moya**
