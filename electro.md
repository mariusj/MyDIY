Potentiometer
---

    - 5V
    - Analog Input
    - GND
  

	const int potPin = A0;
	
	void loop() {
	    int sensorValue = analogRead(potPin);
	    int outputValue = map(sensorValue, 0, 1023, 0, 255);
	}

    
LEDs
---

- Anode Vcc, longer pin
- Cathode GND, flat side

Color | If | Vf | Resistor | Notes
------|----|----|----------|------
Yellow 5mm | 20mA | 2.0 V | 150-180
Green 5mm | 20 mA | 2.3 - 2.5 V | 150
Red 5mm | 20 mA | 2.0 - 2.3 V | 150-180
White Warm 5mm | 20 mA | 3.2 - 3.3 V | 100
Yellow 3mm | 20mA | 2.0 - 2.3 V | 150-180
Green 3mm | 20mA | 2.1 - 2.4 V | 150
Red 3mm | 20mA | 2.0 - 2.3 V | 150-180
Blue 3mm | 20 mA | 3.6 V | 82
RGB 5mm Anode | | | | 1 - blue, 2 - green, 3 - Vcc, 4 - red
  Red | 20 mA | 2.0 V | 150-180
  Green | 20 mA | 3.5 V | 82
  Blue | 20 mA | 3.5 V | 82
RGB 5mm Cathode | | | | 1 - blue, 2 - green, 3 - GND, 4 - red
  Red | 20 mA | 2.0 V | 150-180
  Green | 20 mA | 3.5 V | 82
  Blue | 20 mA | 3.5 V | 82


	int ledPin = 9;
	
	void setup()  {
		pinMode(ledPin , OUTPUT);
	}

	void loop()  {
		analogWrite(ledPin, 128);
	}


Arduino Pro Mini
---

- DC Current per I/O Pin - 40 mA
- External Interrupts: 2 and 3
- PWM: 3, 5, 6, 9, 10, and 11
- LED: 13
