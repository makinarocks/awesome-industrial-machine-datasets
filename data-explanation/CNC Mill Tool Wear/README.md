## Mechanical    
### [CNC Mill Tool Wear](https://www.kaggle.com/shasun/tool-wear-detection-in-cnc-mill/data) 

CNC Mill Tool Wear 데이터는 'Tool wear detection', 'Detection of inadequate clamping' 등의 classification studies를 수행하기 위해 제공되었다.    

A series of machining experiments were run on 2" x 2" x 1.5" wax blocks in a CNC milling machine in the System-level Manufacturing and Automation Research Testbed (SMART) at the University of Michigan. Machining data was collected from a CNC machine for variations of tool condition, feed rate, and clamping pressure. Each experiment produced a finished wax part with an "S" shape - S for smart manufacturing - carved into the top face, as shown in `test_artifact.jpg` (included in the dataset).  

18개의 experiment_xx.csv 파일과 train.csv 파일이 제공되었다.  각 experiment_xx.csv 파일은 48개의 columns로 구성되며, 각 row의 수는 experiment_01.csv부터 experiment_18.csv까지 (1056, 1669, 1522, 533, 463, 1297, 566, 606, 741, 1302, 2315, 2276, 2234, 2333, 1382, 603, 2151, 2254) 이다. 18 different experiments에 대한 general data는 train.csv에 제공되어 있다. 18 experiments로부터 수집된 time series data는 100ms 의 sampling rate로 수집되었다.    

