# Challenge 2 (Parte 2): Modelo Predictivo de Churn de Clientes
Este repositorio contiene la solución a la segunda parte del desafío de Data Science de Alura Latam. El proyecto se enfoca en la construcción de un pipeline de Machine Learning para predecir la probabilidad de cancelación de clientes (Churn) en la empresa ficticia "Telecom X", utilizando los datos previamente procesados en la Parte 1 (ETL).
______________________________________________________
🎯 Misión del Proyecto
Tras un exitoso análisis exploratorio en la Parte 1, la misión en esta segunda fase fue avanzar hacia una solución predictiva. El objetivo principal fue desarrollar, entrenar y evaluar modelos de Machine Learning capaces de identificar a los clientes con mayor riesgo de cancelar su servicio, permitiendo a la empresa anticiparse al problema y aplicar estrategias de retención de manera proactiva.
_________________________________________________
🧠 Objetivos del Desafío
Preprocesamiento de Datos: Preparar los datos limpios para el modelado, aplicando técnicas de codificación (One-Hot Encoding), manejo de valores nulos (Imputación) y estandarización.

Construcción de Modelos: Entrenar y comparar al menos dos modelos de clasificación diferentes (Random Forest y Regresión Logística).

Evaluación de Modelos: Evaluar el rendimiento de los modelos utilizando un conjunto de métricas estándar (Accuracy, Precision, Recall, F1-Score, Matriz de Confusión).

Interpretación de Resultados: Analizar la importancia de las variables para identificar los factores más influyentes en la predicción del Churn.

Comunicación Estratégica: Sintetizar los hallazgos en un informe ejecutivo con conclusiones y recomendaciones de negocio.
__________________________________________________
🛠️ Tecnologías Utilizadas
Python 3

Pandas: Para la carga y manipulación final de los datos.

Scikit-learn: Para el preprocesamiento de datos (SimpleImputer, StandardScaler), la división de datos (train_test_split), el entrenamiento de modelos (RandomForestClassifier, LogisticRegression) y la evaluación de métricas.

Matplotlib y Seaborn: Para la visualización de datos, incluyendo la matriz de confusión y el gráfico de importancia de variables.

Google Colab / Jupyter Notebook: Como entorno de desarrollo interactivo.
__________________________________________________
🚀 Pipeline de Machine Learning
El proyecto siguió un flujo de trabajo estructurado para la construcción del pipeline predictivo:

Carga de Datos: Se cargó el dataset limpio y procesado generado en la Parte 1.

Preprocesamiento Final: Se eliminaron columnas irrelevantes (customerID) y se aplicó One-Hot Encoding para transformar todas las variables a un formato numérico.

División de Datos: El dataset se dividió en conjuntos de entrenamiento (80%) y prueba (20%).

Manejo de Nulos y Estandarización: Se aplicó imputación por la mediana para rellenar valores NaN y se estandarizaron los datos para el modelo de Regresión Logística.

Entrenamiento y Evaluación: Se entrenaron y evaluaron los dos modelos propuestos, comparando sus resultados para seleccionar el de mejor rendimiento.

Análisis de Importancia: Se extrajeron y visualizaron las características más importantes del modelo Random Forest para entender los impulsores del Churn.
___________________________________________________________
📊 Informe Final: Conclusiones del Modelo Predictivo
1. Resumen Ejecutivo
Este informe presenta los resultados del pipeline de Machine Learning desarrollado para predecir el Churn de clientes. El objetivo fue construir un modelo robusto y, a su vez, interpretar sus resultados para extraer insights estratégicos que guíen las futuras acciones de retención de Telecom X.

2. Resultados y Selección del Modelo
Se entrenaron dos modelos: Random Forest y Regresión Logística. Aunque ambos mostraron un buen rendimiento general (cercano al 80% de exactitud), la Regresión Logística se seleccionó como el modelo superior debido a su mayor capacidad para identificar correctamente a los clientes que realmente cancelaron (Recall del 54% vs. 46% del Random Forest). Esta métrica es crucial para minimizar la cantidad de clientes en riesgo que no son detectados.

3. Factores Clave en la Predicción de Churn
El análisis de la importancia de las variables reveló los siguientes factores como los más determinantes para predecir la cancelación:

Antigüedad del Cliente (customer.tenure): Es el factor protector más fuerte. A mayor antigüedad, menor es la probabilidad de cancelación.

Gasto Mensual y Total (Charges.Monthly y Charges.Total): Una baja antigüedad (y por ende, bajo gasto total) combinada con una factura mensual elevada son los principales indicadores de riesgo.

Tipo de Contrato: La ausencia de contratos a largo plazo es un impulsor clave del Churn.

Servicios de Soporte: La falta de servicios de valor añadido como internet.TechSupport y internet.OnlineSecurity aumenta el riesgo de abandono.

4. Recomendaciones Estratégicas
Basado en las conclusiones del modelo, se proponen las siguientes acciones:

Programa de Fidelización Proactivo: Enfocar los esfuerzos de retención en clientes con menos de 10 meses de antigüedad y facturas mensuales altas, ofreciéndoles beneficios o revisiones de su plan.

Incentivar Contratos a Largo Plazo: Crear campañas para migrar a clientes de contratos mensuales a planes anuales, destacando los ahorros y la estabilidad.

Fortalecer la Oferta de Valor: Promocionar activamente los servicios de soporte y seguridad, ya que el modelo demuestra que son factores clave para la retención.
