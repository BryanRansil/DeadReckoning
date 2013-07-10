DeadReckoning
=============

An experiment in placing 3d objects in real space with Dead Reckoning techniques

This project will combine several types of technologies together:

1. Accelerometer and Compass for movement detection.

2. OpenGL for 3d models and the camera. If we could input the accelerometer's readings directly into the camera that could show us some interesting results.

3. Cameras for seeing the scene.

Our priorities will be getting the first two components to work since movement detection and 3d are the two components we really need to work together.


Goal
--------------
The goal for this summer is to get an application which spawns an object in real space and allows the user to move around the object relatively smoothly. This involves moving the camera in OpenGL according to the movement readings.

Setup
--------------
**Main Activity** Operates many of the components, manages the operation.
 - (Static) **Movement Class** Combines the Accelerometer and Compass and presents the current position and acceleration to the Main Activity Class
 - (Static) **World Class**. Loads the 3d models we want to see. Displays them. Owns a Camera Preview object.
 - (Static) **Camera Preview Class**. Shows the real world. Only accessed by the World Class, because the World needs to set the background to be the current scene