Need 1 to send and 1 (or more) to receive

To change settings Pin SET needs to be LOW. To activate Serial Pin CS needs to be LOW.

Connect  power and TX/RX. When you set CS to LOW, it will send "Wake" to serial port.  This is standard transparent mode.

If you want to change settings make pin SET LOW. Now you can send AT commands
eg. Send AT+CLSSC1 and it needs a carridge return, to send all GPIOs as input (button to LOW) 

Serial communication (9600 baud standard, up to 19200) over 2.4Mhz

Can send serial to serial (transparent mode) standard CS-pin = LOW for both JDY-40's

Can send IO-pin to IO-pin (CLSS = C0 or C1 for sender and CLSS = C2 ... C5 for receiver.) CS-pin = HIGH for both (not connected)

Can send IO-pin to serial (CLSS = C0 or C1 for sender and CLSS = C2 ... C5 for receiver) CS-pin = HIGH for sender, Low for receiver.
	You will get something like 03 AA 01 01 03 AA 01 00 (03 AA IO-pin state) here I am using C4 on receiver GPIO1 LOW (active button) GPIO1 HIGH button released

Probably also serial to IO-pin, but not tested by me (yet)


Most common uses will be 
	transparent, both devices on CLSS A0
	IO-pin button to receiver output,  sender = CLSS C1 and receiver CLSS C4 is the simpelest version. Button pushed on sender, output HIGH on receiver. Button released and output goes LOW.
	
		C5 push button on sender and output goes HIGH. Release and it stays HIGH. New push will make it go LOW.
		C2 button push gives a pulse of 30 ms LOW to HIGH puls
		C1 button push gives a pulse of 30 ms HIGH to LOW puls