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
𝑒^𝑘  𝑖𝑠 𝑡ℎ𝑒 𝑒𝑑𝑔𝑒 𝑣𝑒𝑐𝑡𝑜𝑟 | 𝑣𝑒𝑐𝑡𝑜𝑟 𝑓𝑟𝑜𝑚 𝑛𝑜𝑑𝑒 𝑘−1 𝑡𝑜 𝑛𝑜𝑑𝑒 𝑘.𝑡^𝑘  𝑖𝑠 𝑡ℎ𝑒 𝑢𝑛𝑖𝑡 𝑣𝑒𝑐𝑡𝑜𝑟 | 𝑡^𝑘=  (𝑒^𝑘 ) ̅/‖(𝑒^𝑘 ) ̅ ‖   

The model of the ell exhibits fore-and-aft symmetry. From, <cite paper>, we see that a simple travelling wave moving along the body of the robot leads to a net movement in the forward direction. Mathematically, the momentum produced by each of the links add-up and result in a net momentum. From the following animation and the coressponding plot of the centre of mass, we can see we can see the robot move when excited by a travelling wave. 

<img src="images/nodetraj_straight.JPG" width=1000 align=center>
<p align="center">
  <img src="images/swimmingEel_new.gif" height 100 width=500>
</p>


Next, we look to achieve a turning motion. By exciting the robot with an offsetted travelling wave, we can see that the robot moves on a curve, whose radius is proportinal to the angle of offset.

<p align="center">
  <img src="images/nodetraj_curved.JPG" width=400 align=center>
  <img src="images/swimmingEel_curved.gif" width=700 align=middle>
</p>

With the already developed feedback control algorithm and multiple open loop simulations, we quantify the distance the robot moves


### 3. Motion as a combination of gaits
With the already developed feedback control algorithm and multiple open loop simulations, we quantify the distance the robot moves in a unit time. Hence, we get 3 possible motions. Forward, turn left and turn right (Although it is possible to move is numerour direction, we only consider three for simplicity).

Example: Move forward - turn left - move forward combination


### 4. Trajectory planning and control

The approach to trajectory control is to calculate a optimised path to the destination using the Hamilton-Jacobi-Bellman equation and then then develop a position-based feedback control to keep the snake on the path. With simplicity and time frame in mind, motion planning is done in a static environment. The position feedback can be a overhead camera that is trained to track the centre of mass of the robot. 

