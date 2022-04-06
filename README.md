# px4_offtest

`colcon build --symlink-install` then

In different terminals run the following:

```
source install/setup.bash
cd src/Px4
HEADLESS=1 make px4_sitl_rtps jmavsim
```

```
source install/setup.bash
micrortps_agent -t UDP
```

Lastly, verify topics are being received and run the example

```
ros2 topic list (try again if not all were shown)
ros2 topic echo /fmu/vehicle_status/out
```

```
source install.setup.bash
ros2 run px4_ros_com offboard_control
```
