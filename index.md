# IOTLevel-1
{: .IOTLevel1-Blue}
{: .text-center}



 # About Me
 {: .About Me-Blue}


 
 My name is **Sandra Krishnan**. I am studying **BCA** at **Kristu Jyoti College of Management and Technology, Changanassery**. I joined this bootcamp because i want to know more about iot. I don’t know what to do in iot so when i got this oppurtunity i started learning iot.


# Experiment -1 **Hello World LED Blinking**


![iot 1](https://user-images.githubusercontent.com/81381146/132481344-4c51d334-17d8-40bb-a376-66c1adc6ce97.png)


# Code
{: .Code-Blue}


```ino
void setup() 
{ 
  pinMode(8, OUTPUT);
} 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```
# Experiment-2 **Traffic Light**
![iot 2 (2)](https://user-images.githubusercontent.com/81381146/132482282-641ad445-0603-435b-972e-e5ca7c5afc5a.png)
# Code
{: .Code-Blue}


```ino
void setup() 
{
   pinMode(13, OUTPUT);
   pinMode(10, OUTPUT);
   pinMode(8, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(5000);
  digitalWrite(13, LOW);
  
  for(int i=0; i<3; i++)
  {
    delay(500);
    digitalWrite(10, HIGH);
    delay(500);
    digitalWrite(10, LOW);
  }
  
  delay(500);
  digitalWrite(8, HIGH);
  delay(5000);
  digitalWrite(8, LOW);
}
```
# Experiment-3 **LED Chasing Effect**
![iot3](https://user-images.githubusercontent.com/81381146/132483323-225cd110-6e70-4018-b2f7-0aa1606cbd2e.png)
# Code
{: .Code-Blue}
```ino
void setup()
{
   for (int i = 7; i < 13; i ++) 
   {
     pinMode(i, OUTPUT);
   }
}
void loop()
{
   for (int i = 7; i < 13; i ++) 
   {
     digitalWrite(i, LOW);
     delay(200);
   }
   for (int i = 7; i < 13; i ++) 
   {
     digitalWrite(i, HIGH);
     delay(200);
   }  
}

```
# Experiment-4 **Button Controlled LED**
![iot4](https://user-images.githubusercontent.com/81381146/132483435-ca56abdf-567e-493d-8a87-4ca37908ba2e.png)
# Code
{: .Code-Blue}
```ino
int x;
void setup()
{
  pinMode(11, OUTPUT);
  pinMode(7, INPUT);
}
void loop()
{
  val=digitalRead(7);
  if(x == LOW)
  {
    digitalWrite(11, LOW);
  }
  else
  {
    digitalWrite(11, HIGH);
  }
}

```
# Experiment-5 **Buzzer**
[iot 5](https://user-images.githubusercontent.com/81381146/132483592-b453215b-f550-40ad-99eb-b54d3ee2130d.png)
# Code
{: .Code-Blue}
```ino
void setup() 
{ 
  pinMode(8, OUTPUT);
} 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```
# Experiment-6 **RGB LED**
![iot6](https://user-images.githubusercontent.com/81381146/132481844-8f3e56dd-26d8-492e-a0bd-faa5b105f08d.png)
# Code
{: .Code-Blue}
```ino
int red = 11;
int blue =10;
int green =9;
int x;
void setup() {
  pinMode(red, OUTPUT);
  pinMode(blue, OUTPUT);
  pinMode(green, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(x=255; x>0; x--)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
for(x=0; x<255; x++)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
 Serial.println(x, DEC);
}
```
# Experiment-7 **LDR Light Sensor**
![iot 7](https://user-images.githubusercontent.com/81381146/132483722-f2b7f75b-7f15-4d8c-a94b-3f6b55c62194.png)


# Code
{: .Code-Blue}
```ino


```
# Experiment-8 **Flame Sensor**
![iot8](ab.png)
# Code
{: .Code-Blue}
```ino
const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;

void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    Serial.println("Fire!!!");
    digitalWrite(buzzerPin, HIGH);
  }
  else
  {
    Serial.println("No worries");
    digitalWrite(buzzerPin, LOW);
  }
}

```
# Experiment-9 **LM35 Temperature Sensor**
![iot 9](https://user-images.githubusercontent.com/81381146/132482398-d2e34a61-618d-4167-b605-3765650f5aa3.png)
# Code
{: .Code-Blue}
```ino
const int lm35_pin = A1;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int temp_adc_val;
  float temp_val;
  temp_adc_val = analogRead(lm35_pin);
  temp_val = (temp_adc_val * 4.88);
  temp_val = (temp_val/10);
  Serial.print("Temperature = ");
  Serial.print(temp_val);
  Serial.print(" Degree Celsius\n");
  delay(1000);
}
```
# Experiment-10 **IR Remote Control Using TSOP**
![iot10](ab.png)
# Code
{: .Code-Blue}
```ino
#include <IRremote.h>
 
int RECV_PIN = 3;
int c=0;
IRrecv irrecv(RECV_PIN);
decode_results results;

void setup()
{
  pinMode(9, OUTPUT);
  Serial.begin(9600);
  irrecv.enableIRIn();
}

void loop() {
  if (irrecv.decode(&results)) {
    Serial.println(results.value);
    irrecv.resume();
    if(results.value==YOUR VALUE1) {
      digitalWrite(9,HIGH);
    }
    else if(results.value==YOUR VALUE2) {
    digitalWrite(9,LOW);
    }
  }
}
```
# Experiment-11 **Potentiometer Analog Value Reading**
![iot11](ab.png)
# Code
{: .Code-Blue}
```ino
int potpin = 0;
int ledpin = 13;
int val = 0;
void setup()
{
pinMode(ledpin,OUTPUT);
Serial.begin(9600);
}
void loop()
{
  digitalWrite(ledpin, HIGH);
  delay(50);
  digitalWrite(ledpin, LOW);
  delay(50);
  val = analogRead(potpin);
  Serial.println(val);
}
```
# Experiment-12 **7 Segment Display**
![iot2](ab.png)
# Code
{: .Code-Blue}
```ino
void setup()
{
  pinMode(LED_BUILTIN, OUTPUT);
}

void loop()
{
  digitalWrite(LED_BUILTIN, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}
```
# IOT Challenge Assignments

## Assignment-1 **Automatic Night Lamp Using LDR and LED**
![](.png)

# Code
{: .Code-Blue}
```ino
const int LED = 13;  
const int LDR = A0;  

void setup() {
  Serial.begin(9600);
  pinMode(LED, OUTPUT); 
  pinMode(LDR, INPUT);   
}

void loop()
{
  int ldrStatus = analogRead(LDR);  
  if (ldrStatus <= 400) {
    digitalWrite(LED, HIGH);               
    Serial.println("Room is DARK - LED ON");
  }
  else {
    digitalWrite(LED, LOW);         
    Serial.println("Room is BRIGHT - LED OFF");
    }
}
```
## Assignment-2 **Digital Dice Using 6 LEDS and 1 Push Button**
![](.png)

# Code
{: .Code-Blue}
```ino
#define DEBUG 0

int first = 2;
int second = 3;
int third = 4;
int fourth = 5;
int fifth = 6;
int sixth = 7;

int button = 12;
int pressed = 0;

void setup() {
  for (int i=first; i<=sixth; i++) {
    pinMode(i, OUTPUT);
  }
  pinMode(button, INPUT);
  randomSeed(analogRead(0));

  #ifdef DEBUG
  Serial.begin(9600);
  #endif

}

void buildUpTension() {
  for (int i=first; i<=sixth; i++) {
    if (i!=first) {
      digitalWrite(i-1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
    }
  for (int i=sixth; i>=first; i--) {
    if (i!=sixth) {
      digitalWrite(i+1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
  }
}

void showNumber(int number) {
  digitalWrite(first, HIGH);
  if (number >= 2) {
    digitalWrite(second, HIGH);
  }
  if (number >= 3) {
    digitalWrite(third, HIGH);    
  }
  if (number >= 4) {
    digitalWrite(fourth, HIGH);    
  }
  if (number >= 5) {
    digitalWrite(fifth, HIGH);    
  }
  if (number == 6) {
    digitalWrite(sixth, HIGH);    
  }
}

int throwDice() {
  int randNumber = random(1,7);
  
  #ifdef DEBUG
    Serial.println(randNumber);
  #endif
  return randNumber;
}

void setAllLEDs(int value) {
  for (int i=first; i<=sixth; i++) {
    digitalWrite(i, value);
  }
}

void loop() {
  pressed = digitalRead(button);

  if (pressed == HIGH) {
    setAllLEDs(LOW);
    
    buildUpTension();
    int thrownNumber = throwDice();
    showNumber(thrownNumber);
  } 

}

```

