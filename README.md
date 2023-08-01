# Task2-Electronics


## Servo Motor

 ### Definition:
  A Servo Motor is a small device that has an output shaft. This shaft can be positioned to specific angular positions.

 ### Hardware Required:
  - Arduino UNO.
  - Breadboard.
  - Servo Motor.
  - 10k ohm potentiometer
  - hook-up wires.

  ### Circuits:

   
   #### - Knob Circuit
   ![image](knob.png)
   
   #### - Sweep Circuit
  ![image](Sweep.png)



  ### Code:

  #### - Knob Code

```
#include <Servo.h>

Servo myservo;  // create servo object 


int position = 0;   //  servo position

void setup() {
  myservo.attach(3);  // attaches the servo on pin 3 
}

void loop() {
  
   // goes from 0 degrees to 180 degrees
  for (position = 0; position <= 180; position += 1) {
    
    myservo.write(position);              
    delay(15);                       
  }
  
  
  // goes from 180 degrees to 0 degrees
  for (position = 180; position >= 0; position -= 1) { 
    myservo.write(position);              
    delay(15);                       
  }
}
  
```

 #### - Sweep Code

 ```

#include<Servo.h> 

Servo myservo; // create servo object

int position=0; //  servo position

int v; // To store value of the potentiometer

void setup()
{
  myservo.attach(3);
}

void loop()
{
  v = analogRead(position);           
  v = map(v, 0, 1023, 0, 180); 
  myservo.write(v);                  
  delay(15); 
}

 ```

  ### Tinkercad link:

  #### - Knob
  https://www.tinkercad.com/things/bd6KAW0pPJU?sharecode=dfLSPfnHgv3nyEK807E_W-9VUNXNTrZrRVU1_D7EC-s

  #### - Sweep 
  https://www.tinkercad.com/things/kFHIBqkXhlU?sharecode=mrEgE3dCBqDUGgsMTksFGjumzsR0a--6H39O97ehPVE
  
      


## DC Motor

 ### Definition:
  Direct Current (DC) motor is a motor that turns energy from a direct current and
  turns this into mechanical energy.

 ### Hardware Required:
  - Arduino UNO.
  - Breadboard.
  - DC Motor.
  - L293D Motor Driver.
  - hook-up wires.
  - power source (9v battery).

  ### Circuits:

   
   #### - Knob Circuit
   ![image](DC Motor.png)
   
  ### Code:
  
 ```
void setup()
{
  pinMode(3, OUTPUT);
  pinMode(4, OUTPUT);
}
void loop()
{
  digitalWrite(3, HIGH);
  digitalWrite(4, LOW);
  delay(5000); // Wait for 1000 millisecond(s)
  
  digitalWrite(3, LOW);
  digitalWrite(4, HIGH);
  delay(5000); // Wait for 1000 millisecond(s)
}

 ```

  ### Tinkercad link:

https://www.tinkercad.com/things/8cnYCCaSKV7?sharecode=U_pqXf30B8vdipInCkbmTK5nZHgxCKH1wr-CSZMCwb4

  
