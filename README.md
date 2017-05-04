# Robotic-team-project
We have 3 aspects to focus for this project


A. SmoothPathPlanner
=================


Here is an an example to generate a path using the default paramters. 

```java
//create waypoint path
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

<Example of Paths with different Paramters>
