## Project Description

**Analysis Objective:** The goal of the trade-off analysis is to determine which design option for the e-bike has the best combination of high reliability, long range, and low cost.

### 1.MOE and factors of interest
<p align="center">
  <img src="images/moe622.JPG?raw=true" width="700">
</p>
<p align="center">
  <img src="images/foi622.JPG?raw=true" width="700">
</p>

### 2. Modeling and Simulation approach
Analytical models for Cost, Reliability, and Range of the E-bike were developed. A Multi-Attribute Value Function (MAVF) analysis was performed to determine the best design option. Then, a Sensitivity Analysis was performed to assess the effect of uncertainty in the MAVF Analysis results due to the uncertainty in the design factor values. Monte Carlo simulations were performed on the Reliability and Range models to evaluate the uncertainties in the range and reliability of the system which were the inputs to the Sensitivity Analysis.


### 3. System Description
The E-Bike is a personal transportation vehicle which consists of an electric propulsion system fitted to a bicycle chassis. Figure 1 depicts a System Block Definition Diagram of the E-bike System with its environment. The following are the principal components of the E-bike system:

1.	Rider/ User: The rider/user of the system is the person who is riding the E-bike for his/her daily commute. For the purpose of  analysis, we have considered the rider to be an adult with a body weight of 80kg (176.36 lbs.).

2.	Chassis: The Chassis is the main structural component of the E-bike and all the systems components are attached to it. For the purpose of the analysis, we have considered a chassis made of steel which weighs 25 kg.

3.	Battery Package: The battery package consists of the battery, charge controller, discharge controller, and the wiring harness. The battery is used as the primary power source to propel the E-bike forward. For the purpose of the analysis, we have considered batteries with the same energy capacity of 1440 Wh.

4.	Motor Package: The motor package includes the motor, its wiring harness, and the motor controller. The motor provides the necessary torque to drive the wheels of the E-bike. We are considering 48V 1000W motors for this analysis.

The environmental factors that affect the E-bike system performance are:

1.	Wind

2.	Terrain surface resistance

3.	Terrain Gradient or slope

### 4. Analysis Approach
This section will provide a brief description of the analysis performed and the supporting mathematical models involved.

1.	Establish the design options to be studied

2.	Identify metrics for analysis– reliability, range, and cost

3.	Identify Factors affecting selected metrics

4.	Develop an analytical model for the cost

5.	Develop an analytical model for System Reliability

6.	Develop analytical models of E-bike Range

7.	Perform MAVF (multi attribute value function) analysis to determine the best design option

8.	Develop stochastic (Monte Carlo) models and simulations for Reliability

9.	Develop stochastic (Monte Carlo) models and simulations for Range

10.	Perform sensitivity analysis on the MAVF solution

### 5. Analytical Models

1. Range Model
<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;Range=\frac{E_{batt}*\eta_{motor}}{F_aero+F_rolling+F_slope}" /><br/>
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;F_{aero}=K_{aero}(V+V_{wind})^2" /><br/>
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;F_{rolling}=C_{rr}M_g" /><br/>
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;M=M_{rider}+M_{chassis}+M_{motor}+M_{battery}" /><br/>
  where-<br/>
    <img src="https://latex.codecogs.com/svg.latex?\Large&space;E_{batt}=" /> battery's total energy<br/>
    <img src="https://latex.codecogs.com/svg.latex?\Large&space;\eta_{motor}=" /> motor's efficiency<br/>
    <img src="https://latex.codecogs.com/svg.latex?\Large&space;V=" /> Velocity of the E-bike<br/>
    <img src="https://latex.codecogs.com/svg.latex?\Large&space;V_{wind}=" /> Velocity of the wind<br/>
    <img src="https://latex.codecogs.com/svg.latex?\Large&space;C_{rr}=" /> coefficient of rolling friction or resistance<br/>
</p>

<p align="center">
  <img src="images/range622.JPG?raw=true" width="300">
</p>

### 6. Monte-Carlo Results
The objective of the Range Monte Carlo Simulation is to determine the uncertainty in the Range given the uncertainty in the factor values. The Monte Carlo simulation is performed 2000 times (N=2000) by assuming the bike velocity, wind velocity, gradient and rolling resistance to be random variables. A normal distribution is assumed for all the above-mentioned variables with the following characteristics:
<p align="center">
  <img src="images/MCtable622.JPG?raw=true" width="500">
</p>
The design options consist of different battery and motor technology. The results of the MC analysis for range are-  
<p align="center">
  <img src="images/MCresult622.JPG?raw=true" width="500">
</p>
<p align="center">
  <img src="images/Mcgraph622.JPG?raw=true" width="500">
</p>
### 7. Sensitivity Analysis
The Sensitivity Analysis is Performed by changing the Reliability, Range and Cost values to their high/low values of DO2 (the reference DO) and by recording the changes in the MAVF values as shown in the following table.
<p align="center">
  <img src="images/sen1622.JPG?raw=true" width="500">
</p>
The high/low values are determined by Monte Carlo Simulations for Range and Reliability Models and by using high/low component cost values for Cost model as described before. Then a Tornado diagram is developed to visualize the dependency of uncertainties on the total uncertainty in the MAVF value.
<p align="center">
  <img src="images/sen2622.JPG?raw=true" width="500">
</p>
<p align="center">
  <img src="images/tornado622.JPG?raw=true" width="500">
</p>

### 8. Results
The Design Option 2 i.e. Ni-Cd Battery with Brushless DC motor is the recommended design option as it is the best design option based on the MAVF analysis as discussed above. But as discussed in the Sensitivity Analysis, due to uncertainties in Range and Reliability factor values, the Design Option 1 can also be selected. Thus, for a conclusive result we might have to collect extensive data on Range factors viz. wind velocity, terrain gradient and rolling resistance to reduce the uncertainty in the Range model. 
