# Resultados de Modelos de Clasificación

Se han evaluado varios modelos para la predicción de la variable `Churn`. A continuación se presentan los resultados obtenidos para cada uno de los modelos y un análisis comparativo de su desempeño.

## Resumen de las Métricas de Evaluación

| **Modelo**                   | **Precisión** | **Recall** | **F1-Score** | **AUC-ROC** | **Accuracy** |
|------------------------------|---------------|------------|--------------|-------------|--------------|
| **AdaBoost**                  | 0.9970        | 0.9692     | 0.9829       | 0.9945      | 0.9809       |
| **XGBoost**                   | 0.9997        | 0.9848     | 0.9922       | 0.9975      | 0.9912       |
| **Random Forest**             | 1.0000        | 0.9806     | 0.9902       | 0.9969      | 0.9890       |
| **Logistic Regression**       | 0.9225        | 0.8865     | 0.9041       | 0.9586      | 0.8934       |
| **K-Nearest Neighbors (KNN)** | 0.9919        | 0.9110     | 0.9497       | 0.9778      | 0.9453       |

## Análisis Comparativo

### 1. **Precisión**:
   - **XGBoost** tiene la mayor precisión (0.9997), seguida por **Random Forest** (1.0000) y **AdaBoost** (0.9970).
   - **Random Forest** tiene una precisión perfecta de 1.0000, lo que sugiere que no hay falsos positivos.

### 2. **Recall**:
   - **XGBoost** tiene el mejor **recall** (0.9848), seguido por **Random Forest** (0.9806).
   - El **recall** mide la capacidad del modelo para identificar correctamente los casos positivos (minimizar falsos negativos).

### 3. **F1-Score**:
   - **XGBoost** tiene el mejor **F1-Score** (0.9922), seguido por **Random Forest** (0.9902).
   - El **F1-Score** es una medida combinada de precisión y recall, lo que hace que sea ideal para situaciones de clasificación desbalanceada.

### 4. **AUC-ROC**:
   - **XGBoost** tiene el mejor **AUC-ROC** (0.9975), seguido por **AdaBoost** (0.9945).
   - Un AUC-ROC cercano a 1.0 indica un excelente desempeño en la clasificación.

### 5. **Accuracy**:
   - **XGBoost** (0.9912) y **Random Forest** (0.9890) tienen las mejores tasas de **accuracy**.
   - La **accuracy** refleja la capacidad general del modelo para hacer predicciones correctas.

## Conclusión y Recomendación

1. **XGBoost** es el modelo más adecuado para esta tarea, ya que tiene el mejor desempeño en términos de **precision**, **recall**, **F1-Score** y **AUC-ROC**.
   
2. **Random Forest** es una excelente opción con una **precision perfecta (1.0000)** y un alto **AUC-ROC**. Sin embargo, su **recall** es ligeramente inferior al de **XGBoost**.

3. **AdaBoost** tiene un buen desempeño, pero **XGBoost** y **Random Forest** le superan en varias métricas clave.

### Recomendación Final:
- **XGBoost** es la opción más equilibrada, especialmente si se necesita optimizar tanto la precisión como el recall. Es ideal para mantener una alta tasa de clasificación correcta y minimizar tanto falsos positivos como falsos negativos.
