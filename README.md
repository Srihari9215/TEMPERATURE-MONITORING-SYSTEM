# TEMPERATURE-MONITORING-SYSTEM

COMPANY: CODTECH IT SOLUTIONS

"NAME: SRIHARI A

"INTERN ID: CT04DY35

"DOMAIN: EMBEDDED SYSTEMS"

DURATION: 4 WEEEKS

"MENTOR: VAISHALI"

🔧 Project Title:

Temperature Monitoring System using Arduino and LCD

📋 Project Description:

This system uses a temperature sensor to continuously monitor the ambient temperature. The temperature is displayed both on an LCD screen and printed to the Serial Monitor for real-time observation.

The project is ideal for basic temperature monitoring, learning analog sensor interfacing, and demonstrating how sensors can be used in home automation, weather stations, or environmental monitoring.

🔌 Hardware Components:

Arduino Uno/Nano

Temperature Sensor (likely TMP36 or LM35):

TMP36: output is 0.5V at 0°C, increasing by 10mV/°C

LM35: output is 0V at 0°C, increasing by 10mV/°C

16x2 LCD Display (used with 6 digital pins)

Connecting wires

Breadboard

🧠 Working Principle:

The sensor outputs an analog voltage proportional to the temperature.

Arduino reads this voltage using analogRead().

The voltage is converted to temperature:

float temperatureC = (voltage - 0.5) * 100;


This formula is for TMP36. If you're using LM35, use:

float temperatureC = voltage * 100;


The temperature value is:

Displayed on a 16x2 LCD.

Printed to the Serial Monitor.

🔍 Code Analysis:
int sensorPin = 0;  // A0 analog input


The sensor is connected to A0 pin of Arduino.

float voltage = reading * 4.68 / 1024.0;


Converts analog value (0–1023) to voltage.

4.68 is used instead of 5.0 for more accurate calibration, based on actual measured Vcc.

float temperatureC = (voltage - 0.5) * 100;


Converts voltage to °C using TMP36 formula.

lcd.setCursor(0,0);
lcd.print("Temperature Value ");
lcd.setCursor(0,1);
lcd.print(" degrees C");
lcd.setCursor(11,1);
lcd.print(temperatureC);


Displays temperature on LCD.

🖥️ LCD Output Example:
Temperature Value
   28.56 degrees C

🧪 Applications:

Room or lab temperature monitoring

Smart thermostat development

Weather station

Home automation

✅ Possible Improvements:

Add °C symbol (custom character)

Add Fahrenheit conversion:
float temperatureF = temperatureC * 9.0 / 5.0 + 32;

Add Data Logging to SD card

Use I2C LCD module to save pins

Trigger fan/AC if temperature exceeds a threshold


Output:
https://github.com/Srihari9215/TEMPERATURE-MONITORING-SYSTEM/issues/1#issue-3325187199
