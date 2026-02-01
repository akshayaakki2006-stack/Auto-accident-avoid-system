# Auto-accident-avoid-system
The code is to  protect people from accidents
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
