# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:

Use from robomaster import robot.

### Step2:

Choose the x,y,z - axis movement distance(meters).

### Step3:

Give ep_chassis.move to move straight.

### Step4:

Give time.sleep() for a break.
### Step5:

Give ep_chassis.drive_speed to have a circular movement.

## Program
```python
'''
Developed by: SARAVANAN G
Register Number: 23005445
'''
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.6, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=153,b=204,effect="on")

    ep_chassis.move(x=0.3, y=0, z=75, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    ep_chassis.move(x=1, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")

    ep_chassis.move(x=0, y=-1.6, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=153,effect="on")

    ep_chassis.move(x=0, y=0, z=-115, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=-1.4, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=1.45, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=153,b=255,effect="on")

    ep_chassis.move(x=2.03, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=153,effect="on")

    ep_chassis.move(x=0, y=0, z=80, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")

    ep_chassis.move(x=0.65, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=0,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![Untitled](https://github.com/Saravanan2512/mobilerobot-openloopcontrol/assets/144979117/648d9002-127a-4a11-8c1b-987ed34ca655)
![Untitled-1](https://github.com/Saravanan2512/mobilerobot-openloopcontrol/assets/144979117/eb133e1d-1937-42dc-ae1d-217d964de21a)









## MobileRobot Movement Video:
https://youtu.be/K35vxo9Al-o?si=Dqg0_vSv96A4Jx1_
Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE)


## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
