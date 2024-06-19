[![en](https://img.shields.io/badge/lang-en-blue.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-en.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-pt.md)
[![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/README.md)
[![zh-CN](https://img.shields.io/badge/lang-zh--br-red.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-zh_CN.md)

# Proposal for a Soft Computing Based System for Automobile Accident Analysis
## 1. Introduction
The proposed system aims to analyze automobile accidents in Madrid, Spain, from 2019 to 2023. Using soft computing techniques, the system will allow identifying patterns and contributing factors to accidents, facilitating decision making and implementation of safety measures.
## 2. Variable Selection
The model is based on a specific period, to use other years search the datasets in: https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default
Input Variables :

- date : Date of accident
- time : Time of accident
- location : Location of the accident
- district_code : District code
- district : district
- accident_type : Type of accident \
- weather_status : weather condition \
- type_vehicle : Type of vehicle \
- type_person : Type of person \
- age_range : Age range
- coordenada_x_utm : X coordinate in UTM \
- coordenada_y_utm : Y coordinate in UTM \
- positive_alcohol : Positive result for alcohol \
- positive_drug : Positive result for drugs \
Output Variables : \
- Accident probability : Estimation of the probability of an accident occurring at a specific location, considering the input variables. \
- Accident hotspots : Identification of areas with higher probability of accidents, based on the calculated accident probability. \
## 3. Analysis Model Construction
The system uses a Decision Tree model to analyze the accident data. This algorithm is suitable for identifying patterns and contributing factors in traffic accidents, as it is easy to interpret and can handle both categorical and continuous variables.
### Model Implementation
The Decision Trees model is implemented using Python libraries such as Scikit-learn, which facilitates the creation and evaluation of decision tree models.
### 3.2. Outline of the Analysis Process
The analysis process is divided into the following stages:
1. Data Collection and Preparation : Accident data are obtained from sources such as the Dirección General de Tráfico (DGT) or the Instituto Nacional de Estadística (INE).
2.	Cleaning and Preprocessing : The data are cleaned and preprocessed to eliminate missing values, convert categorical variables to numerical and normalize the data.
3.	Model Training : The Decision Trees model is trained with the preprocessed data.
4.	Model Evaluation : The model performance is evaluated using metrics such as accuracy, completeness and F1 score.
5.	Prediction : The trained model is used to predict accident probability and accident hotspots.
### 3.3. Results and Analysis
The system generates two types of results: \
- Accident Probability Map : This map shows the accident probability in different areas of Madrid, visualizing the areas of highest risk. \
- Critical Points Map : This map identifies the areas with the highest concentration of accidents, allowing authorities to take measures to improve road safety.
## 4. Application Examples
### 4.1. Practical Example
The system is applied to automobile accident data in Madrid, Spain, from 2019 to 2023. A real accident data set is used, including information on date, time, location, type of accident, weather conditions, type of vehicle, and type of person involved.
### 4.2. Visualization of Results
![This image shows the predicted accidents by zone](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/2c7103bf227e00fe7e68e58e39f89864ec0901bc/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen3.png) 

1717399581495
This image shows the predicted accidents by zone. As the algorithm predicts by coordinate, it was chosen to display them in points that gather the possible accidents around them.
 This image shows the predicted features per zone](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/2c7103bf227e00fe7e68e58e39f89864ec0901bc/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen5.png) 


1717399594301
The application also allows to zoom in and show more details as to the most possible places where car accidents may occur. This could help to map out safer routes for people, especially for tourists who may be less familiar with the movements of the streets of Madrid.
## 5. Conclusion
We have developed a complete system for the analysis of automobile accidents in Madrid, Spain, using soft computing. The system includes the implementation of a Decision Tree model, data cleaning and preparation, and the development of a web interface for the presentation of results.
## 6. Limitations of the Study
The study has some limitations: \
- Data Availability : The quality and quantity of available data may affect the accuracy of the model. \
- Generalizability : The model may not be generalizable to other cities or regions with different characteristics. \
- Factors Not Considered: The model does not consider all factors that may contribute to crashes, such as driver fatigue or vehicle condition.
## 7. Proposals for Future Work
- Expand the Data Set : Include more crash data from different cities or regions to improve the generalizability of the model.
- Incorporate New Factors : Consider additional factors that may influence crash probability, such as vehicle condition or driver fatigue.
- Develop a Warning System : Implement a warning system that notifies users of areas of increased crash risk.

