## Chemical
### [Gas Sensor Array Drift](https://archive.ics.uci.edu/ml/datasets/Gas+Sensor+Array+Drift+Dataset+at+Different+Concentrations)  

This archive contains 13910 measurements from 16 chemical sensors exposed to 6 different gases at various concentration levels. These measurements are utilized in simulations for drift compensation in a __discrimination task of six gases at various levels of concentrations.__  
The dataset was gathered during the period of January 2008 to February 2011 (36 months).  
This data is divided into 10 batch files with a '.dat' extension.  

The dataset was gathered during the period of January 2008 to February 2011 (36 months) in a gas delivery platform facility situated at the ChemoSignals Laboratory in the BioCircuits Institute, University of California San Diego.    

![](https://img.shields.io/badge/sector-chemical-red.svg)
![](https://img.shields.io/badge/labeled-yes-blue.svg)
![](https://img.shields.io/badge/time--series-yes-blue.svg)![](<https://img.shields.io/badge/simulation-yes-blue.svg>)       


- 데이터 요약  

Data Set Characteristics | Attribute Characteristics | Associated Tasks  
---- | ---- | ----  
Multivariate, Time-Series | Real | Classification, Regression, Clustering, Causa  

Number of Instances | Number of Attributes | Number of Missing Values(N/A) | Number of Classes
---- | ---- | ---- | ----    
13910 | 129 | 0 | 6            

> 첫번째 nomial 변수는 class(target) 을 의미하는 변수이다. 나머지 128개 변수는 모두 numeric type 이다.   
> data file 내에 training data 와 test data 가 구분되어 있지 않다.  

- 6개의 class인 gas 이름과, 각 gas의 interval of concentration levels  

Name of gas| Ammonia | Acetaldehyde | Acetone | Ethylene | Ethanol | Toluene  
---- | ---- | ---- | ---- | ---- | ---- | ----   
ppmv | (50,1000) | (5,500) | (12,1000) | (10,300) | (10,600) | (10,100)  


- 클래스 개수  

| 1    | 2    | 3    | 4    | 5    | 6    |
| ---- | ---- | ---- | ---- | ---- | ---- |
| 2565 | 2926 | 1641 | 1936 | 3009 | 1833 |

- Attributes 설명    

  why 128-element feature vector per measurement?   

  MOX gas sensors typically describe a monotonically smooth change in the conductance of the sensing

  layer due to the adsorption/desorption reaction processes of the exposed chemical analyte substance.

  We represented each time series with an aggregate of __eight features__ reflecting the sensor response.

  In particular, we considered two distinct types of features in the creation of this dataset: __two steady-state features__ and __six features__ reflecting the sensor dynamics.  

  The steady-state features include the amplitude of the resistance change, and its normalized value.

  The transient features were extracted based on the exponential moving average (EMA) to reflect the

  sensor dynamics of the increasing/decaying transient portion of the sensor responses. The EMA

  transform evaluates the rising/decaying portions of the sensor resistance by considering the

  maximum/minimum values of y[k] of the following first-order digital filter:  

  y[k] = (1-a)y[k-1] + a(x[k] - x[k-1])  

  where 0 < α < 1 is the smoothing parameter of the filter and x[k] is the acquired value at time k. Since different values of α provide different feature values and different information of the transient response, we computed the EMA filter for three values of α = 0.1, 0.01, 0.001 for both the rising and the decaying stages. Therefore, each of the __16 sensors__ used in the study contributes with __8 features__, thereby yielding a __128-element feature vector__ per measurement.  

   

### 관련 연구  

1. [Chemical gas sensor array dataset](<https://reader.elsevier.com/reader/sd/pii/S2352340915000050?token=703079EA4C2B27AA2C40FBF241BDEE424D1285B924547E4CD23E1F00225824C7F22E6820460C0D3B21DBA671C31CCD8C>)  

   keywords: concept drift, active learning, and pattern recognition in Machine Learning.   

2. [Chemical gas sensor drift compensation using classifier ensembles](<https://www.researchgate.net/publication/216301619_Gas_sensor_drift_mitigation_using_classifier_ensembles>)   

   keywords: sensor drift, chemical sensing, time series classification, ensemble methods, support vector machines   

3. [Effective Clustering Algorithm for Gas Sensor Array
   Drift Dataset](<http://www.periyaruniversity.ac.in/ijcii/issue/Vol3No3December2013/IJCII%203-3-111.pdf>)   

   keywords: K-Means, Fuzzy C-Means(FCM) and Rough K-Means algorithm    

##### Data Folder Link   
[https://archive.ics.uci.edu/ml/machine-learning-databases/00270/](https://archive.ics.uci.edu/ml/machine-learning-databases/00270/)    
[gas_sensor_array_drift](https://github.com/LSHReader/data-explanation/tree/master/Gas%20Sensor%20Array%20Drift/gas_sensor_array_drift/gas_sensor_array_drift)    

데이터 용량(압축상태)    

9.6MB    

