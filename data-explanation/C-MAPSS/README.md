## Mechanical    
### [C-MAPSS](https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/) 
#### Turbofan Engine Degradation Simulation Data Set  

C-MAPSS 데이터를 이용하여 engine degradation simulation 을 수행하고자 한다. 각 data set은 train과 test set으로 나뉘어져 있다.  
각각의 time-series data set는 다른 engine에서 얻은 data set이다. 하나의 dataset은 동일한 유형의 엔진으로부터 온 데이터이다.  
4개의 data set은 각각 operational conditions(ONE, SIX)와 fault modes(ONE, TWO)를 다르게 한 상태에서 얻어진 multivariate time-series data이다.  
engine performance에 영향을 주는 three operational settings가 있다.  
각 test data에 대해서, RUL(Remaining Useful Life) values 값이 제공된다.  
training set에서는, 엔진을 가동하는 것이 좋지 않다고 판단되는 predefined threshold에 도달할 때까지 degradation이 커진다. test set에서는
완전히 degradation이 되기 전에 시계열 데이터가 종료된다.  
각 data set마다 26개 sensors를 의미하는 columns가 있다.   

response surfaces of all sensors are generated via a thermo-dynamical simulation model for the engine as a function of variations of flow and efficiency of the modules of interest.  

![](https://img.shields.io/badge/sector-mechanical-purple.svg)
![](https://img.shields.io/badge/labeled-implicit-green.svg)
![](https://img.shields.io/badge/time--series-yes-blue.svg)  
![](https://img.shields.io/badge/time--to--failure-gray.svg)![](<https://img.shields.io/badge/simulation-yes-blue.svg>)     

- 데이터 부연 설명  

각 엔진은 초기에 약간의 wear(마모)가 있고 manufacturing variation이 있지만 이는 정상적인 것으로 간주된다.  
engine performance에 영향을 주는 three operational settings 가 있음. -> 데이터에 영향을 미친다.  
data가 sensor noise에 의해 오염되었다.  
각 시계열 데이터가 수집되는 처음에는 엔진은 정상 상태에서 시작하며, 어느 time point에서 fault가 발생한다.    
training set에서, system failure 가 발생할 때까지 fault가 커진다.  
test set에서, 시계열은 system failure 가 발생하기 전에 어느 정도 종료된다.    

- competition에서의 목적   
test set에서, system failure가 발생하기 전까지의 the number of remaining operational cycles 를 예측하는 것.     


- 각 data set마다 요약    

Data Set | Train trajectories | Test trajectories | Conditions | Fault modes  
---- | ---- | ---- | ---- | ----
FD001 | 100 | 100 | One(sea level) | One(HPD Degradation)   
FD002 | 260 | 259 | Six | One(HPC degradation)   
FD003 | 100 | 100 | One | Two(HPC degradation, fan degradation)   
FD004 | 249 | 248 | Six | Two(HPC degradation, fan degradation)  

Train Data Set | Number of row | Test Data Set | Number of row  | RUL Data Set | Number of row 
---- | ---- | ---- | ----  | ----  | ----  
FD001 | 20631 | FD001 | 13096  | FD001 | 100 
FD002 | 53759 | FD002 | 33991  | FD002 | 259 
FD003 | 24720 | FD003 | 16596  | FD003 | 100 
FD004 | 61249 | FD004 | 41214  | FD004 | 248 


- Attributes Explanation    

각 dataset마다 26개의 columns가 있다.  
The columns correspond to:  

1)	unit number  
2)	time, in cycles  
3)	operational setting 1  
4)	operational setting 2  
5)	operational setting 3  
6)	sensor measurement  1  
7)	sensor measurement  2  
...  
26)	sensor measurement  26   

- train/test data set __N/A__   
  __None__( 존재하지 x)  
- 추가적으로 조사할 것  
  test data가 아니라 train data에 RUL값이 제공되어야 하는 것 아닌지 -> 그건 아니고, train data는 위에서 특정 threshold에 도달할 때까지 진행된다고 하였다.   
  RUL dataset에서 각 element값이 각 test set에서 어떤 timestep에서의 RUL 값을 의미하는건지 -> 각 test set의 unit number의 max 수만큼 RUL값이 있다.  
  RUL_FD001에서, 첫번째 row에 있는 값의 의미 = test_FD001에서 unit number = 1 에 해당하는 operation의 RUL 값 -> 시점 기준이 last cycle 인지 first cycle인지 모르겠다.  

### 관련 연구  

1. [Long Short-Term Memory Network for Remaining
   Useful Life Estimation](<http://www.hitachi-america.us/rd/about_us/bdl/docs/LSTM_RUL.PDF>)   

   keywords: LSTM,  Multi-Layer Perceptron (MLP), Support Vector Regression (SVR), Relevance Vector Regression (RVR) and Convolutional Neural Network (CNN)   

2. [Remaining Useful Life Estimation Using Functional
   Data Analysis](<https://arxiv.org/pdf/1904.06442.pdf>)   

   keywords: LSTM, CNN, MLP    



##### Data Download Link  
[https://ti.arc.nasa.gov/c/6/](https://ti.arc.nasa.gov/c/6/)   

데이터 용량(압축상태):  

11.9MB   

