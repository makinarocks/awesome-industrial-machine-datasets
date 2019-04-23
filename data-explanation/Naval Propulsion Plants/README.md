# Condition Based Maintenance of Naval Propulsion Systems

[data](https://archive.ics.uci.edu/ml/datasets/Condition+Based+Maintenance+of+Naval+Propulsion+Plants#)

Data have been generated from a sophisticated simulator of a Gas Turbines (GT), mounted on a Frigate characterized by a COmbined Diesel eLectric And Gas (CODLAG) propulsion plant type.

 ![](https://img.shields.io/badge/sector-mechanical-red.svg)

 ![](https://img.shields.io/badge/labeled-yes-blue.svg)

 ![](https://img.shields.io/badge/time--series-yes-blue.svg)  

#### Data Set Information

- 데이터 요약  

| Data Set Characteristics | Attribute Characteristics | Associated Tasks |
| ------------------------ | ------------------------- | ---------------- |
| Multivariate             | Real                      | Regression       |

| Number of Instances | Number of Attributes |      |      |
| ------------------- | -------------------- | ---- | ---- |
| 11934               | 16                   |      |      |

> 

The experiments have been carried out by means of a numerical simulator of a naval vessel (Frigate) characterized by a Gas Turbine (GT) propulsion plant. The different blocks forming the complete simulator (Propeller, Hull, GT, Gear Box and Controller) have been developed and fine tuned over the year on several similar real propulsion plants. In view of these observations the available data are in agreement with a possible real vessel. 
In this release of the simulator it is also possible to take into account the performance decay over time of the GT components such as GT compressor and turbines. 
The propulsion system behaviour has been described with this parameters: 

- Ship speed (linear function of the lever position lp). 
- Compressor degradation coefficient kMc. 
- Turbine degradation coefficient kMt. 
  so that each possible degradation state can be described by a combination of this triple (lp,kMt,kMc). 
  The range of decay of compressor and turbine has been sampled with an uniform grid of precision 0.001 so to have a good granularity of representation. 
  In particular for the compressor decay state discretization the kMc coefficient has been investigated in the domain [1; 0.95], and the turbine coefficient in the domain [1; 0.975]. 
  Ship speed has been investigated sampling the range of feasible speed from 3 knots to 27 knots with a granularity of representation equal to tree knots. 
  A series of measures (16 features) which indirectly represents of the state of the system subject to performance decay has been acquired and stored in the dataset over the parameter's space. 

#### Variables

A 16-feature vector containing the GT measures at steady state of the physical asset:   

1 - Lever position (lp) [ ]  
2 - Ship speed (v) [knots]  
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

- GT Compressor decay state coefficient.  
- GT Turbine decay state coefficient.   

#### NOTE

- Features are not normalized
- Each feature vector is a row on the text file (18 elements in each row)

데이터가 사용된 논문 : Integration of Numerical Modeling and Simulation Techniques for the
Analysis of Towing Operations of Cargo Ships (데이터 소개는 딱히 없음)