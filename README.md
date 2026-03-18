# dual-builds-2026
just my passion projects
## Week 1: Digital Sensor + Actuator Demo (Button → LED)

**Goal:** Simulate reading a digital input sensor and controlling an actuator (LED) using INPUT_PULLUP.

<image-card alt="Tinkercad Button + LED Circuit" src="Spectacular Robo.png" ></image-card>

- Wiring:
  - Pushbutton: diagonal legs → pin 2 and GND
  - LED: anode → pin 13, cathode → 220 Ω resistor → GND
- Code uses `INPUT_PULLUP` so button is HIGH (unpressed) by default
- Behavior: LED OFF when button released, ON when pressed
- Bosch tie-in: Mirrors digital sensor reading + output control in Mikrocontroller Praxisphasen
