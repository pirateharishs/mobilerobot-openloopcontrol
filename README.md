# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

## Step1:
Use from robomaster import robot
## Step2:
Choose the x,y,z - axis movement distance(meters)
## Step3:
Give ep_chassis.move to move straight.
## Step4:
Give time.sleep() for a break
## Step5:
Give ep_chassis.drive_speed to have a circular movement.

## Program:

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

    ep_chassis.move(x=2.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=255,effect="on")

    ep_chassis.move(x=0.5, y=0, z=80, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=100,b=0,effect="on")

    ep_chassis.move(x=1.0, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=0, z=-118, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")
    
    ep_chassis.move(x=-1.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")
    
    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")
    

    ep_chassis.move(x=0, y=1.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=2.1, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=0, z=84, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0.6, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=150,g=150,b=150,effect="on")


    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![WhatsApp Image 2024-05-10 at 03 41 01_9700ba8d](https://github.com/Mario-Viofer-J/mobilerobot-openloopcontrol/assets/144979232/2ca1a7df-71ab-4958-905a-02dfccb60c3e)
<br/>
![WhatsApp Image 2024-05-10 at 03 41 01_0749d320](https://github.com/Mario-Viofer-J/mobilerobot-openloopcontrol/assets/144979232/75f6870a-5c29-43ea-9265-0f1bb2bfe1c8)
<br/>
![WhatsApp Image 2024-05-10 at 03 41 01_9b692e71](https://github.com/Mario-Viofer-J/mobilerobot-openloopcontrol/assets/144979232/a2636ed5-f4fa-4c22-952f-0372c7b86631)



## MobileRobot Movement Video:

## Url:https://youtu.be/IZzPEsh2DO8



## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
HARISH S (212223230071)
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
