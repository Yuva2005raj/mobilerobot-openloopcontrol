# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1:

Use from robomaster import robot

### Step2:

Choose the x,y,z - axis movement distance(meters).

### Step3:

Give ep_chassis.move to move straight.

### Step4:

Give time.sleep() for a break.

### Step5:

Give ep_chassis.drive_speed to have a circular movement

## Program

```

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
    ''' 
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5] 
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second)  [0.5,2]

    '''
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=51,b=0,effect="on") 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=255,b=255,effect="on") 
    ep_chassis.move(x=1.8, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=50, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=102,b=0,effect="on") 
    ep_chassis.move(x=2.2, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-40, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on") 
    ep_chassis.move(x=2.4, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-45, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=255,g=0,b=0,effect="on") 
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-100, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=255,b=255,effect="on") 
    ep_chassis.move(x=5.7, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=128,b=128,effect="on") 
    
    


   



    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")
    ep_robot.close()
    
```    
    
    

## MobileRobot Movement Image:

![image](https://github.com/Yuva2005raj/mobilerobot-openloopcontrol/assets/118343998/aa5bde56-eedb-4e10-a2dc-1bf79a5f8cc5)


## Movement images:
![image](https://github.com/Yuva2005raj/mobilerobot-openloopcontrol/assets/118343998/4347188e-f753-45f6-99f8-8d42d5507e14)
![image](https://github.com/Yuva2005raj/mobilerobot-openloopcontrol/assets/118343998/f1576e1d-370a-482b-9c14-ef88e98573cb)
![image](https://github.com/Yuva2005raj/mobilerobot-openloopcontrol/assets/118343998/663738c7-371c-4c79-a4fc-d4aa4fae4180)


## MobileRobot Movement Video:
https://youtube.com/shorts/RQaaCqOnsjU?feature=share


## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
