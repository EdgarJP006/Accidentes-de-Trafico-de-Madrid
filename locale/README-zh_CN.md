[![en](https://img.shields.io/badge/lang-en-blue.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-en.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-pt.md)
[![es](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/README.md)
[![zh-CN](https://img.shields.io/badge/lang-zh--br-red.svg)](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/main/locale/README-zh_CN.md)

## 基于软计算的汽车事故分析系统的建议
## 1. 引言
本系统旨在分析 2019 年至 2023 年西班牙马德里的汽车事故。利用软计算技术，该系统将能够识别事故的模式和诱因，促进决策制定和安全措施的实施。
## 2. 变量选择
该模型基于特定时期，如需使用其他年份的数据集，请在以下网址搜索： https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default
输入变量 ：

- date : 事故发生日期
- time：事故发生时间
- location：事故发生地点
- district_code : 地区代码
- district : 地区
- type_accident : 事故类型
- weather_status : 天气状况
- type_vehicle : 车辆类型
- type_person : 人的类型
- age_range : 年龄范围
- coordenada_x_utm : X 坐标（UTM） （或
- coordenada_y_utm : UTM Y 坐标
- positive_alcohol：酒精检测结果呈阳性。
- positive_drug：毒品阳性结果
输出变量 ： \
- 事故概率 考虑到输入变量，估计特定地点发生事故的概率。\
- 事故热点：根据计算出的事故概率，确定事故发生概率较高的区域。\
## 3. 分析模型构建
该系统使用决策树模型来分析事故数据。这种算法易于解释，既可处理分类变量，也可处理连续变量，因此适用于识别交通事故的模式和诱因。
### 3.1 模型实现
决策树模型使用 Scikit-learn 等 Python 库实现，这些库有助于创建和评估决策树模型。
### 3.2. 分析过程概要
分析过程分为以下几个阶段：
数据收集和准备：从 Dirección General de Tráfico (DGT) 或 Instituto Nacional de Estadística (INE) 等来源获取事故数据。
2.	清理和预处理：对数据进行清理和预处理，以消除缺失值，将分类变量转换为数值变量，并对数据进行归一化处理。
3.	模型训练：在预处理数据上训练决策树模型。
4.	模型评估：使用准确性、完整性和 F1 分数等指标评估模型的性能。
5.	预测：利用训练好的模型预测事故概率和事故热点。
### 3.3 结果与分析
该系统生成两种结果： \
- 事故概率图： 该地图显示了马德里不同区域发生事故的概率，直观显示了风险最高的区域。\
- 关键点地图：该地图可识别事故最集中的区域，以便当局采取措施改善道路安全。
### 应用实例
### 4.1. 实际例子
该系统适用于西班牙马德里 2019 年至 2023 年的车祸数据。使用的是真实事故数据集，包括日期、时间、地点、事故类型、天气条件、车辆类型和涉事人员类型等信息。
### 4.2 结果可视化
![本图显示按区域划分的预测事故](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/2c7103bf227e00fe7e68e58e39f89864ec0901bc/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen3.png) 

1717399581495
本图显示了按区域划分的事故预测结果。由于该算法是按坐标进行预测的，因此选择以点的形式显示，以聚集其周围可能发生的事故。
 ![This image shows the predicted features per zone](https://raw.githubusercontent.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/main/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen5.png)  
 
1717399594301

该应用程序还允许放大和缩小，以更详细地显示最有可能发生车祸的地方。这有助于为人们规划出更安全的路线，尤其是对于不太熟悉马德里街道动向的游客而言。
### 5.
我们利用软计算开发了一套完整的系统，用于分析西班牙马德里的车祸。该系统包括决策树模型的实施、数据清理和准备，以及用于展示结果的网络界面的开发。
## 研究的局限性
本研究存在一些局限性： \
- 数据可用性：可用数据的质量和数量可能会影响模型的准确性。\
- 可推广性：模型可能无法推广到具有不同特征的其他城市或地区。\
- 未考虑的因素：该模型未考虑可能导致撞车的所有因素，如驾驶员疲劳或车辆状况。
## 未来工作建议
- 扩大数据集：纳入更多来自不同城市或地区的交通事故数据，以提高模型的通用性。
- 纳入新因素：考虑可能影响碰撞概率的其他因素，如车辆状况或驾驶员疲劳。
- 开发警告系统：实施警告系统，通知用户碰撞风险增加的区域。
