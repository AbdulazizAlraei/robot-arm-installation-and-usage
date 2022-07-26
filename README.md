# robot-arm-installation-and-usage
the steps of installing and using the robot arm.

## First installation steps:
install the package for noetic distro by typing these commands in the terminal :
```
sudo apt-get install ros-noetic-moveit
```
```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
```
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
then
make a directory for catkin_ws
```
mkdir -p ~/catkin_ws/src
```
then
```
catkin_make
```
then
```
cd ~/catkin_ws/src
```
then
get a clone of https://github.com/smart-methods/arduino_robot_arm.git inside the file
```
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```
then
```
cd ~/catkin_ws
```
then
```
rosdep install --from-paths src --ignore-src -r -y
```
then 
```
sudo nano ~/.bashrc
```
at the end of the (bashrc) file add the follwing line
(source /home/wesam/catkin_ws/devel/setup.bash)
then 
ctrl + o
then
```
source ~/.bashrc
```

## Second for configuring arduino with ROS:

Install Arduino IDE in Ubuntu https://www.arduino.cc/en/software to install run
```
sudo ./install.sh after unzipping the folder
```
Install the arduino package and ros library by running
```
sudo apt-get install ros-noetic-rosserial-arduino
```
```
sudo apt-get install ros-noetic-rosserial
```
then
install ros_lib into the Arduino Environment
```
cd <sketchbook>/libraries
```
```
  rm -rf ros_lib
```
```
rosrun rosserial_arduino make_libraries.py .
```


## Third usage:

## Controlling the robot arm by joint_state_publisher
```
roslaunch robot_arm_pkg check_motors.launch
```
after running this command you will git this page:

![لقطة الشاشة 2022-07-26 213956](https://user-images.githubusercontent.com/109360750/181086689-bf639e99-1f89-4d61-9397-cfdfb6ee59a7.png)







