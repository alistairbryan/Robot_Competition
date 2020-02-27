# Engineering Physics Robotics Competition

## Summary
Collaboratively designed, prototyped, and built an autonomous robot, with the goal of navigating a complex course, collecting difficult-to-access objects, and depositing them in a remote and unforgiving receptacle.

[TV Coverage](https://www.facebook.com/BTCityNewsVAN/videos/583404632190468/?t=0)

## Robot Overview
Two independent STM32 MCUs operated the arm and driving systems respectively. An array of IR sensors were used to detect black electrical tape beneath the robot, which was processed by a PID controller to enable navigation.

The claw moved on both horizontal and vertical lead screws, and its pincers were linearly actuated by a servo motor.

Limit switches were placed on the front of the robot to detect collisions with posts, the scoring area, or other robots.

## Navigation System
Designed the navigation system to track position by counting the number of tape junctions passed in a round. With this, it could determine where the robot was on the course, and thus which way it should turn at junctions.

When the arm came into contact with an object, the Master BluePill communicated with the BluePill controlling the arm; this was done by manipulating the voltages of mutually connected regions. The arm BluePill then subsequently indicated whether an attempt to grab an object was successful. 
