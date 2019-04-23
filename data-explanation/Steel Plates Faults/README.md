# Steel Plates Faults Data Set

[data](http://archive.ics.uci.edu/ml/datasets/Steel+Plates+Faults)

sector : steel

 ![](https://img.shields.io/badge/sector-steal-red.svg)

 ![](https://img.shields.io/badge/labeled-yes-blue.svg)

 ![](https://img.shields.io/badge/time--series-no-blue.svg)

fault classification

#### Data Set Information

| Data Set Characteristics | Attribute Characteristics | Associated Tasks |
| ------------------------ | ------------------------- | ---------------- |
| Multivariate             | Real                      | Classification   |

| Number of Instances | Number of Attributes |      |      |
| ------------------- | -------------------- | ---- | ---- |
| 1941                | 27                   |      |      |

(Faults.NNA data)

There are 34 fields. The first 27 fields describe some kind of steel plate faults seen in images

The last 7 columns are one hot encoded classes, i.e. if the plate fault is classified as "Stains" there will be a 1 in that column and 0's in the other columns. If you are unfamiliar with one hot encoding, **just know that the last seven columns are your class labels.**

Every dataset record represents a superficial fault of a stainless steel leaf. There are 6 different typologies of
faults. The fault description is constituted by 27 indicators representing the geometric shape of the fault
and its contour. We have 1941 records in total. 

The Faults’ dataset underlines, in a well-marked way, the efficacy in using meta-classifiers and is further
illustrative of the evidence that serves to establish the quality of Meta-Consensus as a classifier. While it
occupies the third position in terms of weighted average, it is the first of the set that does not create a
base classifier (Arcing, Boosting) but rather, uses the available base classifiers. 

#### Variable

27 Independent variables

X_Minimum  
X_Maximum  
Y_Minimum   
Y_Maximum  
Pixels_Areas  
X_Perimeter  
Y_Perimeter  
Sum_of_Luminosity  
Minimum_of_Luminosity  
Maximum_of_Luminosity  
Length_of_Conveyer  
TypeOfSteel_A300  
TypeOfSteel_A400  
Steel_Plate_Thickness  
Edges_Index  
Empty_Index  
Square_Index  
Outside_X_Index  
Edges_X_Index  
Edges_Y_Index  
Outside_Global_Index  
LogOfAreas  
Log_X_Index  
Log_Y_Index   
Orientation_Index  
Luminosity_Index  
SigmoidOfAreas   

Type of dependent variables(7 Types of Steel Plates Faults) - one hot encoding

Pastry  
Z_Scratch  
K_Scatch  
Stains  
Dirtiness  
Bumps  
Other_Faults  

file:///home/makinarocks/Downloads/METANET.pdf  

file:///home/makinarocks/Downloads/NAFIPS-101-Buscema.pdf  