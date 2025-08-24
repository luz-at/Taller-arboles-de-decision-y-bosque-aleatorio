# Análisis de Abandono de Clientes - Árboles de Decisión y Bosque Aleatorio

## Descripción del proyecto

Este proyecto analiza los factores que influyen en el abandono de clientes en una empresa de telecomunicaciones utilizando técnicas de Machine Learning. Se implementan y comparan dos modelos: **Árbol de Decisión** y **Bosque Aleatorio** para predecir qué clientes tienen mayor probabilidad de abandonar la compañía.

## Dataset

- **Fuente**: Telecom Customer Churn (2023) - Kaggle
- **URL**: https://www.kaggle.com/datasets/yeanzc/telco-customer-churn-ibm-dataset
- **Descripción**: Datos de clientes de una empresa de telecomunicaciones con información demográfica, servicios contratados y comportamiento de abandono

## Estructura del análisis

### 1. Carga y limpieza de datos
- Importación del dataset desde archivo Excel
- Traducción de columnas al español
- Eliminación de columnas irrelevantes
- Tratamiento de valores nulos y duplicados
- Conversión de tipos de datos

### 2. Análisis exploratorio
- Estadísticas descriptivas
- Análisis de distribución de la variable objetivo
- Identificación de desbalance de clases

### 3. Análisis de frecuencias
- Visualización de patrones de abandono por:
  - Tipo de servicio de internet
  - Tipo de contrato
  - Dependientes
  - Antigüedad del cliente

### 4. Preprocesamiento
- **Balanceo de clases**: Técnica de submuestreo (undersampling)
- **Codificación de variables**:
  - One-Hot Encoding para variables categóricas
  - Ordinal Encoding para variables con orden (tipo de contrato)
- División train/test (70/30)

### 5. Entrenamiento de modelos

#### Árbol de decisión
- Parámetros: `max_depth=3`, `class_weight='balanced'`
- Accuracy Train: Variable según datos
- Accuracy Test: Variable según datos

#### Bosque aleatorio
- Parámetros: `n_estimators=40`, `max_depth=5`, `class_weight='balanced'`

### 6. Evaluación y validación
- Matrices de confusión
- Métricas de clasificación (Precision, Recall, F1-Score)
- Análisis de importancia de características
- Pruebas con nuevos clientes

## Principales hallazgos

### Factores clave de abandono

1. **Tipo de contrato** (Factor más importante)
   - Clientes con contrato "Month-to-month" abandonan más
   - Contratos de largo plazo retienen mejor a los clientes

2. **Servicio de internet**
   - Clientes con "Fiber optic" muestran mayor tasa de abandono

3. **Antigüedad**
   - Clientes más nuevos tienen mayor probabilidad de abandonar

4. **Dependientes**
   - Clientes sin dependientes abandonan más frecuentemente

## Contribuciones
Cindy Sanchez,
Cindy Aparicio,
Estefany Acuña,
Yuranis Fernandez,
Eliana Fernandez y
Luz Atencio.
