# common-sensors

A collection of commonly used sensors: urdf files and a few tools

This package includes a variety of sensor models imported from different ROS packages available throughout the web.
I picked the best / most suitable models and copied them to this package, so they are all available in one location.
I may have edited the one or other model but at the time I didn't document which ones they were, and where I
originally got them from.

I also imported from Uni Texas: the FootprintFilter and NanToInfFilter. Here is their [LICENSE](https://github.com/utexas-bwi/segbot/blob/devel/LICENSE).

For now, this package does only exist so that simple sensor models can be used in the other packages without
the need to introduce a large set of ROS package dependencies just because of the URDF models of the sensors.


### Dependencies

- [shape_tools](http://wiki.ros.org/shape_tools)
- [laser_filters](http://wiki.ros.org/laser_filters)
- [openni_launch](http://wiki.ros.org/openni_launch)
- [common_sensors](https://github.com/JenniferBuehler/common-sensors)
    
**TODO** do we need this?

* pluginlib

**Install mandatory dependencies**

```
sudo apt-get install \
    ros-<distro>-shape-tools \
    ros-<distro>-laser-filters \
    ros-<distro>-openni-launch
```

**Install common-sensors**

Add the git repository to your catkin workspace:

```
cd <your-catkin-ws>/src
git clone https://github.com/JenniferBuehler/common-sensors.git
```

*Hint*: Alternatively to cloning the repositry directly into the catkin source folder, you
may also clone the repositories elsewhere and then create a softlink to the main folders
in your catkin source directory:    
``ln -s <path to common-sensors>`` 

**Compile**
 
To compile, you can now use catkin\_make as usual:

```
cd ..
catkin_make
```
