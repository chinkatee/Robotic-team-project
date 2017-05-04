# Robotic-team-project
We have 3 aspects to focus for this project


A. SmoothPathPlanner
=================


Here is an an example to generate a path using the default paramters. 

```java
//example create waypoint path
double[][] waypoints = new double[][]{
	{1, 1},
	{5, 1},
	{9, 12},
	{12, 9},
	{15, 6},
	{19, 12}
}; 

double totalTime = 8; //max seconds we want to drive the path
double timeStep = 0.1; //period of control loop on Rio, seconds
double robotTrackWidth = 2; //distance between left and right wheels, feet

FalconPathPlanner path = new FalconPathPlanner(waypoints);
path.calculate(totalTime, timeStep, robotTrackWidth);
```

B. Localisation using enchanced filter
=================

Class
Publisher
Subscriber



> Note: This algorithm does consider pat of the robot. What that means is it does require an initial or final orientation of the robot, and it gurantee the final orientation. Once you reach the desintation, you may need to use navigation command on your chassis to rotate to the desired final heading.

Assumptions
=========================
1. Robot Chassis is a skid-steer platform
2. Ground robot is to travel on is considered to be an even plane, with no hills, ramps, bumbs, or other obstacles
3. Robot has independant speed controllers for both sides of the Robot Chassis, tuned to meet the velocity profile changes
4. Sufficient time is given for the robot to complete the path. 
