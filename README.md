Nota: La entrega final "Proyecto_ParteIII_Arancibia" la encontrarán en la carpeta "Entregas".

---

# 🍷 Predicción de calidad de vino tinto con Árbol de Decisión

Este proyecto fue desarrollado en marco del curso **Data Science I** de Coderhouse. Se trabajó con un dataset de vinos tintos y se aplicaron técnicas de análisis exploratorio, selección de variables y modelado supervisado para predecir la calidad del vino en tres categorías: `baja`, `media` y `alta`.

---

## 📁 Dataset

Se utilizó el dataset **Wine Quality (Red Wine)** del repositorio UCI Machine Learning, con 1144 observaciones y 13 variables fisicoquímicas:

- `fixed acidity`, `volatile acidity`, `citric acid`
- `residual sugar`, `chlorides`, `sulfur dioxide` (free & total)
- `density`, `pH`, `sulphates`, `alcohol`
- `quality` (variable objetivo original: 0 a 10)

La variable `quality` fue transformada en tres clases:
- **baja:** puntuación ≤ 5
- **media:** puntuación = 6
- **alta:** puntuación ≥ 7

---

## 🧠 Objetivos del proyecto

- Formular hipótesis y explorarlas con visualizaciones
- Identificar variables relevantes
- Aplicar una técnica de reducción de dimensionalidad
- Entrenar un modelo de clasificación supervisado (Árbol de Decisión)
- Evaluar su desempeño con métricas
- Interpretar visualmente la lógica del modelo

---

## 🧰 Herramientas y librerías

- **Python** (Google Colab)
- **Pandas**, **NumPy**, **Seaborn**, **Matplotlib**
- `scikit-learn`: 
  - `SelectKBest`, `DecisionTreeClassifier`
  - `train_test_split`, `classification_report`, `confusion_matrix`
- `Axes3D` para gráficos 3D

---

## 🔎 Exploración y visualizaciones

Se analizaron outliers, se aplicó `df.describe()`, se identificaron correlaciones y se trabajaron hipótesis como:

1. A mayor alcohol, mayor calidad
2. A mayor acidez volátil, menor calidad
3. A más sulfitos, menor calidad
4. Alcohol + sulfatos podrían ser determinantes

Cada hipótesis fue acompañada de su respectivo gráfico, análisis estadístico y visualización.

---

## 📉 Selección de variables

Se aplicó `SelectKBest` para reducir la dimensionalidad a las 6 variables más relevantes:

- `alcohol`, `volatile acidity`, `citric acid`, `sulphates`, `total sulfur dioxide`, `fixed acidity`

---

## 🌳 Modelado supervisado

Se entrenó un **Árbol de Decisión multiclase**, sin limitar su profundidad.  
Se utilizó codificación manual para asignar valores numéricos a las clases (`baja = 0`, `media = 1`, `alta = 2`).

---

## 📊 Resultados del modelo

- **Accuracy:** 63%
- **Clase más precisa:** `baja` (F1 = 0.71)
- **Confusión:** principal entre `media` y `alta`
- **Matriz de confusión** incluida
- **Gráfico 3D** de las variables más relevantes (`alcohol`, `sulphates`, `volatile acidity`)

---

## 📌 Conclusiones

- `alcohol` resultó ser la variable más predictiva
- El modelo tiende a predecir mejor la clase `baja`
- Existen zonas de superposición entre `media` y `alta` que dificultan la separación
- El modelo es interpretable y presenta una buena base para aplicar técnicas de mejora

---

## 👨‍💻 Autor

**Nicolás Arancibia**  
Curso: Data Science I – Coderhouse  
GitHub: [@nicoarann](https://github.com/nicoarann)

---

