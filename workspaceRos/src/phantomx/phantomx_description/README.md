# PhantomX Description

ROS package providing mesh files and URDF of the Phantom X Hexapod robot for use with the real robot or Gazebo.
URDF contains joint transmissions for controllers and Gazebo referenced plugins for camera and the IMU provided by hector_gazebo.


## Usage

You can display the robot in Rviz with:
    
    roslaunch phantomx_decription display.launch


You can load the robot's description and start the Robot State Publisher in a `launch` file with:

```xml
<include file="$(find phantomx_description)/launch/description.launch"/>
```


## License

This software is provided by Génération Robots http://www.generationrobots.com and HumaRobotics http://www.humarobotics.com under the Simplified BSD license
