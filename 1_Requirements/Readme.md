# Requirements

# Wiper Control System

## Description

 - A Wiper Control System for an automotive wiper controls the operational speed of a wiper in accordance with rain conditions.It useful in the automotive unit the main purpose of the system is to clean the windscreen sufficiently to provide suitable visibility at all times.

## Features

 * If the User button is pressed Once, the red LED will be on    
 
 * If the User Button is pressed TWICE, Blue,Green,Orange LED's come ON at a time with set of frequency

 * If the User Button is pressed THIRD time, ON All LED's in CLOCKWISE manner an speeed will increase 

 * If the User Button is pressed FOURTH time ,all LED's on anticlock manner

 * If the User Button is pressed FIFTH time, the red LED will be off 

![Screenshot (105)](https://user-images.githubusercontent.com/62429376/167068935-6c3e8f17-1708-4a77-9bd0-ddd2fd4e5171.png)

## State of art

 * The main focus point is seeing the wiper control of the car.
 * And also seeing the seep of the wiper system in the car
 * Now this two features are explained in these project

# 5W's & 1H  

![Screenshot (104)](https://user-images.githubusercontent.com/62429376/167068196-569dce68-9ded-4259-8ef5-8cd52300e01f.png)

#  SWOT ANALYSIS 

![Screenshot (103)](https://user-images.githubusercontent.com/62429376/167066480-c12c3086-1d1b-426f-99c4-815b6db4368f.png)

## High level Requirements

  <html>
<body>
<!--StartFragment-->

ID | Description
-- | --
HLR-1 | User shall be able to ON the motor
HLR-2 | User shall be able to ON the wipers and controll the speed of wipers 
HLR-3 | User shall be able to OFF the wiper
HLR-4 | User shall be able to OFF the motor

<!--EndFragment-->
</body>
</html>

## Low level Requirements

<html>
<body>
<!--StartFragment-->

ID | Description
-- | --
LLR-1 | When user presses the switch for first time for two seconds, The Red LED is ON
LLR-2 | When user presses the button twice,  Blue, Green and Orange LEDs come ON one at a time with the set frequency, The frequency changes on every alternate key press, 3 frequency levels with 1, 4 and 8 Hz
LLR-3 | When user presses the button  fourth time The LED glow pattern stops 
LLR-4 | Again pressing the button for two seconds The Red LED is OFF

<!--EndFragment-->
</body>
</html>


## Best Methods To Be Followed

* Used functions to decrease dependency on main function
* Used Functions to accept the inputs from environmental conditions and store the values which helped in creating easy design of the system.
* comments have been placed only wherever necessary to avoid confusions
* Created header file so that the fuctions can be used else where ever required without any difficulty
