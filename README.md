# Home service Robot Project

In this project, I build a home service robot using a turtlebot that autonomously navigate to transport objects from one location to another.

## Instructions

1. Place the files in the repo in the following directory structure **/home/workspace/catkin_ws/src/slam_project..**
2. Build the catkin workspace.
2. Navigate to the slam_project folder and run the following commands

Since these scripts were generated on a windows machine, you might need to install and run
```
sudo apt-get install dos2unix
dos2unix shellscript.sh
```
After that,
```
chmod +x slam_project.sh
./slam_project.sh
```
This will run rtabmap in the kitchen_dining gazebo world. To run rtabmap in the custom world, simply replace the world.launch command in the shell script with
```
roslaunch slam_project myworld.launch
```

Now, you can use the teleop keys given in the teleop.launch terminal to begin mapping the environment. To access the already generated maps for the environments [click here.](https://www.dropbox.com/s/t7d9el3rasf64pk/rtabmap-db.zip?dl=0)

**Notes**
1. If using a GPU workspace, make the following changes to the gazebo file.
   1. Change the sensor type of the hokuyo sensor from "ray" to "gpu_ray".
   2. Change the plugin file from "libgazebo_ros_laser.so" to "libgazebo_ros_gpu_laser.so"
2. Make sure you install rtabmap and all its dependencies before running this project. Instructions can be found in the ROS wiki pages.
