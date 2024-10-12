# Telecom Churn Prediction

## Descripción del Proyecto
Este proyecto tiene como objetivo predecir la **deserción de clientes** (churn) en una empresa de telecomunicaciones utilizando modelos de **Machine Learning**. Se han utilizado diferentes técnicas de preprocesamiento y reducción de dimensionalidad, así como varios algoritmos de clasificación para encontrar el mejor modelo predictivo.

## Problema de Negocio
La deserción de clientes es un problema clave para las empresas de telecomunicaciones. Poder predecir qué clientes probablemente cancelarán sus servicios es crucial para la retención y las estrategias de marketing. El modelo desarrollado permite a la empresa identificar clientes en riesgo y tomar medidas preventivas.

## Tecnologías Utilizadas
- **Python**: Para desarrollo y análisis de datos.
- **Pandas** y **NumPy**: Para la manipulación y análisis de datos.
- **Scikit-learn**: Para la implementación de modelos de machine learning.
- **Matplotlib** y **Seaborn**: Para la visualización de datos.

## Modelos y Métodos Utilizados

### 1. Modelo Base: Random Forest
Utilizamos el algoritmo Random Forest como nuestro modelo base, obteniendo una precisión de **78.01%**.

### 2. Reducción de Dimensionalidad
Se han aplicado diferentes técnicas de reducción de dimensionalidad para mejorar la eficiencia y el rendimiento del modelo:
- **Eliminación de Columnas**: Eliminamos columnas con datos irrelevantes, mejorando la precisión hasta **78.44%**.
- **SelectKBest**: Selecciona las mejores características basadas en el valor de Chi2.
- **RFE y RFECV**: Recursive Feature Elimination con y sin validación cruzada para seleccionar las características más importantes.
- **PCA**: Reducción de dimensionalidad con Análisis de Componentes Principales (PCA).

### 3. Métricas de Evaluación
Los modelos han sido evaluados utilizando las siguientes métricas:
- **Precisión**: Evaluamos qué tan exactas son nuestras predicciones.
- **Matriz de Confusión**: Para analizar la tasa de verdaderos positivos, falsos positivos, verdaderos negativos y falsos negativos.
- **Informe de Clasificación**: Proporciona precisión, recall y F1-score para cada clase.

| Técnica | Accuracy (%) |
|--------|--------------|
| Modelo Base (Random Forest) | 78.01 |
| Eliminación de Columnas | 78.44 |
| SelectKBest | 78.44 |
| RFE | 78.49 |
| RFECV | **78.77** |
| PCA | 78.15 |

### 4. Conclusiones
- El método RFECV (0.7877) presenta la mayor precisión, seguido de RFE (0.7849) y el diagrama de puntos (0.785). Esto indica que una eliminación meticulosa de características mediante validación cruzada puede optimizar el rendimiento del modelo
- La PCA (0.7815) es efectiva para la reducción de dimensionalidad y la optimización de la eficiencia computacional; sin embargo, su aplicación no mejora el rendimiento en relación con otros métodos disponibles
- La técnica SelectKBest y la eliminación de columnas con valores irrelevantes (0.7844) son opciones efectivas que no afectan negativamente el rendimiento, aunque tampoco contribuyen a una mejora notable
