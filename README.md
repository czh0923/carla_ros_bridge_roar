1. carla_ros_bridge colcon build, setuptool deprecation warning

pip install setuptools==58.2.0 \
https://answers.ros.org/question/396439/setuptoolsdeprecationwarning-setuppy-install-is-deprecated-use-build-and-pip-and-other-standards-based-tools/


2. pip install carla, module "platform" has no attribute "dist" 

because python version >= 3.8, dist is deprecated, just lower python version


3. connecting to 337d, berkeley major map, timeout error

don't use Calvisitor

### connecting to 337d, berkeley major map, map not found error 
comment out everything in carla_ros_bridge/bridge.py that mentions Towns

### connecting to 337d, berkeley major map, version mismatch error 
pip install carla==0.9.12\
if gotton Client=0.9.12, while simulator=0.9.12-dirty warning, that is fine, it's only a warning, it's already connected. \
If client version 0.9.13, an easy fix is to go into bridge.py and comment out lines exits the program is version mismatches.


if inside conda environment, ros2 launch in terminal gives import carla error, while opening python in terminal and running import carla is fine \
deactivate conda, redo pip install carla

other fixes to try:\
run map with -prefernividia