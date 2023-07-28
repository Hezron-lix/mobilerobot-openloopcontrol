# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: 
Import the necessary modules for controlling the RoboMaster robot and working with the camera.
Step2:
Initialize the connection to the RoboMaster robot using Wi-Fi access point mode (AP mode).
Step3:
Start the video streaming and display the video.
Step4:
Move the robot in a specified direction with a given distance and speed to go along the required path, then set the LED color to a specific combination.
Step5:
Close the connection to the RoboMaster robot.

## Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)


    ep_chassis.move(x =2.8,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")
    
    ep_chassis.move(x =0,y=0,z=50,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x =0.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x =0,y=0,z=50,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x =0.8,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=128,g=128,b=0,effect="on")

    ep_chassis.move(x =0,y=0,z=80,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x =1.4,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=128,g=255,b=0,effect="on")

    ep_chassis.move(x =0,y=0,z=-45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x =1.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=0,effect="on")

    ep_chassis.move(x =0,y=0,z=45,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=128,b=0,effect="on")

    ep_chassis.move(x =1.5,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=255,effect="on")
    
    ep_chassis.move(x =0,y=-0.3,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x =0,y=0,z=95,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x =1.7,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x =0,y=0,z=70,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=0,effect="on")

    ep_chassis.move(x =0.7,y=0,z=0,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on") 

    ep_chassis.move(x =0,y=0,z=20,xy_speed=0.75).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on") 

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
  
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![robo](/WhatsApp%20Image%202023-07-27%20at%2020.30.34.jpg)

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](https://youtu.be/VmRIhdaA5ZM)


## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
