# Motion-Control-Using-Steper-Motor
Precisely control the motion of the CT-Scan bed in one dimension using a stepper motor and its driver
# Table of Centent
1. [Description](#1)
2. [Required Items/Devices](#2)
3. [Code](#3)
4. [Upgrades](#4) 
<a name="1"></a>
# Description
I would like to share another automation/instrumentation project that can be done to precisely control a motion of a piece of equipment, for example, a CT-Scan bed. As you may know, the CT-Scan bed should more very accurate in order to capture enough scans from different parts of the object. Since the rotation of CT-Scan should be coupled with bed motion to produce a full scan, not only from a cross-section of the object but also from a whole length of the object, a stepper motor should be used for this purpose. If you are familiar with a Stepper motor, you can realize that a stepper motor can produce a smooth, accurate, and controllable motion where the speed of motor rotation can be adjusted using the motor driver setting.
In this project, we are going to utilize a stepper motor and develop software which enables the operator to work with a stepper motor. The following is the list of features for the developed code:
1. Determine the number of steps, according to the configuration of the Microstep Driver.
2. Change the direction of the motor from clockwise to anticlockwise rotation.
3. Determine the number of remaining steps to finish the command
4. Stop and rerun the motor while performing a motion.
5. Lock the motor to fix the position of the bed.

<a name="2"></a>
# Required Items/Devices
If you wish to accomplish this project, make sure that the following items are ready:
1. a Steper motor (e.g. 17HS4401)
2. a Micro step Driver (ensure that the output power of the driver is more than the required power of the stepper motor, the maximum amp should be higher)
3. Power supply with a voltage between 9-42 V.
4. Arduino UNO-R3
5. Wire 

<img src="https://user-images.githubusercontent.com/108043716/177061004-4c16ad69-c67a-42cb-b3f2-f1e66fe4b45a.png" width="200" /> <img src="https://user-images.githubusercontent.com/108043716/177061011-0b153606-9755-480f-8bbb-7e3f92e1c12b.png" width="200" /> <img src="https://user-images.githubusercontent.com/108043716/177061021-b74468a6-0cb7-447d-8f01-d193f5420af3.png" width="200" /> <img src="https://user-images.githubusercontent.com/108043716/177061037-20247f0f-f90c-4b71-9127-d5e2a4a6bc65.png" width="200" />

Fig 1. Required devices to initiate a motion control of a stepper motor.

<a name="3"></a>
# Code
Although LabView computer coding software is used here to write the suitable code for motion control, it is not bad idea to generate the same type of code in Python language as well. Since the instrument is connected via USB to the computer, there is no need for furthur configuration to define Arduino UNO-R3. The following figures show the code in LabView as well as the control panel of the developed software. 

![image](https://user-images.githubusercontent.com/108043716/177061257-2623ee32-3e24-4567-bac0-755f04dd3b35.png)

Fig 2. Developed code for the project in LabView computer coding software.

<img src="https://user-images.githubusercontent.com/108043716/177058386-6e176e1f-5c78-4db3-8cc0-cb3ebfb53584.png" width="400" />

Fig 3. The control panel of the developed software for the motion control of a stepper motor.

As can be seen in the control panel, there are four buttons involved in this code with the following actions:
1. Left/Right: In order to change the direction of the rotation, clockwise or anticlockwise
2. Eliminate: In order to stop the software properly by closing the Visa Resource
3. Reset Steps: In order to reinitiate the number of steps for rotation.
4. Run/Stop: In order to stop or rerun the motor. Note that by enabling the stop button, the gear inside the motor will be locked.

<a name="4"></a>
# Upgrades
This software can be upgraded to run three stepper motors at the same time to creat the motion in three dimensions, x-axis, y-axis, and z-axis. Also, other automation can be done. By expansing the code, you can generate a software for a 3D-printer using three stepper motors.
