# Experiment-no-6-DC-Motor-Speed-Control-Using-Arduino

###  DATE: 

###  NAME: JASHWANA FATHIMA S 

###  ROLL NO : 212222040059

###  DEPARTMENT: CSE

### AIM : To control the speed and the direction of a DC motor using L293D driver ic( H- bridge)

### Components Required:
•	Arduino UNO board
•	L293D driver
•	12V DC motor
•	10K ohm potentiometer
•	Pushbutton
•	12V source
•	Breadboard
•	Jumper wires
### THEORY 
The L293D quadruple half-H drivers chip allows us to drive 2 motors in both directions, with two PWM outputs from the Arduino we can easily control the speed as well as the direction of rotation of one DC motor. (PWM: Pulse Width Modulation).
Arduino DC motor control circuit:
Project circuit schematic diagram is the one below.

![image](https://user-images.githubusercontent.com/36288975/167763051-b230c183-afc5-46f2-ba95-0f95e10dd6c9.png)
FIGURE-01 H BRIDGE CIRUCIT INTERFACE 
 
The speed of the DC motor (both directions) is controlled with the 10k potentiometer which is connected to analog channel 0 (A0) and the direction of rotation is controlled with the push button which is connected to pin 8 of the Arduino UNO board. If the button is pressed the motor will change its direction directly.
The L293D driver has 2 VCCs: VCC1 is +5V and VCC2 is +12V (same as motor nominal voltage). Pins IN1 and IN2 are the control pins where:
![image](https://user-images.githubusercontent.com/36288975/167763120-1421c2c5-8381-49eb-b376-03f6e1113b7a.png)
TABLE-01 EXITATION TABLE FOR H BRIDGE 

As shown in the circuit diagram we need only 3 Arduino terminal pins, pin 8 is for the push button which toggles the motor direction of rotation. Pins 9 and 10 are PWM signal outputs, at any time there is only 1 active PWM, this allows us to control the direction as well as the speed by varying the duty cycle of the PWM signal. The active PWM pin decides the motor direction of rotation (one at a time, the other output is logic 0).

### PROGRAM 
```
int input1=5;
int input2=6;
int en=3;

void setup()
{
  pinMode(input1, OUTPUT);
  pinMode(input2, OUTPUT);
  pinMode(en, OUTPUT);
}


void loop()
{ 
  analogWrite(en,50);
 
  digitalWrite(input1, LOW);
  digitalWrite(input2, HIGH);
  delay(500);
}
```
### OUTPUT

![WhatsApp Image 2024-04-05 at 4 23 07 PM](https://github.com/Jashwanafathima/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560192/27cc08fb-e9e0-4494-8947-c30e2f5835ec)

![WhatsApp Image 2024-04-08 at 8 54 25 AM](https://github.com/Jashwanafathima/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560192/7b4d2d1b-981c-4a5b-beb4-7bdb85b8d7f5)

### GRAPH AND TABULATION 

![WhatsApp Image 2024-04-05 at 4 23 12 PM](https://github.com/Jashwanafathima/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560192/a781769a-1063-4400-9b21-4ab3e3f40df0)

![WhatsApp Image 2024-04-05 at 4 23 07 PM](https://github.com/Jashwanafathima/Experiment-no-7-DC-Motor-Speed-Control-Using-Arduino/assets/119560192/56c907da-5dc1-45da-921e-f1a27cd5a4a8)



### RESULTS AND DISCUSSION :
Thus To control the speed and the direction of a DC motor using L293D driver ic( H- bridge) is implemented successfully


