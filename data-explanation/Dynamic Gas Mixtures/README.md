## Chemical    
### [Dynamic Gas Mixtures](https://archive.ics.uci.edu/ml/datasets/Gas+sensor+array+under+dynamic+gas+mixtures) 

다양한 concentration levels 하에, 2개의 gas mixtures에 노출된 16개의 chemical sensors 값을 기록한 시계열 데이터베이스이다.  
각 mixture에 대해서, 12시간 동안 continuous하게 sensor signals 를 얻었다.  

The data set was collected in a gas delivery platform facility at the ChemoSignals Laboratory in the BioCircuits Institute, University of California San Diego.   

![](https://img.shields.io/badge/sector-chemical-red.svg)
![](https://img.shields.io/badge/labeled-yes-blue.svg)
![](https://img.shields.io/badge/time--series-yes-blue.svg) ![](<https://img.shields.io/badge/simulation-yes-blue.svg>)    

#### Data Set Information  

- 데이터 요약  

Data Set Characteristics | Attribute Characteristics | Associated Tasks  
---- | ---- | ----  
Multivariate, Time-Series | Real | Classification, Regression   

Number of Instances | Number of Attributes | Number of Missing Values(NaN/not available)  
---- | ---- | ----  
4178504 | 19 | 0     


- 데이터 설명  
데이터는 2개의 파일로 구성되며, 각 파일은 each gas mixture에 대한 데이터를 포함한다.   
2의 gas mixtures = Ethylene and Methane in air / Ethylene and CO in air  
각 파일은 19개의 columns로 구성된다. = Time(seconds), Methane conc(or CO conc) (ppm), Ethylene conc (ppm), sensor readings (16 channels)  
Sensor의 순서 = TGS2602; TGS2602; TGS2600; TGS2600; TGS2610; TGS2610; TGS2620; TGS2620; TGS2602; TGS2602; TGS2600; TGS2600; TGS2610; TGS2610; TGS2620; TGS2620  


- 추가로 알아볼 것  
  클래스 개수(Ethylene and Methane/ Ethylene and CO)  
  NA값 존재하는지? -> jupyter 상에서 조사해 본 결과 없었음   

#### Paper  

1. [kaggle](<https://www.kaggle.com/uciml/gas-sensor-array-under-dynamic-gas-mixtures>)   

2. [A wireless sensor data-based coal mine gas monitoring algorithm with least squares support vector machines optimized by swarm intelligence techniques](<https://journals.sagepub.com/doi/full/10.1177/1550147718777440>)   

   중간에 gas sensor array drift 데이터를 가지고 실험한 부분 있음.  

   keywords: CNN, LSTM, LS-SVM   

#### Citation   

Citation of Fonollosa et al. 'Reservoir Computing compensates slow response of chemosensor arrays exposed to fast varying gas concentrations in continuous monitoring'; Sensors and Actuators B, 2015 is required.    


##### Data Download Link   
[https://archive.ics.uci.edu/ml/machine-learning-databases/00322/](https://archive.ics.uci.edu/ml/machine-learning-databases/00322/)   

데이터 용량(압축상태):   

352MB    