# Euler Angles Tutorial

This demo uses Euler angles to describe an orientation in 3D space.

# About

This is a demonstration of using Euler angles (pronounced "oiler"-- by the way) to describe an orientation in 3D space. The demo contains 3 lines representing the 3 cardinal axes:	X (red), Y (green), and Z (blue). These can be rotated to any orientation.

Euler angles are 3 scalar values which measure angles. The first angle, the heading, measure the angle of rotation around the Y axis from the  initial orientation (the frame of reference created by the cardinal axes X,Y,Z) to the objects final orientation (X'Y'Z'). The second angle, the Elevation, measures  the angle of rotation around the X axis from the initial X-Z plane to the  X'-Z' plane created by the object's final orientation. The third and final angle, the Roll, is the angle of rotation around the Z' axis to reach the final orientation. It should be noted that the Z' axis is the Z axis of the object in worldspace,  not the Z axis of the world.

An interesting side effect of Euler angles is called Gimbal Lock, which is able to be experienced in this simulation. Gimbal lock is due to the fact that the axis of rotation of the heading never changes, but the axis of rotation of the Roll does. As a result of this, it is possible to cause the axis of rotation of the Roll to change in such a way that it has the same axis of rotation as the heading. When this happens a degree of freedom is lost and it is only possible to rotate about 2 linearly independent directions rather than 3.

In this simulation the Q and E buttons will alter the heading W and S will alter the pitch and A and D will alter the roll

In order to experience gimbal lock, alter the pitch using W or S such that the Z' axis (blue axis) is pointing straight up or straight down. Once this is achieved you can see that the Q and E buttons will accomplish the same action as the A and D buttons.

# Setup

In order to setup, run the following in a shell, then open the project in your preferred editor. Windows setup has been configured for use with Visual Studio.

Windows:
```
cd path/to/folder
setup.cmd
```
Linux:
```
cd path/to/folder
./setup
```

# Credits

For more reading, check out [3D Math Primer for Graphics and Game Development](http://www.amazon.com/Primer-Graphics-Development-Wordware-Library/dp/1556229119) by Fletcher Dunn & Ian Parberry
