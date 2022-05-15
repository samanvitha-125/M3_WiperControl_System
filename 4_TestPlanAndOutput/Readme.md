# HIGH LEVEL TEST PLAN 
 
<html> 
<body> 
<!--StartFragment--> 
 
Test ID | Description | Input | Expected output | Actual Output | status 
-- | -- | -- | -- | -- | -- 
01 | Ignition On |  Pressing Button 1st 2sec  | key status | Key Status Displayed |✅ 
02 | Wiper On | Pressing user button once | Wiper Status-1Hz | Wiper Status Displayed |✅ 
03 | Wiper On | Pressing user button twice | Wiper Status-4Hz | Wiper Status Displayed |✅ 
04 | Wiper On | Pressing user button thrice | Wiper Status-8Hz | Wiper Status Displayed |✅ 
05 | Ignition Off | Pressing Button 1st 2sec  | Ignition key status | key status Displayed |✅ 
 
<!--EndFragment--> 
</body> 
</html> 
 
 
# LOW LEVEL TEST PLAN 
 
<html> 
<body> 
<!--StartFragment--> 
 
Description | Input | Expected output | Actual Output | Status 
-- | -- | -- | -- | --  
ignition_on() | User Button Press 1st 2sec | RED LED ON | RED LED ON | ✅ 
LED cycle | Button Press once | All LEDs ON | All LEDs ON | ✅ 
LED cycle | Button Press twice | All LEDs ON | All LEDs ON | ✅ 
LED cycle | Button Press thrice | All LEDs ON | All LEDs ON | ✅ 
ignition_off() | User Button Press 2nd 2sec | RED LED OFF | RED LED OFF | ✅ 
 
<!--EndFragment--> 
</body> 
</html>


## Scenario:
* Ignition Key Position at ACC: The Red LED is ON, if the user button is pressed and held for 2 secs
* Wiper ON: On press of the user input, Blue, Green and Orange LEDs come ON one at a time with the set frequency, The frequency changes on every alternate key press, 3 frequency levels with 1, 4 and 8 Hz
* Wiper OFF: The LED glow pattern stops on the 4th press; the wiper action starts next press onwards as mentioned in step 2
* Ignition Key Position at Lock: The Red LED is OFF, if the user button is pressed and held for 2 secs

# OUTPUT VIDEO

https://user-images.githubusercontent.com/62429376/167387308-8435a9da-6f4e-4c11-9b20-61ad71fd8822.mp4

# OUTPUT DIAGRAM

## Switch turned off

![Screenshot (106)](https://user-images.githubusercontent.com/62429376/167388539-46c3632a-74a7-4bb7-98e7-c61324d76512.png)

## Ignition Key Position at ACC:

![Screenshot (107)](https://user-images.githubusercontent.com/62429376/167388545-68d0f225-2156-428b-b6a4-75d02bdfbbe0.png)

## Wiper turned on

![Screenshot (118)](https://user-images.githubusercontent.com/62429376/167388551-79b6e314-6096-4fb6-b4f4-e77c11f0b8f7.png)

![Screenshot (108)](https://user-images.githubusercontent.com/62429376/167388573-d8571493-41e5-4ee0-bc5c-880269ca364c.png)

![Screenshot (109)](https://user-images.githubusercontent.com/62429376/167388580-201eabda-fc25-4392-a033-f771ac987651.png)

![Screenshot (111)](https://user-images.githubusercontent.com/62429376/167388586-f24716fb-45ff-431e-99f5-8524efe7ee65.png)

![Screenshot (113)](https://user-images.githubusercontent.com/62429376/167388591-113e5008-3f21-4928-9edf-5aa9fde7c836.png)

![Screenshot (114)](https://user-images.githubusercontent.com/62429376/167388596-ccefc6a7-1a24-4d43-86cf-8208a7d20ff7.png)

## Wiper turned off

![Screenshot (107)](https://user-images.githubusercontent.com/62429376/167388545-68d0f225-2156-428b-b6a4-75d02bdfbbe0.png)

## Ignition Key Position at Lock:

![Screenshot (106)](https://user-images.githubusercontent.com/62429376/167388539-46c3632a-74a7-4bb7-98e7-c61324d76512.png)
