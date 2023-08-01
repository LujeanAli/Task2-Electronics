# Task2-Electronics


## Servo Motor

 ### Dedinition:
  A Servo Motor is a small device that has an output shaft. This shaft can be positioned to specific angular positions.

 ### Hardware Required:
  - Arduino UNO.
  - Breadboard.
  - Servo Motor.
  - 10k ohm potentiometer
  - hook-up wires.

  ### Circuits:

   #### Knob Circuit

   ####

  - When the button is not pressed:
 
      ![image](Circuit-1.png)
 
  - When the button is pressed:
    
      ![image](Circuit-1.1.png)


  ### Code:

```
int led=2;
int PushButton=5;
int button;

void setup()
{
  
  pinMode(led, OUTPUT);
  pinMode(PushButton, INPUT);
  Serial.begin(9600);
}

void loop()
{
  
  button=digitalRead(5);
  
  if(button==HIGH)
  {
    digitalWrite(led,HIGH);
    delay(3000);
  }
  else
  {
     digitalWrite(led,LOW);
  }
  
}
```
  ### Tinkercad link:

      https://www.tinkercad.com/things/dksbH09xmc7?sharecode=gaO8uukPS-zQfJDkhBOqCBr6Dx06qi3JcHrlQG23NlI
