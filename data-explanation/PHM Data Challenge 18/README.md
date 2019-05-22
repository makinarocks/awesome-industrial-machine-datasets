
## Semicon
### [PHM DATA Challenge 18](https://www.phmsociety.org/events/conference/phm/18/data-challenge): Etching tool fault detection (PdM)  

PHM Data Challenge 18에서 제공한 데이터는 웨이퍼 제조 공정 내에서, ion mill etch tools의 fault behavior을 조사하기 위한 목적으로 제공되었다. 다양한 설정 조건 하에서 작동하는 ion mill etching tools 로부터, 시간 순으로 센서 데이터를 수집한 데이터베이스이다.  

![](https://img.shields.io/badge/sector-semicon-blue.svg)
![](https://img.shields.io/badge/labeled-yes-blue.svg)
![](https://img.shields.io/badge/time--series-yes-blue.svg) ![](<https://img.shields.io/badge/simulation-no-red.svg>)        

#### Training data

Training data는 총 60개의 csv파일로 구성되어 있으며, training data인 train 파일 20개, 이상 시점에서만의 이상 정보를 담은 train_fault 파일 20개, ttf 정보를 표시한 train_ttf 파일 20개로 이루어져 있다.  

- 요약  

이상 데이터 개수| 정상 데이터 개수 | 총 데이터 개수  
---- | ---- | ----  
1,236 | 82,188,204 | 82,189,440   

- Train 파일 20개는 총 82,189,440개의 row로 이루어져 있으며, 24개의 column으로 구성된다. 24개의 column 정보는 아래와 같다. 

ID#| Parameter Name | Type | Description
---- | ---- | ---- | ----
S1 | time | Numeric | time
S2 | Tool | Categorical | tool id
S3 | stage | Categorical | processing stage of wafer
S4 | Lot | Categorical | wafer id
S5 | runnum | Numeric | number of times tool has been run
S6 | recipe | Categorical | describes tool settings used to process wafer
S7 | recipe_step | Categorical | process step of a recipe
S8 | IONGAUGEPRESSURE | Numeric(Sensor) | pressure reading for the main process chamber when under vacuum
S9 | ETCHBEAMVOLTAGE | Numeric | voltage potential applied to the beam plate of the grid assembly
S10 | ETCHBEAMCURRENT | Numeric | ion current impacting the beam grid determining the amount of ions accelerated through the grid assembly to the wafer
S11 | ETCHSUPPRESSORVOLTAGE | Numeric | voltage potential applied to the suppressor plate of the grid assembly
S12 | ETCHSUPPRESSORCURRENT | Numeric(Sensor) | ion current impacting the suppressor grid plate
S13 | FLOWCOOLFLOWRATE | Numeric | rate of flow of helium through the flowcool circuit, controlled by mass flow controller
S14 | FLOWCOOLPRESSURE | Numeric(Sensor) | resulting helium pressure in the flowcool circuit
S15 | ETCHGASCHANNEL1READBACK | Numeric | rate of flow of argon into the source assembly in the vacuum chamber
S16 | ETCHPBNGASREADBACK | Numeric | rate of flow of argon into the PBN assembly in the chamber
S17 | FIXTURETILTANGLE | Numeric | wafer tilt angle setting
S18 | ROTATIONSPEED | Numeric | wafer rotation speed setting
S19 | ACTUALROTATIONANGLE | Numeric(Sensor) | measure wafer rotation angle
S20 | FIXTURESHUTTERPOSITION | Numeric | open / close shutter setting for wafer shielding
S21 | ETCHSOURCEUSAGE | Numeric | counter of use for the grid assembly consumable
S22 | ETCHAUXSOURCETIMER | Numeric | counter of the use for the chamber shields consumable
S23 | ETCHAUX2SOURCETIMER | Numeric | counter of the use for the chamber shields consumable
S24 | ACTUALSTEPDURATION | Numeric(Sensor) | measured time duration for a particular step


- Train_fault 파일 20개는 총 1,236개의 row로 이루어져 있으며, 3개의 column으로 구성된다. 

ID#| Parameter Name | Type | Description
---- | ---- | ---- | ----
F1 | time | Numeric | time
F2 | fault_name | Categorical | name of the particular class of fault that occurred at the specified time
F3 | stage | Categorical | - 

- Train_ttf 파일 20개는 총 82,189,440개의 row로 이루어져 있으며, 4개의 column으로 구성된다.     

Parameter Name | Type
---- | ----
time | Numeric 
TTF_FlowCool Pressure Dropped Below Limit | Numeric 
TTF_Flowcool Pressure Too High Check Flowcool Pump | Numeric 
TTF_Flowcool leak | Numeric  

#### Test data
- Test data는 5개의 csv파일로 이루어져 있다. 총 7,198,948개의 row로 이루어져 있으며, 24개의 column으로 구성된다.   

####  data challenge의 task(목적)    

이 PHM data challenge 의 목적은 다음 두 가지와 같다.  

1. Diagnose failure(i.e detect and identify)  
2. Determine time remaining until next failure (i.e predict remaining useful life)  

#### 관련 연구

PHM data challenge 2018에서 제공한 데이터를 사용한 것은 아니지만, [2018 PHM Society Conference brochure (2018-09-22).pdf](<https://www.phmsociety.org/sites/phmsociety.org/files/2018%20PHM%20Society%20Conference%20brochure%20(2018-09-22).pdf>) 의 paper session에 등록되어 있는 몇가지 논문을 첨부하였다.  

1. [A Data Driven Health Monitoring Approach to Extending Small
   Sats Mission](https://www.phmpapers.org/index.php/phmconf/article/download/573/phmc_18_573) - Prognostics    

   keywords: anomaly detection, LSTM, Auto-Encoder, sensor   

2. [Automated Hyper-parameter Tuning for Machine Learning Models
   in Machine Health Prognostics](https://www.phmpapers.org/index.php/phmconf/article/download/490/phmc_18_490) - : Diagnostics  

   keywords: data from PHM 2016 Data Challenge, Bayesian optimization algorithms, hyper-parameter optimization problem  

##### 데이터 다운로드 링크  
[https://drive.google.com/open?id=15Jx9Scq9FqpIGn8jbAQB_lcHSXvIoPzb](https://drive.google.com/open?id=15Jx9Scq9FqpIGn8jbAQB_lcHSXvIoPzb)

데이터 용량(압축상태) : 5.0G   

