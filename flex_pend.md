## Project Description

**Project description:** The Discrete Elastic Rod (DER) theory is one of the many approaches to model flexible bodies. Based on Kirchhoff's rod theory. Uses concepts from discrete differential geometry. Primary focus is on the planar case. 
<p align="center">
  <img src="images/coiling_1.gif?raw=true" width="500">
</p>
<p align="center">
  Credits: http://www.cs.columbia.edu/cg/elastic_coiling/
</p>

### 1. DER Formulation

Consider a pendulum with flexible link of mass M continuously distributed throughout the length L. If the link is rigid, the dynamics are straightforward. For a flexible link, DER formulation “discretizes” the rod into a set of-

1. N nodes each with a mass 𝑀_𝑖.
2. N-1 edges of length of length 𝐿_𝑖. 
	
<p align="center">
  <img src="images/pder1.JPG" height 100 width=500>
</p>
<p align="center">
  Figure 1.1, Jawed, M.K., Novelia, A., O’Reilly O, M.: A Primer on the Kinematics of Discrete Elastic Rods. [1]
</p>

Predicted model is close to the theoretical model (Based on Euler’s classical theory of elasticity) for higher values of N. The Mass is assumed to be concentrated at nodes, with the links being massless. A given node ‘i’ is only affected by its immediate neighbors. (Nodes i-1 and i+1).


### 2.PDER Theory
Twisting about the center line is neglected. A set of links can only stretch and/or bend in a plane. (assume this to be the x-y plane)

<p align="center">
  <img src="images/pder2.JPG" height 100 width=500>
</p>

<p align="center">
	<img src="https://latex.codecogs.com/svg.latex?\Large&space;e^k" />  is the edge vector from node k-1 to node k. The unit vector is-
</p>

<p align="center">
	<img src="https://latex.codecogs.com/svg.latex?\Large&space;t^k=\frac{|\overline{e^k}|}{\|\overline{e^k}\|}" title="\Large x=\frac{-b\pm\sqrt{b^2-4ac}}{2a}" />
</p>

For simplicity, we assume N=4 (4 nodes and 3 links). The 3 links can independently stretch along their center line. Hence, the linear strain is given by-

<p align="center">
	strain = <img src="https://latex.codecogs.com/svg.latex?\Large&space;\|e^k\|-\|\overline{e^k}\|" /><br/>
</p>

Next we quantify the bending between adjacent links-
<p align="center">
	<img src="https://latex.codecogs.com/svg.latex?\Large&space;\varphi_k=\cos^{-1}{\left(t^{k-1}.t^k\right)}" /><br/>
	<img src="https://latex.codecogs.com/svg.latex?\Large&space;\kappa_k=2\ast\tan{(\frac{\varphi_k}{2})}" /><br/>
	where- <br/>
</p>


### 3. Motion as a combination of gaits
With the already developed feedback control algorithm and multiple open loop simulations, we quantify the distance the robot moves in a unit time. Hence, we get 3 possible motions. Forward, turn left and turn right (Although it is possible to move is numerour direction, we only consider three for simplicity).

Example: Move forward - turn left - move forward combination


### 4. Trajectory planning and control

The approach to trajectory control is to calculate a optimised path to the destination using the Hamilton-Jacobi-Bellman equation and then then develop a position-based feedback control to keep the snake on the path. With simplicity and time frame in mind, motion planning is done in a static environment. The position feedback can be a overhead camera that is trained to track the centre of mass of the robot. 

