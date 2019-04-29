# Appliances energy prediction Data Set

[data](https://archive.ics.uci.edu/ml/datasets/Appliances+energy+prediction)

11.4MB

Experimental data used to create regression models of appliance energy use in a low energy building

 ![](https://img.shields.io/badge/sector-power-skyblue.svg)

 ![](https://img.shields.io/badge/label-yes-blue.svg)

 ![](https://img.shields.io/badge/time--series-yes-blue.svg)

 ![](https://img.shields.io/badge/house environment-gray.svg)

#### Data Set Information

| Data Set Characteristics  | Attribute Characteristics | Associated Tasks |
| ------------------------- | ------------------------- | ---------------- |
| Multivariate, Time-Series | Real                      | Regression       |

| Number of Instances | Number of Attributes |      |      |
| ------------------- | -------------------- | ---- | ---- |
| 19735               | 29                   |      |      |

The data set is at 10 min for about 4.5 months. The house temperature and humidity conditions were monitored with a ZigBee wireless sensor network. Each wireless node transmitted the temperature and humidity conditions around 3.3 min. Then, the wireless data was averaged for 10 minutes periods. **The energy data was logged every 10 minutes with m-bus energy meters.** Weather from the nearest airport weather station (Chievres Airport, Belgium) was downloaded from a public data set from Reliable Prognosis (rp5.ru), and merged together with the experimental data sets using the date and time column. 

#### Variables

date : time year-month-day hour:minute:second(10분 단위로 기록)  
Appliances : energy use in Wh(종속변수)  
lights : energy use of light fixtures in the house in Wh  
T1 : Temperature in kitchen area, in Celsius  
RH_1 : Humidity in kitchen area, in %  
T2 : Temperature in living room area, in Celsius  
RH_2 : Humidity in living room area, in %  
T3 : Temperature in laundry room area  
RH_3 : Humidity in laundry room area, in %  
T4 : Temperature in office room, in Celsius  
RH_4 : Humidity in office room, in %  
T5 : Temperature in bathroom, in Celsius  
RH_5 : Humidity in bathroom, in %  
T6 : Temperature outside the building (north side), in Celsius  
RH_6 : Humidity outside the building (north side), in %  
T7 : Temperature in ironing room , in Celsius  
RH_7 : Humidity in ironing room, in %  
T8 : Temperature in teenager room 2, in Celsius  
RH_8 : Humidity in teenager room 2, in %  
T9 : Temperature in parents room, in Celsius  
RH_9 : Humidity in parents room, in %  
T_out : Temperature outside (from Chievres weather station), in Celsius  
press_mm_hg : Pressure (from Chievres weather station), in mm Hg  
RH_out : Humidity outside (from Chievres weather station), in %  
Windspeed : (from Chievres weather station), in m/s  
Visibility : (from Chievres weather station), in km  
Tdewpoint : (from Chievres weather station), Â°C  
rv1 : Random variable 1, nondimensional  
rv2 : Random variable 2, nondimensional  

#### Paper

[Data driven prediction models of energy use of appliances in a low-energy house](https://www.sciencedirect.com/science/article/pii/S0378778816308970?via%3Dihub)

**Highlights**

- The appliances [energy consumption](https://www.sciencedirect.com/topics/earth-and-planetary-sciences/energy-consumption) prediction in a low energy house has been studied.

- Weather data from a nearby station was found to improve the prediction.

- Pressure, [air temperature](https://www.sciencedirect.com/topics/engineering/air-temperature) and wind speed are important parameters in the prediction.

- Data from a WSN that [measures temperature](https://www.sciencedirect.com/topics/engineering/measure-temperature) and humidity increase the pred. -accuracy.

- From the WSN, the kitchen, laundry and living room data ranked high in importance.

**Abstract**

이 논문은 appliances의 에너지 사용에 대해 data-driven 예측 모델을 제시하고 이에 대해 설명함. 사용된 데이터에는 무선 네트워크로부터 온도, 습도 센서 측정, 인근 공항 역의 날씨 및 조명 기구의 에너지 사용 기록이 포함된다. 

The paper discusses data filtering to remove non-predictive parameters and feature ranking. Four statistical models were trained with repeated cross validation and evaluated in a testing set: (a) multiple linear regression, (b) support vector machine with radial kernel, (c) random forest and (d) gradient boosting machines (GBM). 

The best model (GBM) was able to explain 97% of the variance (*R*2) in the training set and with 57% in the testing set when using all the predictors. **From the wireless network, the data from the kitchen, laundry and living room were ranked the highest in importance for the energy prediction.** The prediction models with only the weather data, selected the atmospheric pressure (which is correlated to wind speed) as the most relevant weather data variable in the prediction. **Therefore, atmospheric pressure may be important to include in energy prediction models and for building performance modeling.**