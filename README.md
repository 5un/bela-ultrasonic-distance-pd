# bela-ultrasonic-distance-pd
Bela.io ultrasonic distance example with HC-SR04 Ultrasonic module in PureData

## Connections
* HC-SR04 VCC to Bela P9_07 (SYS 5V)
* HC-SR04 GND to Bela P8_01 (GND)
* HC-SR04 Trigger to Bela Analog Out 0
* HC-SR04 Echo to Bela P8_08 (Digital Pin 12) with voltage divider!!

Warning: A voltage divider must be used to connect the echo pin of HC-SR04 (5V) to Bela's Digital Input (3.3V). You will risk Bela by not doing so. 

You can refer to this Rasberry Pi HC-SR04 voltage divider example [https://metacpan.org/pod/RPi::HCSR04](https://metacpan.org/pod/RPi::HCSR04)

## Debugging

The trigger pulse is connected to Oscilloscope channel 1 (dac~ 27). The echo digital input is connected to Oscilloscope channel 2 (dac~ 28).

### Steps to debug
* Connect the circuit according to connection instructions above
* Open Bela's Scope view and check if the trigger pulse (red by default) is working.
* Obstruct your ultrasonic sensor at different distances and see if the length of the echo pulse (blue by default) changed.


