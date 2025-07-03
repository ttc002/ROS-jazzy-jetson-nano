# ROS2 jazzy 
create workspace
```
mkdir -p ros2_jazzy/src
cd  ros2_jazzy/src
```
build cmake 3.27.9
```
wget https://github.com/Kitware/CMake/releases/download/v3.27.9/cmake-3.27.9.tar.gz
tar -xzvf cmake-3.27.9.tar.gz
cd cmake-3.27.9
./bootstrap && make -j$(nproc) && sudo make install
```
pull ROS2
```
mkdir -p ~/ros2_jazzy/src
cd ~/ros2_jazzy
wget https://raw.githubusercontent.com/ros2/ros2/jazzy/ros2.repos
vcs import src < ros2.repos
```



# Nav2
[intra_process_demo](https://github.com/ttc002/ROS-jazzy-jetson-nano/blob/main/docs/intra_process_demo.md)
# nav2 and SLAM toolbox
install dependences
```
sudo apt install libboost-all-dev libsuitesparse-dev libgeographic-dev libceres-dev libgraphicsmagick++-dev libsqlite3-dev libzmq3-dev
```
create workspace
```
mkdir -p ros2_nav/src
cd  ros2_nav/src
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
git clone https://github.com/ros-geographic-info/geographic_info.git
```
