A clock with analog volt meters as the display, and an internet connection to obtain the time via NTP 

This project is based on an Arduino Mega (any Arduino will work), an ethernet shield, and 3 analog volt/amp meters. The ethernet shield is used to connect to the internet and obtain the time from an NTP server. The time is obtained once a second, converted to hours, minutes and seconds, and then each value is converted to a relative voltage (0 to 5vdc) using the PWM feature of the Arduino. These voltages are then output to the analog meters, representing hours, minutes and seconds. New meter dials are printed with custom dial software from Tonne Software (www.tonesoftware.com) to create the meter faces, with the three meters reading hours, minutes and seconds, along with the appropriate timescales. The meters are then housed in a wooden project box from Hobby Lobby.
The software algorithm is relatively simple:
1.	Obtain the time from the NTP server using off the shelf open source software for the Arduino (code is included in the program available on this site).
2.	Convert the NTP time into hours, minutes and seconds
3.	Convert each of the 3 outputs (hours, minutes and seconds) to a voltage between 0 and 5v to drive the meter needles to the correct position. The values for each position of the hour, minutes and seconds are contained in a lookup table for each meter. In order to properly scale the meters, as they all have unique internal resistances, an external resistor and potentiometer are placed in series with each of the meters to normalize the values and have the meter track the scale properly.
In this case, each of the meters is 3½” in diameter (including the bezel), and the project box is 13½” long by 4" high by 3½“deep. There are 2 external connections, a USB cable for programming and power, and an internet cable.
This project works equally well with a multitude of time sources including GPS receivers and small clock modules.
I’ve included clock faces which will fit Weston analog panel meters (3 ½ “ in diameter with bezel). Other faces can be custom made using the software above, or by contacting me directly.
