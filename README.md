# EXPERIMENT-NO--02-INTERFACING-ANALOG-INPUT-SENSOR-POT-WITH-ARDUINO
# AIM:
To interface a Analog input (angular displacement sensor POT) and scale the values up on change in the input.
# NAME : Harini G
# REG NO : 212225230091
# COMPONENTS REQUIRED:
 10 KΩPOT
 1 KΩ resistor
 Arduino Uno
 USB Interfacing cable
 Connecting wires
 LED of choice
# Procedure:
Open Tinkercad → Circuits and create a new circuit.

Drag an Arduino Uno R3 into the workspace. Add a breadboard.

Add a potentiometer to the breadboard. Connect one outer pin of the potentiometer to 5V of Arduino.

Connect the other outer pin to GND of Arduino. Connect the middle pin of the potentiometer to A0 of Arduino. 

Click Code and select Text mode. 

Enter the Arduino program to read the analog value. 

Start the simulation by clicking Start Simulation.

Rotate the potentiometer knob. 

Observe the analog value in the Serial Monitor.

The value should change approximately from 0 to 1023 as you rotate the potentiometer

# Algorithm:
Start Connect the potentiometer to Arduino.

Connect the potentiometer's wiper pin to analog pin A0.

Initialize serial communication. Read the analog voltage from A0 using analogRead(). 

Store the value in a variable.

Display the value on the Serial Monitor. 

Rotate the potentiometer and observe the change in value.

Repeat steps 5–8 continuously.

# PROGRAM:
```
const int sensorPin=A0;
const int ledPin=9;
void setup(){
  pinMode(ledPin, OUTPUT);
    Serial.begin(9600);
}

  void loop() {
   int sensorValue = analogRead(sensorPin);
  
  
  int brightness = map(sensorValue, 0, 1023, 0, 255);
  
  analogWrite(ledPin, brightness);
  
  
  Serial.print("Sensor: ");
  Serial.print(sensorValue);
  Serial.print(" -> LED Brightness: ");
  Serial.println(brightness);
  
  delay(10);
}
```
# OUTPUT:
# LED OFF:

<img width="1917" height="1078" alt="Screenshot 2026-10-30 085953" src="https://github.com/user-attachments/assets/35a7782b-901a-4854-b669-bec9ab792e25" />

# LED ON:

<img width="1917" height="1021" alt="Screenshot 2026-10-30 090024" src="https://github.com/user-attachments/assets/da5d7886-4849-417e-9462-3de2b5614ff7" />

# RESULT: 
Thus a Analog input (angular displacement sensor POT) and scale the values up on change in the input has been executed successfully.

Screenshot 2026-11-03 141719
RESULT:
Thus a Analog input (angular displacement sensor POT) and scale the values up on change in the input has been executed successfully.
