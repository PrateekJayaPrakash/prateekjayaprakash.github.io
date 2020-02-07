## Project Description

**Project description:** Aguilliform robots are essentially eel-like robots designed for improved underwater agility and efficiency. By quantifying their motion into gaits, we can use the symmetry of the underlying Lie brackets to develop an outer loop feedback control to control the path of the robot.

### 1. Dynamic model of an eel

Planar Discrete Elastic Rod theory is used to develop a dynamic model of a flexible eel robot. The model assumes that the the links are flexible and massless. The nodes carry all the mass, and consequently, the forces that act on the robot. We use a simplified fluid force model by [Kelasidi et. al](site it) to calculate the dynamic fluid force acting on the nodes. The flexible links experience a force due to relative stretching and bending which interact with the fluid forces to generate motion.

### 2.Quantifying motion into gaits

The model of the ell exhibits fore-and-aft symmetry. From, <cite paper>, we see that a simple travelling wave moving along the body of the robot leads to a net movement in the forward direction. Mathematically, the momentum produced by each of the links add-up and result in a net momentum. From the following animation and the coressponding plot of the centre of mass, we can see we can see the robot move when excited by a travelling wave. 

<img src="images/nodetraj_straight.JPG" width=1000 align=center>
<p align="center">
  <img src="images/swimmingEel_new.gif" height 100 width=500 align=middle>
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

