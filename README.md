# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
Step1:

Initiate the MobileRobot.

Step2:

Connect your PC with the MobileRobot.

Step3:

Open Python program.

Step4:

Program the movements of the robot using python code.

Step5:

Execute the python program.

## Program
```
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

    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_chassis.move(x=0.9, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-80, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=0,effect="on")

    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=-65, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x=0.5, y=0, z=0, xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x=0, y=0, z=-40, xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x=1, y=0, z=0, xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")
    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
    ep_chassis.move(x=1.1, y=0 , z=0, xy_speed=1).wait_for_completed()
 
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=0, y=0 , z=41, xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=1.5, y=0, z=0,xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=0, y=0, z=-47,xy_speed=1).wait_for_completed()
    
    ep_led.set_led(comp = "all",r=255,g=153,b=204,effect="on")
    ep_chassis.move(x=0.6, y=0, z=0,xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=51,g=204,b=204,effect="on")
    ep_chassis.move(x=0, y=0, z=-45,xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=0.6, y=0, z=0,xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")
    ep_chassis.move(x=0, y=0, z=-80,xy_speed=1).wait_for_completed()

    ep_led.set_led(comp = "all",r=51,g=51,b=153,effect="on")      
    ep_chassis.move(x=2.8, y=0, z=0,xy_speed=1).wait_for_completed()

    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

strting point image:
![startingpoint](https://github.com/Gokulanbazhagan/mobilerobot-openloopcontrol/assets/119518996/68f39f22-0d79-4051-a6ff-9a460555fdbd)
momenting point image:
![mobilerobotmovement](https://github.com/Gokulanbazhagan/mobilerobot-openloopcontrol/assets/119518996/053d0842-c734-4740-a6f9-f4750bb4e13c)





## MobileRobot Movement Video:

video-id:
https://youtu.be/JI9PzVFJESU



## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
