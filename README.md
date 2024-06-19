[![en](https://img.shields.io/badge/lang-en-blue.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-en.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-pt.md)
[![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/README.md)
[![zh-CN](https://img.shields.io/badge/lang-zh--br-red.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-zh_CN.md)


# Propuesta de Sistema para el Análisis de Accidentes Automovilísticos Basado en Soft Computing
## 1. Introducción
El sistema propuesto tiene como objetivo analizar los accidentes automovilísticos en Madrid, España, desde 2019 hasta 2023. Utilizando técnicas de soft computing, el sistema permitirá identificar patrones y factores contribuyentes a los accidentes, facilitando la toma de decisiones y la implementación de medidas de seguridad.
## 2. Selección de Variables
El modelo está basado en un periodo en especifico, para usar otros años busar los datasets en: https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default
Variables de Entrada :

•	fecha : Fecha del accidente \
•	hora : Hora del accidente \
•	localizacion : Localización del accidente \
•	cod_distrito : Código del distrito \
•	distrito : Distrito \
•	tipo_accidente : Tipo de accidente \
•	estado_meteorológico : Estado meteorológico \
•	tipo_vehiculo : Tipo de vehículo \
•	tipo_persona : Tipo de persona \
•	rango_edad : Rango de edad \
•	coordenada_x_utm : Coordenada X en UTM \
•	coordenada_y_utm : Coordenada Y en UTM \
•	positiva_alcohol : Resultado positivo para alcohol \
•	positiva_droga : Resultado positivo para drogas \
Variables de Salida : \
•	Probabilidad de accidente : Estimación de la probabilidad de que ocurra un accidente en una ubicación específica, considerando las variables de entrada. \
•	Puntos críticos de accidentes : Identificación de zonas con mayor probabilidad de accidentes, basados en la probabilidad de accidente calculada. \
## 3. Construcción del Modelo de Análisis
El sistema utiliza un modelo de Árboles de Decisión para analizar los datos de accidentes. Este algoritmo es adecuado para identificar patrones y factores contribuyentes en los accidentes de tráfico, ya que es fácil de interpretar y puede manejar tanto variables categóricas como continuas.
### 3.1. Implementación del Modelo
El modelo de Árboles de Decisión se implementa utilizando librerías de Python como Scikit-learn, que facilita la creación y evaluación de modelos de árboles de decisión.
### 3.2. Esquema del Proceso de Análisis
El proceso de análisis se divide en las siguientes etapas:
1.	Obtención y Preparación de Datos : Los datos de accidentes se obtienen de fuentes como la Dirección General de Tráfico (DGT) o el Instituto Nacional de Estadística (INE).
2.	Limpieza y Preprocesamiento : Los datos se limpian y preprocesan para eliminar valores faltantes, convertir variables categóricas a numéricas y normalizar los datos.
3.	Entrenamiento del Modelo : El modelo de Árboles de Decisión se entrena con los datos preprocesados.
4.	Evaluación del Modelo : Se evalúa el rendimiento del modelo utilizando métricas como la precisión, la exhaustividad y la puntuación F1.
5.	Predicción : El modelo entrenado se utiliza para predecir la probabilidad de accidente y los puntos críticos de accidentes.
### 3.3. Resultados y Análisis
El sistema genera dos tipos de resultados: \
•	Mapa de Probabilidad de Accidentes : Este mapa muestra la probabilidad de accidente en diferentes zonas de Madrid, visualizando las áreas de mayor riesgo. \
•	Mapa de Puntos Críticos : Este mapa identifica las zonas con mayor concentración de accidentes, permitiendo a las autoridades tomar medidas para mejorar la seguridad vial.
## 4. Ejemplos de Aplicación
### 4.1. Ejemplo Práctico
El sistema se aplica a los datos de accidentes automovilísticos en Madrid, España, desde 2019 hasta 2023. Se utiliza un conjunto de datos de accidentes reales, incluyendo información sobre la fecha, hora, ubicación, tipo de accidente, condiciones climáticas, tipo de vehículo y tipo de persona involucrada.
### 4.2. Visualización de Resultados
![Esta imagen muestra los accidentes predichos por zona](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/2c7103bf227e00fe7e68e58e39f89864ec0901bc/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen3.png) 

1717399581495
Esta imagen muestra los accidentes predichos por zona. Como el algoritmo predice por coordenada, se optó por mostrarlos en puntos que juntan los posibles accidentes a su alrededor.
 ![Esta imagen muestra los accidentes predichos por zona](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/2c7103bf227e00fe7e68e58e39f89864ec0901bc/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen5.png) 
 
1717399594301
La aplicación también permite hacer zoom y mostrar más detalles en cuanto a los lugares más posibles en los que pueden haber accidentes automovilísticos. Esto podría ayudar a trazar rutas más seguras para las personas, sobre todo para los turistas que pueden conocer menos los movimientos de las calles de Madrid.
## 5. Conclusión
Hemos desarrollado un sistema completo para el análisis de accidentes automovilísticos en Madrid, España, utilizando soft computing. El sistema incluye la implementación de un modelo de Árboles de Decisión, la limpieza y preparación de datos, y el desarrollo de una interfaz web para la presentación de resultados.
## 6. Limitaciones del Estudio
El estudio tiene algunas limitaciones: \
•	Disponibilidad de Datos : La calidad y cantidad de datos disponibles pueden afectar la precisión del modelo. \
•	Generalización : El modelo puede no ser generalizable a otras ciudades o regiones con diferentes características. \
•	Factores No Considerados : El modelo no considera todos los factores que pueden contribuir a los accidentes, como la fatiga del conductor o el estado del vehículo.
## 7. Propuestas para Trabajo Futuro
•	Ampliar el Conjunto de Datos : Incluir más datos de accidentes de diferentes ciudades o regiones para mejorar la generalización del modelo.
•	Incorporar Nuevos Factores : Considerar factores adicionales que pueden influir en la probabilidad de accidente, como el estado del vehículo o la fatiga del conductor.
•	Desarrollar un Sistema de Alerta : Implementar un sistema de alerta que notifique a los usuarios sobre las zonas de mayor riesgo de accidentes.

