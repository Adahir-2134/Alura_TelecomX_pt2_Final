# Análisis de Cancelación de Clientes (Churn) - Telecom X

![Badge en Desarrollo](https://img.shields.io/badge/Estado-Completado-green) 
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)

Proyecto de análisis predictivo para identificar factores de cancelación de clientes y proponer estrategias de retención efectivas.

## 📌 Objetivo
Identificar los factores que más influyen en la cancelación de clientes (churn) y desarrollar estrategias de retención basadas en análisis de datos para Telecom X.

## 📊 Datos
- **Fuente**: Dataset interno de clientes de Telecom X
- **Variables clave**: 
  - `customer_tenure` (tiempo como cliente)
  - `account_Charges_Total` (gasto total)
  - `MonthlyCharges` (cargos mensuales)
  - `account_Contract` (tipo de contrato)
  - Entre otras variables demográficas y de servicio

## 🔍 Metodología

### 1. Preprocesamiento de Datos
- Eliminación de columnas no relevantes (`customerID`, `Cuentas_Diarias`)
- Codificación de variables categóricas (One-Hot Encoding)
- Estandarización de variables numéricas (`StandardScaler`)
- Manejo de valores nulos

### 2. Análisis Exploratorio (EDA)
- Matriz de correlación entre variables
- Visualización de relaciones clave:
  - Boxplots para `customer_tenure` vs `Churn`
  - `account_Charges_Total` vs `Churn`
- Análisis de balance de clases

### 3. Modelado Predictivo
- **Partición de datos**: 80% entrenamiento - 20% prueba
- **Algoritmos implementados**:
  - Regresión Logística
  - Random Forest Classifier
- **Métricas de evaluación**:
  - Exactitud
  - Precisión
  - Recall
  - F1-score
  - Matriz de confusión

## 📈 Resultados

### Rendimiento de Modelos

| Métrica         | Regresión Logística | Random Forest |
|-----------------|---------------------|---------------|
| Exactitud       | 0.794               | 0.789         |
| Precisión       | 0.637               | 0.638         |
| Recall          | 0.521               | 0.471         |
| F1-score        | 0.574               | 0.542         |

### Factores Clave de Churn
1. **Tiempo de contrato**: Clientes con menor antigüedad más propensos a cancelar
2. **Gasto total**: Menor gasto asociado a mayor probabilidad de churn
3. **Tipo de servicio**: Clientes con fibra óptica muestran mayor tendencia a cancelar
4. **Método de pago**: Pago electrónico asociado a mayor churn
5. **Tipo de contrato**: Contratos de 2 años con menor tasa de cancelación

## 🚀 Estrategias de Retención Propuestas

- **Programas para clientes nuevos**: Incentivos durante primeros meses
- **Análisis de bajo gasto**: Paquetes personalizados para clientes con bajo consumo
- **Mejora en servicio de fibra óptica**: Investigar causas de insatisfacción
- **Optimización de pagos electrónicos**: Mejorar experiencia de pago
- **Promoción de contratos largos**: Beneficios para contratos de 2 años
- **Segmentación proactiva**: Identificación temprana de clientes en riesgo

## 🛠 Tecnologías Utilizadas
- Python 3.8+
- Bibliotecas:
  - Pandas, NumPy (análisis de datos)
  - Scikit-learn (modelado)
  - Matplotlib, Seaborn (visualización)
- Jupyter Notebooks

## 📂 Estructura del Proyecto
