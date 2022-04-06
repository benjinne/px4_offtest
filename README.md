# px4_offtest

`colcon build --symlink-install` then

In 3 terminals run the following:

```
source install/setup.bash
cd src/px4
HEADLESS=1 make px4_sitl_rtps jmavsim
```

```
source install/setup.bash
micrortps_agent -t UDP
```

Lastly, the offboard_control example can be run
```
source install.setup.bash
ros2 run px4_ros_com offboard_control
```
