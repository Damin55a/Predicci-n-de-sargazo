**Predicción Espaciotemporal de Sargazo con Redes Neuronales**


Este proyecto tiene como objetivo desarrollar un modelo predictivo espaciotemporal para estimar la propagación del sargazo en áreas oceánicas y generar informacion ante su probable llegada a las costas de cancun utilizando datos satelitales del Sentinel-3 OLCI. Se pretende generar imágenes satelitales proyectadas (a 1 y 3 días en el futuro) que permitan comparar la situación real con la predicción del modelo.

Descripción
El proyecto se basa en el procesamiento y análisis de grandes volúmenes de datos provenientes del satélite Sentinel-3 OLCI, utilizando archivos en formato NetCDF para almacenar información histórica de varios años. Entre las variables más relevantes se encuentran:

AFAI: Indicador de presencia o concentración de sargazo.

Temperatura: Distribución térmica que puede influir en la dinámica del sargazo.

Velocidad del Viento: Influencia de las condiciones atmosféricas en la dispersión del sargazo.

Modelo de Predicción ConvLSTM2D:
La arquitectura del modelo integra varias capas ConvLSTM2D junto con capas de BatchNormalization y una capa final TimeDistributed con una Conv2D. Esto permite obtener predicciones multicanal que reflejan las condiciones espaciales y temporales.

El proceso incluye la carga, preprocesamiento y normalización de estos datos, seguido de la generación de secuencias temporales para modelar la dinámica en el tiempo. La arquitectura del modelo se basa en redes neuronales de tipo ConvLSTM2D, que combinan capas convolucionales (para extraer características espaciales) y LSTM (para capturar la evolución temporal). El modelo es capaz de predecir una secuencia de imágenes futuras que se pueden comparar visualmente con los datos reales.

