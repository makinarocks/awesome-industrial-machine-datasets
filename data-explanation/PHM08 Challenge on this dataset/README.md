## Mechanical  
### [PHM08 Challenge on this dataset](https://ti.arc.nasa.gov/tech/dash/groups/pcoe/prognostic-data-repository/)  

__C-MAPSS 데이터와 거의 같은데, 유일한 차이점 -> C-MAPSS 데이터에는 true RUL values가 있었던 것에 반해, 이 dataset에는 RUL values가 없다.__ 

Data sets consist of multiple multivariate time series. Each data set is further divided into training and test subsets. Each time series is from a different engine – i.e., the data can be considered to be from a fleet of engines of the same type. Each engine starts with different degrees of initial wear and manufacturing variation which is unknown to the user. This wear and variation is considered normal, i.e., it is not considered a fault condition. There are three operational settings that have a substantial effect on engine performance. These settings are also included in the data. The data are contaminated with sensor noise.
The engine is operating normally at the start of each time series, and starts to degrade at some point during the series. In the training set, the degradation grows in magnitude until a predefined threshold is reached beyond which it is not preferable to operate the engine. In the test set, the time series ends some time prior to complete degradation.  
The objective of the competition is to predict the number of remaining operational cycles before in the test set, i.e., the number of operational cycles after the last cycle that the engine will continue to operate properly.  
The data are provided as a zip-compressed text file with 26 columns of numbers, separated by spaces. Each row is a snapshot of data taken during a single operational cycle; each column is a different variable.  


![](https://img.shields.io/badge/competition-gray.svg)
![](https://img.shields.io/badge/scoring_and_ranking-gray.svg)   

- Attribute Explanation   

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


- Data Set  
train.txt, test.txt, final_test.txt     
Train trjectories: 218   
Test trajectories: 218   
final_test trajectoris: 435    
Train/Test는 모델을 만드는 데 사용하는 것 같고, 마지막으로 final_test 를 써서 final score를 산출하는 것 같다. 
(Once algorithms are trained to satisfaction, users can apply them to the final test dataset contained in the file named final_test.txt. )  
final score은 RUL errors의 weighted sum 이다.    


##### Data Folder Link  
[https://ti.arc.nasa.gov/c/13/](https://ti.arc.nasa.gov/c/13/)   


