## Project Description

**Project Objective:** To Model an underwater snake robot based on PDER framework and develop feedback algorithms based on distributed control to correct the trajectory of the robot.
(PDER- Planar Discrete elastic rod)

### 1. Why elastic links?

Traditionally, robots are made of rigid links with angular control of node angles. With this framework, there is a major restriction on the 
rigidity of the robot and contact forces are difficult to model. 
By using elastic links with direct control on the shape of the robot, we can achieve the same goal of locomotion with additional advantages-
1. Elastic links allow for an inbuild pneumatic buayancy controller where the buoyancy can be varied by pumping air into the flexible   links.
2. Elastic links offer a wide range of applications in search and rescue operations. (Ability to access tight areas)
3. Elastic links allow for better gripping of obects. One possible application of this robot can be to grip objects using a few links and then using the rest of the body to propel the payload to any required target.

[An example of this buoyancy and shape control](https://youtu.be/1sJJOY3BnEQ).Credit to Dr. Derek Paley and team at the CDCL lab, University of Maryland.


### 2. Why distributed control?

A set of nodes can be treated as a multiagent system with physical and control coupling. The physical coupling is fixed with each node attached to its neighbors. The control coupling,however, is flexible and based on the approach can be coupled as desired. This coupling lets us use distributed control to have nodes make low level decisions with the data from other control coupled nodes and reach a desired concensus.

The desired consensus here is that the nodes oscillate at a fixed amplitude and frequency but with a phase difference that results in a travelling wave motion which results in forward motion.

### 3. Open Loop results

<img src="images/dummy_thumbnail.jpg?raw=true"/>

### 4. Approach to control

After stable open loops results, we proceed to closed loop control. We proceeded with eigenstructure reassignment.

EIGENSTRUCTURE assignment is a classical design methodology used to specify (a subset of) closed-loop eigenvalues and associated eigenvectors to achieve a desired behavior for a linear system. The results are promising.

### 5. Closed Loop results

The results will be posted in this section once the paper is published.

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
