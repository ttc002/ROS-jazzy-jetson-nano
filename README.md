# ROS2 jazzy 
Create workspace
```
mkdir -p ros2_jazzy/src
cd  ros2_jazzy/src
```

Build cmake 3.27.9
```
wget https://github.com/Kitware/CMake/releases/download/v3.27.9/cmake-3.27.9.tar.gz
tar -xzvf cmake-3.27.9.tar.gz
cd cmake-3.27.9
./bootstrap && make -j$(nproc) && sudo make install
```

Update some packages
```
pip install --user --upgrade pybind11
sudo add-apt-repository ppa:lttng/ppa
sudo apt update
sudo apt install lttng-tools liblttng-ctl-dev
```

Pull ROS2
```
mkdir -p ~/ros2_jazzy/src
cd ~/ros2_jazzy
wget https://raw.githubusercontent.com/ros2/ros2/jazzy/ros2.repos
vcs import src < ros2.repos
```

Export
```
export LD_LIBRARY_PATH=/usr/local/lib
export PKG_CONFIG_PATH=/usr/local/lib/pkgconfig
export C_INCLUDE_PATH=/usr/local/include
export LIBRARY_PATH=/usr/local/lib
```


# Nav2
[intra_process_demo](https://github.com/ttc002/ROS-jazzy-jetson-nano/blob/main/docs/intra_process_demo.md)
# nav2 and SLAM toolbox
Install dependences
```
sudo apt install libboost-all-dev libsuitesparse-dev libgeographic-dev libceres-dev libgraphicsmagick++-dev libsqlite3-dev libzmq3-dev
```
Create workspace
```
mkdir -p ros2_nav/src
cd  ros2_nav/src
```
Add repositories
```
git clone --branch jazzy https://github.com/ros-navigation/navigation2
git clone --branch jazzy https://github.com/ros-planning/navigation_msgs.git
git clone --branch jazzy-devel https://github.com/cra-ros-pkg/robot_localization.git
git clone --branch jazzy https://github.com/ros2/demos.git
git clone --branch ros2 https://github.com/SteveMacenski/slam_toolbox.git
git clone --branch ros2 https://github.com/ros-geographic-info/geographic_info.git
git clone --branch jazzy https://github.com/ros2/geometry2.git
git clone --branch ros2 https://github.com/ros/bond_core.git
git clone --branch ros2 https://github.com/ros/angles.git
git clone --branch ros2-jazzy https://github.com/ros/diagnostics.git
git clone --branch 4.5.x https://github.com/BehaviorTree/BehaviorTree.CPP.git behaviortree_cpp
```
