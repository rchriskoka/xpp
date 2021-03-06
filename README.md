### <img src="https://i.imgur.com/ct8e7T4.png" width="20%" /> 

[![Build Status](http://build.ros.org/buildStatus/icon?job=Kdev__xpp__ubuntu_xenial_amd64)](http://build.ros.org/view/Kdev/job/Kdev__xpp__ubuntu_xenial_amd64/)
[![Documentation](https://img.shields.io/badge/docs-generated-brightgreen.svg)](http://docs.ros.org/kinetic/api/xpp/html/)
[![ROS hosting](https://img.shields.io/badge/ROS-integration-blue.svg)](http://wiki.ros.org/xpp)
[![License BSD-3-Clause](https://img.shields.io/badge/license-BSD--3--Clause-blue.svg)](https://tldrlegal.com/license/bsd-3-clause-license-%28revised%29#fulltext)

<img src="https://i.imgur.com/qI1Jfyl.gif"  width="60%"/>

Xpp is a [ROS package](http://wiki.ros.org/xpp) for the visualization of motion-plans for legged robots. It
draws support areas, contact forces and motion trajectories in RVIZ and displays URDFs for specific robots, including a one-legged, a two-legged hopper and [HyQ]. More example motions can be seen in this [video](https://www.youtube.com/watch?v=0jE46GqzxMM&feature=youtu.be), generated by the library [towr](https://github.com/ethz-adrl/towr).  


## Install
The recommended way to install is through the [ROS binaries](http://wiki.ros.org/xpp):
  ```bash
  sudo apt-get install ros-<ros-distro>-xpp
  ```

## Build from source
In case you don't want to install from the ROS binaries, this package requires [Eigen] and [ROS]:
  ```bash
  sudo apt-get install ros-<ros-distro>-desktop-full
  sudo apt-get install libeigen3-dev
  ```

Then you can build the package in your catkin workspace

  ```bash
  cd catkin_workspace/src
  git clone https://github.com/leggedrobotics/xpp.git
  cd ..
  catkin_make
  source ./devel/setup.bash
  ```

#### Unit Tests

Make sure everything installed correctly by running the unit tests through

    catkin_make run_tests
    
or if you are using [catkin tools].

    catkin build xpp_vis --no-deps --verbose --catkin-make-args run_tests


## Usage

A few examples for different robots are provided in the `xpp_examples` package, e.g.
[xpp_examples/src/monoped_pub.cc](https://github.com/leggedrobotics/xpp/blob/master/xpp_examples/src/monoped_pub.cc). For starters, run

    roslaunch xpp_examples hyq_bag.launch  // or any other launch file in this package
    
<img align="right" src="https://i.imgur.com/BzOnbkS.gif" />


## Add your own Robot
Want to visualize your own robot, then checkout these [instructions](http://wiki.ros.org/xpp#Visualize_.2BAC8_Contribute_your_own_robot) and we're happy to receive your pull-request.
See here the list of [contributors](https://github.com/leggedrobotics/xpp/graphs/contributors) who participated in this project.


## Authors 
[Alexander W. Winkler](https://www.alex-winkler.com) - Initial Work/Maintainer

The work was carried out at the following institutions:

[<img src="https://i.imgur.com/aGOnNTZ.png" height="45" />](https://www.ethz.ch/en.html "ETH Zurich") &nbsp; &nbsp; &nbsp; &nbsp; [<img src="https://i.imgur.com/uCvLs2j.png" height="45" />](http://www.adrl.ethz.ch/doku.php "Agile and Dexterous Robotics Lab")  &nbsp; &nbsp; &nbsp; &nbsp;[<img src="https://i.imgur.com/gYxWH9p.png" height="45" />](http://www.rsl.ethz.ch/ "Robotic Systems Lab")


## Citation
If you use this work in an academic context, please cite as follows:

    @misc{xpp_ros,
      author = {Alexander W. Winkler},
      title  = {{Xpp - A collection of ROS packages for the visualization of legged robots}},
      year   = {2017},
      doi    = {10.5281/zenodo.1037901},
      url    = {https://doi.org/10.5281/zenodo.1037901}
    }

##  Bugs & Feature Requests

Please report bugs, request features or ask questions using the [Issue Tracker](https://github.com/leggedrobotics/xpp/issues).

[HyQ]: https://www.iit.it/research/lines/dynamic-legged-systems
[ROS]: http://www.ros.org
[towr]: http://wiki.ros.org/towr
[rviz]: http://wiki.ros.org/rviz
[catkin tools]: http://catkin-tools.readthedocs.org/
[Eigen]: http://eigen.tuxfamily.org
[Fa2png]: http://fa2png.io/r/font-awesome/link/
