# px4_offtest

`colcon build --symlink-install` then

In different terminals run the following:

```
source install/setup.bash
cd src/px4
HEADLESS=1 make px4_sitl_rtps jmavsim
```

```
source install/setup.bash
micrortps_agent -t UDP
```

Lastly, verify topics are being received and run the example

```
ros2 topic list
ros2 topic echo _any topic_
```

```
source install.setup.bash
ros2 run px4_ros_com offboard_control
```
