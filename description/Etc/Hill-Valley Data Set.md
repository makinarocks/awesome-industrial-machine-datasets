# Hill-Valley Data Set

[data](https://archive.ics.uci.edu/ml/datasets/Hill-Valle)

This is NOT a manufacturing dataset, but looks good for testing pattern detection methods.

 ![](https://img.shields.io/badge/sector-etc-red.svg)

 ![](https://img.shields.io/badge/labeled-yes-red.svg)

 ![](https://img.shields.io/badge/time--series-yes-red.svg)

hill-valley classification

#### Data Set Information:

| Data Set Characteristics | Attribute Characteristics | Associated Tasks |
| ------------------------ | ------------------------- | ---------------- |
| Sequential               | Real                      | Classification   |

| Number of Instances | Number of Attributes | Number of Classes |      |
| ------------------- | -------------------- | ----------------- | ---- |
| 1212                | 101                  | 2                 |      |

class는 2개, nominal

feature : V1~V100, Class (총 101개)

Each record represents 100 points on a two-dimensional graph. When plotted in order (from 1 through 100) as the Y co-ordinate, the points will create either a Hill (a “bump” in the terrain) or a Valley (a “dip” in the terrain). 

There are six files, as follows: 

(a) Hill_Valley_without_noise_Training.data 
(b) Hill_Valley_without_noise_Testing.data 

These first two datasets (without noise) are a training/testing set pair where the hills or valleys have a smooth transition. 

(c) Hill_Valley_with_noise_Training.data 
(d) Hill_Valley_with_noise_Testing.data 

These next two datasets (with noise) are a training/testing set pair where the terrain is uneven, and the hill or valley is not as obvious when viewed closely. 

(e) Hill_Valley_sample_arff.text 

The sample ARFF file is useful for setting up experiments, but is not necessary. 

(f) Hill_Valley_visual_examples.jpg 

This graphic file shows two example instances from the data. 

#### Variables

1-100: Labeled “X##”. Floating point values (numeric) 
101: Labeled “class”. Binary {0, 1} representing {valley, hill} 

https://www.openml.org/d/1566