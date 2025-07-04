# 🧠 Predicción de Diabetes Tipo 2 con Machine Learning

Este proyecto aplica ciencia de datos al diagnóstico predictivo de diabetes tipo 2, utilizando un conjunto de datos clínico real. El objetivo fue construir un modelo capaz de identificar posibles casos de diabetes a partir de variables médicas como glucosa, insulina, IMC, presión arterial y antecedentes familiares.

---

## 📌 Objetivo

Desarrollar y evaluar modelos de clasificación supervisada que ayuden a identificar pacientes en riesgo de desarrollar diabetes tipo 2.

---

## 🔬 Flujo del proyecto

1. **Exploración de datos**
   - Análisis de outliers, valores inválidos (como ceros en glucosa o insulina).
   - Estudio del sesgo de variables numéricas.

2. **Limpieza y transformación**
   - Reemplazo de ceros inválidos por `NaN`.
   - Imputación con `KNNImputer` optimizado por MAE.

3. **Visualización**
   - Histogramas, boxplots, matriz de correlación.
   - Comparación entre grupos (`Outcome = 0` vs `1`).

4. **Modelado**
   - Se entrenaron y compararon:
     - `Logistic Regression`
     - `Random Forest`
     - `XGBoost` (modelo final)
   - Optimización de hiperparámetros con `GridSearchCV` y `RandomizedSearchCV`.

5. **Evaluación**
   - Métricas clave: `Accuracy`, `Recall`, `F1-score`, `ROC AUC`
   - Elección del modelo con mejor balance general.

---

## 🤖 Resultados

🔹 **Modelo final: XGBoost optimizado**

| Métrica     | Valor   |
|-------------|---------|
| Accuracy    | 0.76    |
| Recall      | 0.70    |
| F1-score    | 0.67    |
| ROC AUC     | 0.83    |

Este modelo fue seleccionado por su capacidad para identificar correctamente casos positivos de diabetes, manteniendo un buen balance con la precisión.

---

## 🧰 Tecnologías usadas

- Python
- Jupyter Notebook
- Pandas, NumPy
- scikit-learn
- XGBoost
- Matplotlib, Seaborn

---

## 📁 Estructura del repositorio

<pre> <code> ``` diabetes-prediccion-ml/ ├── data/ │ ├── diabetes.csv │ ├── diabetes_imputado.csv │ └── diabetes_imputado_modelado.csv │ ├── models/ │ ├── modelo_xgboost_diabetes.pkl │ ├── modelo_diabetes_random_forest.pkl │ └── modelo_LogisticRegression_diabetes.pkl │ ├── notebooks/ │ └── diabetes_modelo_final.ipynb │ ├── README.md └── .gitignore ``` </code> </pre>


## 📌 Cómo reproducir

1. Clonar este repositorio.
2. Crear un entorno virtual e instalar las dependencias:

```bash
pip install -r requirements.txt
```
---

✨ Inspiración
Este proyecto se basó en el conjunto de datos de la población Pima Indian Diabetes disponible en Kaggle y UCI ML Repository, con un enfoque práctico en limpieza de datos reales y modelado robusto para aplicación clínica.


## 🩺 Autor

**Andrés Felipe Ruiz Hernández**  
Ingeniero biomédico y aspirante a científico de datos, con interés en el análisis clínico y modelos predictivos para la salud pública.  
[🔗 LinkedIn](https://www.linkedin.com/in/andresfeliperuiz/) • [🔗 GitHub](https://github.com/afeliperh)