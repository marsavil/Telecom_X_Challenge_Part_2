# Telecom_X_Challenge_Part_2

# 🧠 Churn Prediction - Análisis de Cancelación de Clientes

Este proyecto tiene como objetivo predecir la cancelación de clientes utilizando técnicas de Machine Learning. Se analizan los factores más relevantes que influyen en la cancelación y se proponen estrategias de retención basadas en los resultados obtenidos.

---

## 📂 Contenido

- Exploración y preprocesamiento de datos
- Selección de variables relevantes
- Entrenamiento de modelos (Random Forest, Gradient Boosting)
- Comparación de métricas y selección del modelo campeón
- Análisis interpretativo y visualizaciones
- Recomendaciones para retención de clientes

---

## 📌 Variables Seleccionadas

Tras un proceso de selección de características, se identificaron las siguientes variables como las más relevantes para predecir la cancelación:

- `Contract_Month-to-month`
- `customer_tenure`
- `internet_OnlineSecurity_No`
- `internet_TechSupport_No`
- `internet_InternetService_Fiber optic`
- `account_PaymentMethod_Electronic check`
- `account_Contract_Two year`
- `account_Charges.Monthly`

---

## 🔍 Análisis Exploratorio

### Tiempo de Contrato × Cancelación

Se utilizó un boxplot para mostrar cómo el tiempo de permanencia varía entre quienes cancelan y quienes no:

<img width="686" height="471" alt="chur-tenure" src="https://github.com/user-attachments/assets/64aab74a-a5f8-4e56-97ad-7b5a5d05c1ce" />


📌 **Conclusión:** Los clientes que cancelan suelen tener menor antigüedad.

---

### Gasto Total × Cancelación

También se exploró la relación entre el gasto total y la cancelación:

#### Boxplot:

<img width="704" height="471" alt="churn y gastos" src="https://github.com/user-attachments/assets/733d90db-7422-4cc3-9d7e-271442a44402" />


#### Scatter plot:

<img width="704" height="471" alt="gastos y permanencia" src="https://github.com/user-attachments/assets/4b40add9-d472-4937-847b-81b45ef802f9" />


📌 **Conclusión:** La mayoría de los clientes que cancelan tienen poco tiempo en la compañía y bajo gasto total.

---

## 🤖 Modelos Entrenados

| Modelo             | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|--------------------|----------|-----------|--------|----------|---------|
| Random Forest      |  0.776   | 0.591     | 0.505  | 0.545    | 0.802   |
| Gradient Boosting  |  0.789   | 0.614     | 0.545  | 0.578    | 0.815   |
| **Champion Model** | **0.7411** | **0.5027** | **0.8217** | **0.6238**  |  **0.8373**  |

### Referencias

## 📊 Métricas de Evaluación del Modelo

| Métrica       | Qué mide                                                                 | Fórmula                                         | Cuándo usarla                                                                  |
|---------------|---------------------------------------------------------------------------|--------------------------------------------------|---------------------------------------------------------------------------------|
| ✅ **Accuracy**   | Proporción de predicciones correctas.                                      | (TP + TN) / (TP + TN + FP + FN)                  | Cuando las clases están **balanceadas**.                                        |
| 🎯 **Precision**  | De las predicciones positivas, cuántas fueron correctas.                   | TP / (TP + FP)                                   | Cuando querés **evitar falsos positivos**.                                      |
| 📡 **Recall**     | De los casos positivos reales, cuántos detectó el modelo.                  | TP / (TP + FN)                                   | Cuando se busca **detectar todos los positivos**, incluso con falsos positivos.   |
| ⚖️ **F1 Score**   | Promedio armónico entre Precision y Recall.                                | 2 * (P * R) / (P + R)                             | Cuando hay **clases desbalanceadas** y se quiere equilibrar errores.              |
| 📈 **ROC AUC**    | Qué tan bien distingue el modelo entre clases (positiva vs negativa).     | Área bajo la curva ROC                           | Cuando se quiere evaluar el **rendimiento global** del modelo en distintos umbrales. |


📌 El modelo campeón se seleccionó por su mejor balance entre precisión y recall.

---

## 🧠 Conclusiones

### 🔑 Principales factores que influyen en la cancelación

- **Contratos mensuales** tienen mayor tasa de cancelación.
- **Baja antigüedad** (tenure) está fuertemente asociada a la cancelación.
- **Falta de servicios de seguridad y soporte técnico** (Online Security y Tech Support).
- **Uso de servicios de fibra óptica**, probablemente por costos más altos.
- **Método de pago con débito automático (Electronic check)** se relaciona con más cancelaciones.
- **Clientes con cargos mensuales altos** tienden a cancelar más.

---

## 📈 Recomendaciones de Retención

- Incentivar **contratos anuales o bianuales** con beneficios exclusivos.
- Implementar programas de fidelización para **clientes nuevos**.
- Promocionar y facilitar el acceso a **servicios de soporte y seguridad**.
- Ofrecer **paquetes personalizados** para usuarios con altos cargos mensuales.
- Promover métodos de pago más confiables para disminuir fricción.

---

## 🛠️ Tecnologías

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- Jupyter Notebook
