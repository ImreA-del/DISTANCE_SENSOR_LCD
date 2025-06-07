# DISTANCE_SENSOR_LCD

This is my second project using the Arduino Uno R3.
The goal of this project was to use an ultrasonic distance sensor to measure the distance of objects in front of it and display that value on a 16x2 LCD screen in real-time.

What You’ll Need
You can use parts from the Arduino Uno R3 Super Starter Kit or get them separately:

x1 Arduino Uno R3
x1 HC-SR04 Ultrasonic Sensor
x1 16x2 LCD Display (with Hitachi HD44780 or compatible driver)
x1 10K Resistor or Potentiometer (for LCD contrast control — I used a resistor)
x1 Solderless Breadboard
x1 220 Ohm Resistor (for LCD backlight control, optional)
x1 USB cable (for power and uploading code)
x10 Jumper Wires (Male-to-Male)
x4 Jumper Wires (Female-to-Male)

Wiring for LCD1602
RS -> Pin 12
E -> Pin 11
D4 -> Pin 5
D5 -> Pin 4
D6 -> Pin 3
D7 -> Pin 2
VSS -> GND
VDD -> 5V
VO -> 10K resistor to GND (for contrast)
A (LED+) -> 5V (through 220Ω resistor)
K (LED−) -> GND

Wiring for HC-SRO4
VCC -> 5V
GND -> GND
TRIG -> Digital Pin 9
ECHO ->  Digital Pin 10

What the code does 
- Sends out an ultrasonic pulse using the HC-SR04
- Measures how long it takes to bounce back (echo)
- Converts that time into distance in centimeters and feet
- Displays the result on the LCD screen, refreshing every cycle

What I learned from this 
- How to use an ultrasonic sensor to detect distance using sound
- How to convert duration to distance using basic physics
- How to wire and code for an LCD screen using the LiquidCrystal library
- How to use serial input for control or debugging
- How to display only one value at a time on the LCD using setCursor() and lcd.clear() techniques

