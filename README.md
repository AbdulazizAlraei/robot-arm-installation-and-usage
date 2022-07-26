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








