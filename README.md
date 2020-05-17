# CarND_Capstone
## Setup
During this session the workspace offered by Udacity is used. First, the workspace needs to be set up: 
```python
git clone https://github.com/udacity/CarND-Capstone.git
pip install -r requirements.txt
```
The next step is to install catkin project
```python
cd ros
catkin_make
source devel/setup.sh
roslaunch launch/styx.launch
```
If an error `-- Could not find the required component 'dbw_mkz_msgs'. The following CMake error indicates that you either need to install the package with the same name or change your environment so that it can be found.
CMake Error at /opt/ros/kinetic/share/catkin/cmake/catkinConfig.cmake:83 (find_package):
  Could not find a package configuration file provided by "dbw_mkz_msgs" with
  any of the following names: …"` occurs, a new install of ros-kinetic-dbw-mkz-msgs will help: 
```python
sudo apt-get update
sudo apt-get install -y ros-kinetic-dbw-mkz-msgs
cd /home/workspace/CarND-Capstone/ros
rosdep install --from-paths src --ignore-src --rosdistro=kinetic -y
```
