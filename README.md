# Motion-Control-Using-Steper-Motor
Precisely control the motion of the CT-Scan bed in one dimension using a stepper motor and its driver
# Table of Centent
1.[Description](#1)
2.[Required Items/Devices](#2)
3.[Code](#3)
4. [Upgrade](#4) 

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
2. a Micro step Driver (ensure that the output power of the driverver is more than the required power of the stepper motor, the maximum amp should be higher)
3. Power supply with a voltage between 9-42 V.
4. Arduino UNO-R3
5. Wire 


![image](https://user-images.githubusercontent.com/108043716/177058386-6e176e1f-5c78-4db3-8cc0-cb3ebfb53584.png)