![](https://img.shields.io/badge/sector-mechanical-purple.svg)
![](https://img.shields.io/badge/labeled-meta--only-yellow.svg)
![](https://img.shields.io/badge/time--series-yes-blue.svg)  
![](https://img.shields.io/badge/tool_wear_detection-gray.svg)
![](https://img.shields.io/badge/detection_of_inadequate_clamping-gray.svg) ![](<https://img.shields.io/badge/simulation-yes-blue.svg>)    



- Data Set 


Data Set | Number of row | Data Set | Number of row  
---- | ---- | ---- | ----  
experiment_01.csv | 1056 | experiment_10.csv | 1302 
experiment_02.csv | 1669 | experiment_11.csv | 2315 
experiment_03.csv | 1522 | experiment_12.csv | 2276 
experiment_04.csv | 533 | experiment_13.csv | 2234 
experiment_05.csv | 463 | experiment_14.csv | 2333 
experiment_06.csv | 1297 | experiment_15.csv | 1382 
experiment_07.csv | 566 | experiment_16.csv | 603 
experiment_08.csv | 606 | experiment_17.csv | 2151 
experiment_09.csv | 741 | experiment_18.csv | 2254 
 |  | Train.csv | 18 





- Attribute explanation - Train.csv   

| Inputs(features)     | Description                                                  | Outputs(predictions)     | Description                                                  |
| -------------------- | ------------------------------------------------------------ | ------------------------ | ------------------------------------------------------------ |
| No.experiment number | -                                                            | tool_condition           | label for unworn and worn tools                              |
| material             | wax                                                          | machine_completed        | indicator for if machine was completed without the workspace moving out of the pneumatic vise |
| feed_rate            | relative velocity of the cutting tool along the workpiece(mm/s) | passed_visual_inspection | indicator for if the workpiece passed visual   inspection, only available for experiments where machining was completed |
| clamp_pressure       | pressure used to hold the workpiece in the wise(bar)         | -                        |                                                              |

tool_condition 변수에 tool이 unworn인지 worn인지에 대한 여부가 나타나 있다.   

- Attributes explanation - 18 experiment_xx.csv  

  총 48개의 attributes가 있다.  

  | Attribute name            | Type    | Description                                                  |
  | ------------------------- | ------- | ------------------------------------------------------------ |
  | X1_ActualPosition         | float64 | actual x position of part (mm)                               |
  | X1_ActualVelocity         | float64 | actual x velocity of part (mm/s)                             |
  | X1_ActualAcceleration     | float64 | actual x acceleration of part (mm/s/s)                       |
  | X1_CommandPosition        | float64 | reference x position of part (mm)                            |
  | X1_CommandVelocity        | float64 | reference x velocity of part (mm/s)                          |
  | X1_CommandAcceleration    | float64 | reference x acceleration of part (mm/s/s)                    |
  | X1_CurrentFeedback        | float64 | current (A)                                                  |
  | X1_DCBusVoltage           | float64 | voltage (V)                                                  |
  | X1_OutputCurrent          | float64 | current (A)                                                  |
  | X1_OutputVoltage          | float64 | voltage (V)                                                  |
  | X1_OutputPower            | float64 | power (kW)                                                   |
  | Y1_ActualPosition         | float64 | actual y position of part (mm)                               |
  | Y1_ActualVelocity         | float64 | actual y velocity of part (mm/s)                             |
  | Y1_ActualAcceleration     | float64 | actual y acceleration of part (mm/s/s)                       |
  | Y1_CommandPosition        | float64 | reference y position of part (mm)                            |
  | Y1_CommandVelocity        | float64 | reference y velocity of part (mm/s)                          |
  | Y1_CommandAcceleration    | float64 | reference y acceleration of part (mm/s/s)                    |
  | Y1_CurrentFeedback        | float64 | current (A)                                                  |
  | Y1_DCBusVoltage           | float64 | voltage (V)                                                  |
  | Y1_OutputCurrent          | float64 | current (A)                                                  |
  | Y1_OutputVoltage          | float64 | voltage (V)                                                  |
  | Y1_OutputPower            | float64 | power (kW)                                                   |
  | Z1_ActualPosition         | float64 | actual z position of part (mm)                               |
  | Z1_ActualVelocity         | float64 | actual z velocity of part (mm/s)                             |
  | Z1_ActualAcceleration     | float64 | actual z acceleration of part (mm/s/s)                       |
  | Z1_CommandPosition        | float64 | reference z position of part (mm)                            |
  | Z1_CommandVelocity        | float64 | reference z velocity of part (mm/s)                          |
  | Z1_CommandAcceleration    | float64 | reference z acceleration of part (mm/s/s)                    |
  | Z1_CurrentFeedback        | float64 | current (A)                                                  |
  | Z1_DCBusVoltage           | float64 | voltage (V)                                                  |
  | Z1_OutputCurrent          | float64 | current (A)                                                  |
  | Z1_OutputVoltage          | float64 | voltage (V)                                                  |
  | S1_ActualPosition         | float64 | actual position of spindle (mm)                              |
  | S1_ActualVelocity         | float64 | actual velocity of spindle (mm/s)                            |
  | S1_ActualAcceleration     | float64 | actual acceleration of spindle (mm/s/s)                      |
  | S1_CommandPosition        | float64 | reference position of spindle (mm)                           |
  | S1_CommandVelocity        | float64 | reference velocity of spindle (mm/s)                         |
  | S1_CommandAcceleration    | float64 | reference acceleration of spindle (mm/s/s)                   |
  | S1_CurrentFeedback        | float64 | current (A)                                                  |
  | S1_DCBusVoltage           | float64 | voltage (V)                                                  |
  | S1_OutputCurrent          | float64 | current (A)                                                  |
  | S1_OutputVoltage          | float64 | voltage (V)                                                  |
  | S1_OutputPower            | float64 | current (A)                                                  |
  | S1_SystemInertia          | float64 | torque inertia (kg*m^2)                                      |
  | M1_CURRENT_PROGRAM_NUMBER | float64 | number the program is listed under on the CNC                |
  | M1_sequence_number        | float64 | line of G-code being executed                                |
  | M1_CURRENT_FEEDRATE       | float64 | instantaneous feed rate of spindle                           |
  | Machining_Process         | object  | the current machining stage being performed. Includes preparation, tracing up  and down the "S" curve involving different layers, and repositioning of the spindle as it moves through the air to a certain starting point |


- CNC measurements를 사용할 수 있는 방법 2가지  

  (1) Taking every CNC measurement as an independent observation where the operation being performed is given in the Machining_Process column. Active machining operations are labeled as "Layer 1 Up", "Layer 1 Down", "Layer 2 Up", "Layer 2 Down", "Layer 3 Up", and "Layer 3 Down".    

  (2) Taking each one of the 18 experiments (the entire time series) as an observation for time series classification     

  


### 관련 연구   

1. [CNC Machine Tool’s wear diagnostic and prognostic by
   using dynamic bayesian networks](<https://hal.archives-ouvertes.fr/hal-00672204/document>)    

   keywords: dynamic bayesian networks, Diagnostic, Prognostic, Remaining Useful Life, Condition
   Based Maintenance, Hidden Markov Models, Monitoring data, Tool wear     

   


##### Data Download Link   
데이터 용량(압축상태):   

2.56MB   

데이터 용량(압축 푼 상태):   

11.6MB   

