# 🌧️ Predicción de Lluvia en Australia (Machine Learning)

Este proyecto aplica un flujo completo de Ciencia de Datos para clasificar y predecir si lloverá al día siguiente en Australia a partir de registros meteorológicos históricos.

---

## 📌 Resumen del Proyecto

El objetivo principal es construir un modelo predictivo capaz de identificar patrones en variables como humedad, presión atmosférica y horas de sol, manejando el desbalance de clase inherente a eventos meteorológicos.

### 🛠️ Tecnologías Utilizadas
* **Lenguaje:** Python
* **Procesamiento de Datos:** Pandas, NumPy
* **Visualización:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (Random Forest, StandardScaler, Metrics)
* **API/Datos:** KaggleHub

---

## 🚀 Metodología y Flujo de Trabajo

1. **Carga Automática:** Integración con la API de Kaggle para la obtención dinámica del dataset (`weatherAUS.csv`).
2. **Análisis Exploratorio de Datos (EDA):** Evaluación del desbalance de la variable objetivo (`RainTomorrow`) y correlación de variables climáticas.
3. **Ingeniería de Características:** 
   * Extracción de estacionalidad (mes).
   * Eliminación de `RISK_MM` para prevenir **Data Leakage**.
   * Imputación de valores nulos mediante la *mediana* (variables numéricas) y la *moda* (variables categóricas).
   * Codificación mediante *One-Hot Encoding*.
4. **Modelado y Evaluación:**
   * Algoritmo: `RandomForestClassifier` con ajuste de pesos (`class_weight='balanced'`).
   * Evaluación mediante Matriz de Confusión, Curva ROC-AUC y Top 10 variables predictoras.

---

## 📊 Resultados Destacados

* **ROC-AUC Score:** ~0.88 (Alta capacidad discriminativa entre días secos y lluviosos).
* **Variables Predictoras Clave:** La humedad a las 3:00 PM (`Humidity3pm`), las horas de sol (`Sunshine`) y la presión atmosférica mostraron la mayor importancia predictiva.

---

## 📂 Estructura del Repositorio

```text
├── Mineria_de_Datos.ipynb  # Cuaderno de Google Colab con el flujo completo
└── README.md              # Documentación del proyecto
