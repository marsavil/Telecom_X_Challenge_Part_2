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
<img width="686" height="471" alt="chur-tenure" src="https://github.com/user-attachments/assets/09536dc7-bc4b-4838-80c5-c399d5e52808" />


📌 **Conclusión:** Los clientes que cancelan suelen tener menor antigüedad.

---

### Gasto Total × Cancelación

También se exploró la relación entre el gasto total y la cancelación:

#### Boxplot:

![Total Charges vs Churn](images/boxplot_totalcharges_churn.png)

#### Scatter plot:

![Scatter Tenure vs Total Charges](images/scatter_totalcharges_tenure.png)

📌 **Conclusión:** La mayoría de los clientes que cancelan tienen poco tiempo en la compañía y bajo gasto total.

---

## 🤖 Modelos Entrenados

| Modelo             | Accuracy | Precision | Recall | F1 Score |
|--------------------|----------|-----------|--------|----------|
| Random Forest      | 0.8246   | 0.7059    | 0.7112 | 0.7085   |
| Gradient Boosting  | 0.8271   | 0.7231    | 0.7051 | 0.7140   |
| **Champion Model** | **0.8784** | **0.8248** | **0.6877** | **0.7500** |

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
