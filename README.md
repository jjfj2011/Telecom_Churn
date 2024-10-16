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
- **Eliminación de Columnas**: Eliminamos columnas con datos irrelevantes, mejorando la precisión hasta **77.15%**.
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
| Eliminación de Columnas | 77.15 |
| SelectKBest | 73.16 |
| RFE | 75.44 |
| RFECV | **77.25** |
| PCA | **77.25** |

### 4. Conclusiones
- **Rendimiento General del Modelo:** El modelo Random Forest inicial sin reducción de dimensionalidad (con todas las características) alcanzó la mayor precisión (78.01%). Sin embargo, la reducción de dimensionalidad y los métodos de selección de características, como RFECV y PCA, lograron resultados cercanos (77.25%), lo que sugiere que la reducción de características puede ser útil sin comprometer demasiado el rendimiento del modelo
- **Impacto de la Reducción de Características:** Los métodos de selección como SelectKBest tuvieron un impacto negativo en el rendimiento, mientras que RFE y RFECV mostraron mejoras al seleccionar un subconjunto de características representativas. Esto resalta la importancia de utilizar métodos avanzados que tomen en cuenta la interacción entre variables.
- **Selección de Variables Relevantes:** Características relacionadas con el tiempo de servicio, cobros mensuales, y algunos servicios de internet fueron recurrentemente seleccionadas como importantes en la predicción del churn. Estas características son críticas para entender el comportamiento de los clientes y deberían ser priorizadas en futuras optimizaciones del modelo.
