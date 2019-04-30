## Semicon  
### [SECOM](http://archive.ics.uci.edu/ml/datasets/secom): Semiconductor manufacturing process data.  

반도체 제조 공정에서 590개의 sensors로부터 수집한 FAB 데이터이다. Data는 secom.data와 secom_labels.data 두 파일로
이루어져 있다. secom.data 파일은 590개의 features, 1567개의 examples를 가진 1567 * 590 matrix로 구성되어 있다.  secom_labels.data는 1567개의 각 data마다 classifications 값과 data time stamp 값을 포함하고 있다. secom_labels.data에서 -1은 pass(정상), 1은 fail(비정상)을 나타낸다.   

![](https://img.shields.io/badge/sector-semicon-blue.svg)
![](https://img.shields.io/badge/labeled-yes-blue.svg)
![](https://img.shields.io/badge/time--series-yes-blue.svg)
![](https://img.shields.io/badge/feature_selection-gray.svg)![](<https://img.shields.io/badge/simulation-no-red.svg>)         


- 참고  

data file 내에 training data와 test data가 구분되어 있지 않다.  
590개의 각 변수 -> 590개 각각의 sensor를 의미 
[UCI 홈페이지](http://archive.ics.uci.edu/ml/datasets/secom)에서는 feature의 개수를 591개라고 명시하였으나, 데이터를 직접 로드해 본 결과 secom.data을 dataframe으로 전환한 형태가 (1567, 590)의 shape을 가지고 있었다. 또한 "Big Data Technologies and Applications. Springer International Publishing. (2018)" 에서도 590개의 feature라고 명시하였다.  

- 데이터 요약  

Data Set Characteristics | Attribute Characteristics | Associated Tasks  
---- | ---- | ----  
Multivariate | Real | Classification, Casual - Discovery  

Number of Instances | Number of Attributes | Number of Missing Values(NaN) in secom.data 
---- | ---- | ----  
1567 | 590 | 41951(1567 by 590 matrix 중에서 NA 수)    

- 클래스 개수  

Number of pass | Number of fail | total 
---- | ---- | ---- 
 1463 | 104  | 1567  

#### 관련 연구  

1. [Predictive Models for Equipment Fault Detection in the
   Semiconductor Manufacturing Process ](<http://www.ijetch.org/vol8/898-T10023.pdf>) - 여러 개의 전통적인 머신러닝 방법론 들을 사용한 듯?  

2. [Machine learning for sensor-based manufacturing processes](<https://ieeexplore.ieee.org/document/8116997>)   

   keywords: feature selection, random forest, gradient boosted trees , PCA, Logistic Regression  

   


##### Data Folder Link  
[http://archive.ics.uci.edu/ml/machine-learning-databases/secom/](http://archive.ics.uci.edu/ml/machine-learning-databases/secom/)  

데이터 용량  

secom.data : 5.13MB    

secom.names : 5KB    

secom_labels.data :   40KB   






