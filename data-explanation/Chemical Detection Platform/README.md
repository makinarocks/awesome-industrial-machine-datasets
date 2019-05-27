## Chemical Detection Platform    
### [Gas sensor arrays in open sampling settings Data Set](https://archive.ics.uci.edu/ml/datasets/Gas+sensor+arrays+in+open+sampling+settings)

The dataset contains 18000 time-series recordings from a chemical detection platform at six different locations in a wind tunnel facility in response to ten high-priority chemical gaseous substances.  
The resulting dataset induces a **ten-class** gas discrimination problem   
The dataset was gathered from December 2010 to April 2012(16 months) in wind tunnel research test-bed facility situated at the BioCircuits Institute, University of California San Diego.    

![](https://img.shields.io/badge/sector-chemical-red.svg)
![](https://img.shields.io/badge/labeled-yes-blue.svg)
![](https://img.shields.io/badge/time--series-yes-blue.svg) ![](<https://img.shields.io/badge/simulation-yes-blue.svg>)     

#### Data Set Information    

  Data Set Characteristics | Attribute Characteristics | Associated Tasks  
  ---- | ---- | ----  
  Multivariate, Time-Series | Real | Classification   

  Number of Instances | Number of Attributes | Number of Missing Values(NaN/not available)  
  ---- | ---- | ----  
  18,000 | 1,950,000 | ?    


  - Number of instances:  
    18,000 times-series measurements recorded from a 72 metal-oxide gas sensor array-based chemical detection platform.  
  
  - Number of attributes:  
    Every measurement contains 72 time-series recorded during 260 seconds, each collected at a sample rate of 100Hz (samples per second).
    The dataset also contains time, temperature, and relative humidity information.  
    72개의 metal-oxide gas sensors + time, temperature, relative humidity information = 75개의 측정치 종류 
    The resulting dataset ultimately includes 75-time series composed of 26000 points.  
    Number of Attributes = 75 * 260* 100 = 1,950,000  (Q. 이렇게 곱했을 때 UCI홈페이지에 나와있는 attributes의 수와 일치하는데, 왜 26000을 곱해주는지는 아직 잘 이해되지 않았다.)  
  
  - 10개의 class인 gas의 이름:  
    Acetone, Acetaldehyde, Ammonia, Butanol, Ethylene, Methane, Methanol, Carbon Monoxide, Benzene, Toluene     
  
  - The goal of this data:  
    Identify and discriminate the mentioned chemical hazards at relevant concentrations regardless of the location of the sensory system platform within the annotated wind tunnel research facility as well as the environmental and parametric conditions induced in the setting (Please see manuscript for more details).  


#### Attribute Information  
- Explanation of folder name  

  - data는 11개의 folders로 이루어짐: number of measurements per chemical class identity + nomial concentration   
    ex. Toluene_200 = gas identity가 Toluene이고, 200ppmv의 농도에서 측정됨  
  - 11개의 folders 각각은 6개의 하위 folders로 이루어짐: represent the line location within the test area of the wind tunnel  
    ex. L1은 location 1 의미, L6은 location 6 의미 (L1이 gas source에 가장 가깝게 위치한 지점)  
  - 6개의 하위 folders 각각은 300개의 files로 이루어져 있음: tunnel의 해당 location에서 측정된 number of measurements를 가지고 있음
    각 파일 이름의 의미 = log information of each of the measurements  
    ex.  
    201106060617_board_setPoint_500V_fan_setPoint_060_mfc_setPoint_Toluene_200ppm_p7  
    201106060617 = year, month, day, time  
    board_setPoint_500V = fixed operating temperature value   
    fan_setPoint_060 = set-point value of the nomial rotational speeds of the multiple-step motor-driven exhaust fan utilized    
    mfc_setPoint_Tolune_200ppm = analyte identity and concentration value for each particular measurement   
    p7 = line point location at which the chemo-sensory platform was located in the wind tunnel  

- 각 column의 의미  
  - 각 data file마다 92개의 columns 가 있고, 그 의미는 다음과 같다.
  - 예를 들어, line 1이 다음과 같다면,  
    22250 0 0 100 100 100 103 103 105 22.22 63.43 1 476 555 803 497 775 885 873 843 1 346 545 635 616 571 552 773 745 1 397 509 660 638     755 744 745 657 1 420 510 525 531 504 650 719 715 1 2201 449 652 1228 847 654 850 737 1 370 459 650 445 756 773 847 803 1 345 457 587   554 757 704 769 818 1 354 407 499 696 786 686 757 733 1 339 418 547 567 653 573 773 84  
    각 column에 해당하는 값의 의미는 다음과 같다.  
    22250 = 22.25초에 측정되었다
    0 0 = set point, measured value of the fan speed  
    100 100 100 103 103 105 = set point, actual measured values of the MFC  
    22.22 63.43 = temperature, humidity values  
    1 = boundary between each sensor module board  
    remaining 80 columns = actual time series values for each measurement -> 이 중에서도 8개의 1은 boundary를 의미하고, 나머지 72개는 앞에서   언급한 72 channels time-series 를 의미함  
### 관련 연구    

__     

##### 아직 의미가 애매한 것 
data file 각각을 열어서 본 결과 column의 수는 92개로 동일하였다. row의 수는 다 달랐다.   
72 time-series(72 channel) = 72 metal-oxide gas sensor 같은 의미인지 (같은 의미인 것 같다)    
75 time-series(72 gas sensor + time, temperature, relative humidity information) * 26000 = 1950000이 attributes의 개수인 이유는 무엇인지(이건 좀 이상하다. 72개의 gas sensor과 time, temperature, humidity 총 75개가 attribute여야 하는 것 아닌지 )  
NA값 있는지? -> data file이 너무 커서 확인하지 못하였다 

##### Data Folder Link   

[https://archive.ics.uci.edu/ml/machine-learning-databases/00251/](https://archive.ics.uci.edu/ml/machine-learning-databases/00251/)  

데이터 용량(압축상태)  

7.8GB  