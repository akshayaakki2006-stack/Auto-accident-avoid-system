# Auto-accident-avoid-system
The code is to  protect people from accidents
 # Code :
const int sensorA = 2;
const int sensorB = 3;
const int sensorC = 4;

const int redA = 5;
const int greenA = 6;
const int redB = 7;
const int greenB = 8;
const int redC = 9;
const int greenC = 10;

const int buzzer = 11;

void setup() {
  pinMode(sensorA, INPUT);
  pinMode(sensorB, INPUT);
  pinMode(sensorC, INPUT);
  
  pinMode(redA, OUTPUT);
  pinMode(greenA, OUTPUT);
  pinMode(redB, OUTPUT);
  pinMode(greenB, OUTPUT);
  pinMode(redC, OUTPUT);
  pinMode(greenC, OUTPUT);
  
  pinMode(buzzer, OUTPUT);
  
  digitalWrite(redA, HIGH);
  digitalWrite(redB, HIGH);
  digitalWrite(redC, HIGH);
}

void loop() {
  if(digitalRead(sensorA) == HIGH){
    digitalWrite(greenA, HIGH);
    digitalWrite(redB, HIGH);
    digitalWrite(redC, HIGH);
    digitalWrite(buzzer, HIGH);
    delay(3000);
    digitalWrite(greenA, LOW);
    digitalWrite(buzzer, LOW);
  }
  if(digitalRead(sensorB) == HIGH){
    digitalWrite(greenB, HIGH);
    digitalWrite

# Explanation 
The system employs three sensors (sensorA, sensorB, sensorC) to identify approaching vehicles from both sides of a three-way intersection. Each side has red and green LEDs to regulate traffic lights, and a buzzer provides an auditory signal when a vehicle is approaching.

In the arrangement, all pins are set to initialize, and all traffic lights are set to red initially.

In the loop, the program repeatedly scans each sensor:

When a vehicle is detected at a sensor, the system turns on the green light for that side, holds all other sides at red, and sounds the buzzer for 3 seconds to allow the vehicle to pass.

After 3 seconds, the green light and buzzer are turned off, and the system returns to red, ready to scan for the next vehicle.

This arrangement ensures that only one side can proceed at a time, minimizing the chances of accidents, while warning other vehicles through red lights and sound.
