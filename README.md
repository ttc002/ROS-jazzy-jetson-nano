# ROS2 jazzy 
[intra_process_demo](https://github.com/ttc002/ROS-jazzy-jetson-nano/blob/main/docs/intra_process_demo.md)
# nav2 and SLAM toolbox
install dependences
```
sudo apt install libboost-all-dev libsuitesparse-dev libgeographic-dev libceres-dev libgraphicsmagick++-dev libsqlite3-dev
```
create workspace
```
mkdir -p ros2_nav_slam/src
cd  ros2_nav_slam/src
```
add repositories
```
git clone --branch jazzy git@github.com:ros-planning/navigation2.git
git clone --branch jazzy git@github.com:ros-planning/navigation_msgs.git
git clone --branch v4.3.2 git@github.com:BehaviorTree/BehaviorTree.CPP.git
git clone --branch ros2 git@github.com:SteveMacenski/nav_2d_msgs.git
git clone --branch ros2 git@github.com:cra-ros-pkg/robot_localization.git
git clone --branch ros2 git@github.com:ros2/demos.git demos_ros2
git clone --branch jazzy git@github.com:SteveMacenski/slam_toolbox.git
git clone --branch ros2 git@github.com:ros-geographic-info/geographic_msgs.git
git clone --branch jazzy git@github.com:ros2/geometry2.git
git clone --branch jazzy git@github.com:ros2/common_interfaces.git common_interfaces_ros2
git clone --branch ros2 git@github.com:ros/bond_core.git
git clone --branch ros2 git@github.com:ros/angles.git
git clone --branch ros2 git@github.com:ros/diagnostics.git
git clone --branch 4.5.x git@github.com:BehaviorTree/BehaviorTree.CPP.git behaviortree_cpp
```
