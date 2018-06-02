# LPGedia

LPG GAS LEAKAGE DETECTION AND MANAGEMENT DEVICE 

Salient Features: 

 It detects the leakage of LPG gas. 
 
1. When there is a leakage, it first turns off the regulator using servo motor if regulator is on. 

2. It turns on the buzzer. 

3. Message “Leakage detected!!” is displayed on LCD attached to the device. 
 
 It displays the current Temperature and Humidity. 
 
 It displays the current amount of LPG Gas (in Kg) available in the cylinder. 
 
 It tells the user how much gas was wasted due to leakage. 
 
 It tells the user how much gas was consumed while cooking. 
 
 If the amount of gas in the cylinder falls below a minimum threshold, it displays on LCD to replace the cylinder. And even if user starts cooking, Buzzer starts beeping just to make user aware of this. 


Requirements: 

 Arduino Mega 2560 

 Arduino IDE 

 OS: Windows/Ubuntu 

 MQ5 Gas Sensor 

 Buzzer v1.2 

 Servo Motor (SG90)

 Temperature and Humidity Sensor 

 Load Sensor 

 HX711 Amplifier 

 20*4 LCD Display 

 Breadboard 

 Jumper Wires 



Implementation:

Step 1: Interface an LCD Display with an Arduino 
 
   LCD Pins                          Arduino Pins 
   
     GND             -->>              GND    
	 
     Vcc             -->>              5V 
	 
     VEE             -->>              GND 
	 
     RS              -->>              Digital Pin 7 
	 
     R/W             -->>              GND 
	 
     EN              -->>              Pin 6 
	 
     DB0 – DB3       -->>              Leave 
	 
     DB4 – DB7       -->>              Pin 5 – Pin 2 respectively 
	 
     Led +           -->>              5V 
	 
     Led -           -->>              GND 

Step 2: Interface MQ5 Gas Sensor with Arduino

            MQ5                         Arduino 
			
            SIG           -->>           A0 
			
            NC            -->>           Leave 
			
            Vcc           -->>           5V 
			
            GND           -->>           GND 
			
Step 3: Interface Buzzer with an Arduino
 
           Buzzer                       Arduino
		   
            SIG           -->>           Pin 8 
			
            NC            -->>           Leave 
			
            Vcc           -->>           5V
			
            GND           -->>           GND
			
Step 4: Interface Temperature Sensor with Arduino    

           DHT 11                       Arduino 
		   
            SIG           -->>           A1 
			
            NC            -->>           Leave 
			
            Vcc           -->>           5V
			
            GND           -->>           GND 
       
 
Step 5: Interface Servo Motor with an Arduino 

           Motor                        Arduino 
		   
         Orange Wire      -->>           Pin 9 
		 
         Red Wire         -->>           5V 
		  
         Brown Wire       -->>           GND 
 
Step 6: Interface Load Cell with HX711 Amplifier 

           Load Cell                    HX711 
		   
         Green Wire       -->>           A- 
		 
         Red Wire         -->>           E+ 
		 
         Black Wire       -->>           E- 
		  
         White Wire       -->>           A+ 
 
Step 7: Interface HX711 with an Arduino 

           HX711                        Arduino 
		   
           GND            -->>           GND 
		   
           DT             -->>           A4 
		   
           SCK            -->>           A3
		   
           Vcc            -->>           5V 
 


 
 
Step 8: Add Library of following sensor to Arduino using the steps given below. 
 HX711  -- Library for Load Sensor amplifier 

 DTH   -- Library for Temperature and Humidity Sensor 
   
 Under Arduino IDE, Go to “Sketch” -> ”Include Library” -> ”Add .zip File” -> open the zipped library downloaded from above link -> “Add” 
  
Step 9: Upload Arduino code to Arduino Mega 2560 using Arduino IDE
