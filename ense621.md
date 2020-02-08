## Project Description

**Project description:** Apply concepts of systems engineering to develop a mode of urban commute which is economical, easy to operate and maintain, safe and reliable, reasonably fast and not-physically demanding, portable, eco-friendly, and has range in the order of a few miles.

### 1.Stakeholders
<p align="center">
  <img src="images/stakeholders.JPG?raw=true" width="500">
</p>

### 2. Top level capabilities and Measures of Effectiveness
<p align="center">
  <img src="images/tlcap.JPG?raw=true" width="500">
</p>
<p align="center">
  <img src="images/MOE.JPG?raw=true" width="600">
</p>

### 3. Domain Definition BDD (SysML)
<p align="center">
  <img src="images/domainBDD.JPG?raw=true" width="1100">
</p>

### 4. System Context IBD (SysML)
<p align="center">
  <img src="images/contextIBD.JPG?raw=true" width="500">
</p>
The Maintainer has access to diagnostic data from the system and is authorised to service the vehicle. The operator (i.e user) has also has access to the disgnastic data to carry out simple maintenance.

### 5. Use Case Diagram (SysML)
<p align="center">
  <img src="images/usecase.JPG?raw=true" width="500">
</p>
The are three main use cases are illustrated by the figure above.

### 6. Trade-off Analysis
The objective of the tradeoff analysis is to select a design option which corresponds to minimum weight and minimum cost for the fixed design parameters (Chassis Strength, Battery Capacity and Motor Power).

Method: Pareto Frontier analysis and Multi Attribute Value Function (MAVF) 

Firstly, we define the design criterion. The design factors that were considered in generating alternatives are as follows:
1. Chassis Material (keeping the strength constant).
2. Battery technology (keeping the battery capacity and voltage constant).
3. Motor configuration (keeping the motor power constant).
<p align="center">
  <img src="images/design.JPG?raw=true" width="500">
</p>
Our reference design concept consists of Steel chassis, Lead acid battery and front hub motor. 
<p align="center">
  <img src="images/designoptions.JPG?raw=true" width="500">
</p>
The Pareto grapg is as below-
<p align="center">
  <img src="images/paretoGraph.JPG?raw=true" width="500">
</p>

### 7. MAVF Analysis
The single attribute value function for selecting optimal solution in this case is:
<p align="center">
  𝑉=𝑤_1∗(𝑁𝑜𝑟𝑚𝑎𝑙𝑖𝑧𝑒𝑑 𝑊𝑒𝑖𝑔ℎ𝑡)+𝑤_2∗(𝑁𝑜𝑟𝑚𝑎𝑙𝑖𝑧𝑒𝑑 𝐶𝑜𝑠𝑡)
<p>
MAVF Swing Weighing:
<p align="center">
  <img src="images/MAVFtable.JPG?raw=true" width="500">
</p>
where, w1 = weight for “Weight” metric = 0.3
       w2 = weight for “Cost” metric = 0.7

<p align="center">
  <img src="images/MAVFresults.JPG?raw=true" width="500">
</p>

Result and recommendation: The minimum MAVF value corresponds to the #7 design option which is Aluminum chassis with LiPo battery and Mid drive motor configuration. 


