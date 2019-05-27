# Condition Based Maintenance of Naval Propulsion Systems

[data](https://archive.ics.uci.edu/ml/datasets/Condition+Based+Maintenance+of+Naval+Propulsion+Plants#)

567.1KB (압축)

Data have been generated from a sophisticated simulator of a Gas Turbines (GT), mounted on a Frigate characterized by a COmbined Diesel eLectric And Gas (CODLAG) propulsion plant type.

 ![](https://img.shields.io/badge/sector-mechanical-purple.svg)  ![](https://img.shields.io/badge/labeled-yes-blue.svg)  ![](https://img.shields.io/badge/time--series-no-red.svg)  ![](<https://img.shields.io/badge/simulation-yes-blue.svg>)

#### Data Set Information

| Data Set Characteristics | Attribute Characteristics | Associated Tasks |
| ------------------------ | ------------------------- | ---------------- |
| Multivariate             | Real                      | Regression       |

| Number of Instances | Number of Attributes |      |      |
| ------------------- | -------------------- | ---- | ---- |
| 11934               | 16                   |      |      |

> The experiments have been carried out by means of a numerical simulator of a naval vessel (Frigate) characterized by a Gas Turbine (GT) propulsion plant.
>
> 완전한 simulator(Propeller, Hull, GT, Gear Box and Controller)를 형성하는 다른 여러 block이 개발되어 몇몇 실제 propulsion plants에서 일년 내내 fine tuned되었음.
>
> 이 release of the simulator에서는 GT compressor and turbines와 같은 GT 구성요소의 성능 저하를 고려할 수도 있음
>
> **The propulsion system behaviour has been described with this parameters:**

- Ship speed (linear function of the lever position lp). 
- Compressor degradation coefficient kMc. 
- Turbine degradation coefficient kMt. 

**so that each possible degradation state can be described by a combination of this triple (lp,kMt,kMc). **

compressor와 turbine의 감쇄 범위는 정확히 0.001의 균등한 grid로 sampling되었으므로 표현의 세분화가 잘 됨. 

In particular for the compressor decay state discretization the kMc coefficient has been investigated in the domain [1; 0.95], and the turbine coefficient in the domain [1; 0.975]. 
Ship speed has been investigated sampling the range of feasible speed from 3 knots to 27 knots with a granularity of representation equal to three knots. 

성능 저하의 영향을 받는 system의 상태를 간접적으로 나타내는 일련의 측정(16개의 features)이 수집되어 parameter's space에 저장됨

A series of measures (16 features) which indirectly represents of the state of the system subject to performance decay has been acquired and stored in the dataset over the parameter's space. 

#### Variables

A 16-feature vector containing the GT measures at steady state of the physical asset:   

1 - Lever position (lp) [ ]  
2 - Ship speed (v) [knots] (3,6,9,...,27 을 반복, 3씩 커짐)  
3 - Gas Turbine shaft torque (GTT) [kN m]  
4 - Gas Turbine rate of revolutions (GTn) [rpm]  
5 - Gas Generator rate of revolutions (GGn) [rpm]  
6 - Starboard Propeller Torque (Ts) [kN]  
7 - Port Propeller Torque (Tp) [kN]  
8 - HP Turbine exit temperature (T48) [C]  
9 - GT Compressor inlet air temperature (T1) [C]  
10 - GT Compressor outlet air temperature (T2) [C]  
11 - HP Turbine exit pressure (P48) [bar]  
12 - GT Compressor inlet air pressure (P1) [bar]  
13 - GT Compressor outlet air pressure (P2) [bar]  
14 - Gas Turbine exhaust gas pressure (Pexh) [bar]  
15 - Turbine Injecton Control (TIC) [%]  
16 - Fuel flow (mf) [kg/s]  

17 - GT Compressor decay state coefficient. (kMc, 0.95~1) 

18 - GT Turbine decay state coefficient. (kMt)

**NOTE**

- Features are not normalized
- Each feature vector is a row on the text file (18 elements in each row)

#### Paper

[Condition-Based Maintenance of Naval Propulsion Systems with supervised Data Analysis](https://www.sciencedirect.com/science/article/pii/S0029801817307242) 

**highlights**

- A real-data validated model for the performance decay assessment of the main propulsion plant systems is presented.
- Data-Driven models to investigate the problem of performing Condition-Based Maintenance on a ship propulsion system.
- Several state-of-the-art supervised learning techniques are adopted.
- Unsupervised [learning algorithms](https://www.sciencedirect.com/topics/engineering/learning-algorithm) for [anomaly detection](https://www.sciencedirect.com/topics/engineering/anomaly-detection).
- The results confirm that it is possible to treat a CBM problem in a supervised fashion adopting regression techniques.

Abstract

Depending on the adopted strategy, impact of maintenance on overall expenses can remarkably vary.

ship propulsion system의 유지 보수 기술을 고장이나 예방 유지보수에서보다 효과적인 condition-based 유지 보수 접근법으로 progress하는것이 바람직하다

- **condition-based 유지보수의 성공을 위해 효율적인 예측 모델을 개발하는 것이 필요함**

The behavior and interaction of the [main components](https://www.sciencedirect.com/topics/engineering/main-component) of Ship [Propulsion](https://www.sciencedirect.com/topics/earth-and-planetary-sciences/propulsion) Systems cannot be easily modeled with a priori physical knowledge, considering the large amount of variables influencing them. Data-Driven Models (DDMs), instead, exploit advanced statistical techniques to build models directly on the large amount of historical data collected by on-board [automation systems](https://www.sciencedirect.com/topics/engineering/automation-system), **without requiring any a [priori knowledge](https://www.sciencedirect.com/topics/engineering/priori-knowledge)**. DDMs are extremely useful when it comes to continuously monitoring the propulsion equipment and take decisions based on the [actual condition](https://www.sciencedirect.com/topics/engineering/actual-condition) of the propulsion plant. In this paper, the authors investigate the problem of performing Condition-Based Maintenance through the use of DDMs. In order to conceive this purpose, several state-of-the-art [supervised learning](https://www.sciencedirect.com/topics/earth-and-planetary-sciences/supervised-learning) techniques are adopted, which require labeled sensor data in order to be deployed. **A [naval vessel](https://www.sciencedirect.com/topics/engineering/naval-vessels), characterized by a combined diesel-electric and gas propulsion plant, has been exploited to collect such data and show the effectiveness of the proposed approaches.** Because of confidentiality constraints with the Navy the authors used a real-data validated [simulator](https://www.sciencedirect.com/topics/engineering/simulators) and the [dataset](https://www.sciencedirect.com/topics/engineering/dataset) has been published for free use through the UCI repository.

#### Citation Request:

[1] A. Coraddu, L. Oneto, A. Ghio, S. Savio, D. Anguita, M. Figari, Machine Learning Approaches for Improving Condition?Based Maintenance of Naval Propulsion Plants, Journal of Engineering for the Maritime Environment, 2014, DOI: 10.1177/1475090214540874, (In Press) 

@article{Coraddu2013Machine, 
author={Coraddu, Andrea and Oneto, Luca and Ghio, Alessandro and 
Savio, Stefano and Anguita, Davide and Figari, Massimo}, 
title={Machine Learning Approaches for Improving Condition?Based Maintenance of Naval Propulsion Plants}, 
journal={Journal of Engineering for the Maritime Environment}, 
volume={--}, 
number={--}, 
pages={--}, 
year={2014} 
}