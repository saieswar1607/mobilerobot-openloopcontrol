# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

### Step1: 
Start

### Step2: 
From robomaster import robot

### Step3: 
Intialize the type 

### Step4: 
Run the program to move the robo master through our condition

### Step5: 
Close

## Program
```
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    '''
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_chassis.move(x=2.7, y=0, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.move(x=0, y=0, z=45, xy_speed=1).wait_for_completed()

    ep_chassis.move(x=3.5, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=0, y=-0.5, z=0, xy_speed=0.75).wait_for_completed()

    ep_chassis.drive_speed(x=0.2,y=0,z=-10)
    time.sleep(20)
    ep_chassis.drive_speed(x=0,y=0,z=0)
    ep_chassis.move(x=0, y=0, z=30, xy_speed=0.75).wait_for_completed()
    ep_chassis.move(x=3, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_robot.close()
```

## MobileRobot Movement Image:

![starting](https://user-images.githubusercontent.com/93427011/154926774-4838bf2f-5a8e-43b9-ae08-7e1489fbcc49.jpeg)
![Ending](https://user-images.githubusercontent.com/93427011/154926801-03a34e7c-579b-433a-9d83-79ecee074895.jpeg)


## MobileRobot Movement Video:

https://youtube.com/shorts/IIlc7xhEsho?feature=share

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
