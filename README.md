# 🚲 EcoBici — Segmentación de Usuarios y Predicción de Churn

Proyecto de análisis de datos y Machine Learning aplicado a datos abiertos de **EcoBici, Ciudad de Buenos Aires**, orientado a identificar perfiles de usuarios y predecir riesgo de abandono (*churn*).

## 🎯 Objetivo

Analizar el comportamiento histórico de los usuarios para:

* Segmentar usuarios según sus patrones de uso.
* Identificar factores asociados al abandono.
* Predecir usuarios con riesgo de *churn*.
* Generar insights para estrategias de retención.

## 📊 Datos

Se utilizaron datos abiertos de recorridos de EcoBici publicados por el Gobierno de la Ciudad de Buenos Aires.

El dataset contiene información sobre:

* Edad y género.
* Fechas y horarios de viajes.
* Duración de recorridos.
* Estaciones de origen y destino.
* Identificadores de viajes y usuarios.

## 🔄 Flujo del proyecto

```text
Datos de viajes
      ↓
Limpieza y preprocesamiento
      ↓
Feature Engineering
      ↓
Matriz RFM a nivel usuario
      ↓
EDA
      ↓
K-Means
      ↓
Clasificación de Churn
      ↓
Evaluación y optimización
```

## ⚙️ Feature Engineering

Se transformaron los registros transaccionales de viajes en métricas agregadas a nivel usuario:

* **Recencia:** días desde el último viaje.
* **Frecuencia:** cantidad total de viajes.
* **Intensidad:** duración promedio de los recorridos.
* **Churn:** usuario con más de 60 días de inactividad.

## 🤖 Machine Learning

### Segmentación

Se utilizó **K-Means** para identificar perfiles de comportamiento.

El número de clusters se evaluó mediante:

* Método del Codo.
* Silhouette Score.
* StandardScaler para estandarización de variables.

### Predicción de Churn

Se evaluaron dos modelos:

* Regresión Logística como baseline.
* Random Forest Classifier.

La optimización del modelo se realizó mediante **GridSearchCV** y validación cruzada de 5 folds.

## 📈 Evaluación

Se utilizaron:

* Matriz de Confusión.
* Recall.
* F1-Score Macro.
* Validación Cruzada.

El **Recall** fue priorizado debido al objetivo de identificar la mayor cantidad posible de usuarios en riesgo de abandono.

## 🛠️ Tecnologías

* Python
* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn
* Google Colab

## 📁 Estructura

```text
.
├── Pre_Entrega_Proyecto_Final/
│   ├── ML_Pre_Entrega_Proyecto_Final.ipynb
│   └── dataset/
│
├── Entrega_Final_Proyecto_Integrador/
│   ├── Perea_Daniela_Comision_25262_TPI_Machine_Learning.ipynb
│   └── dataset/
│       ├── recorridos-2025.csv
│       └── usuarios_procesado_rfm.csv
│
└── README.md
```

## 💡 Resultados e Insights

El análisis permite identificar diferentes perfiles de uso y desarrollar un modelo orientado a detectar usuarios con riesgo de abandono.

Las conclusiones finales y métricas obtenidas se encuentran documentadas en el notebook de la entrega final.
* [Ver conclusiones 🡥](https://github.com/daniela-perea/ecobici-user-segmentation-churn)

## 👩‍💻 Autora

**Daniela Perea**

Estudiante de Ciencia de Datos e Inteligencia Artificial.

---
