# Path Planning
## Introduction

Install Ubuntu Bionic docker image then install [ROS Melodic](http://wiki.ros.org/melodic/Installation/Ubuntu) into it, or directly install ROS Melodic from [Docker](https://hub.docker.com/r/tiryoh/ros-melodic-desktop).


```
catkin_create_pkg -D "A package which implements a path planning algorithm and shows its simulation." -l "BSD" --author "Felix Sihitshuwam" --maintainer "Felix Sihitshuwam" path_planning rospy roscpp std_msgs geometry_msgs tf2 tf2_ros
```

```
cd .. && catkin build
```
```
sudo apt-get install ros-melodic-jackal-desktop
```

```
git clone https://github.com/NicksSimulationsROS/multi_jackal.git
```


Install the following packages which `multi_jackal` depends on via `sudo apt-get install ros-melodic-`\
`controller-manager`\
`move-base`\
`interactive-marker-twist-server`\
`gazebo-ros-control`\
`hector-gazebo-plugins`\
`joint-state-controller`\
`diff-drive-controller`\
`sudo apt-get install ros-melodic-lms1xx`\
`pointgrey-camera-driver`\
`pointgrey-camera-description`
`global-planner`


```
catkin build path_planning
```

```
chmod +x multi_jackal_description/scripts/env_run
```

## Installing Mesh-Navigation
Run
```
sudo apt install ros-melodic-mesh-navigation
```

```
sudo apt install sudo apt install ros-melodic-robot-pose-ekf
sudo apt install sudo apt install ros-melodic-uos-common-urdf
```

Create an empty workspace, then clone `pluto-robot` in it
```
cd workspace/src
git clone https://github.com/uos/pluto_robot.git
cd .. && catkin build
```

Afterwards run the code below or one of the other simulations available [here](https://github.com/uos/pluto_robot)
```
roslaunch pluto_gazebo pluto_physics.launch
```

## References
1. [Jackal Simulation](https://www.clearpathrobotics.com/assets/guides/melodic/jackal/simulation.html)
2. [Multi Jackal](https://github.com/NicksSimulationsROS/multi_jackal)