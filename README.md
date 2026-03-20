# dual-builds-2026
just my passion projects
## Day 1: Digital Sensor + Actuator Demo (Button → LED)

**Goal:** Simulate reading a digital input sensor and controlling an actuator (LED) using INPUT_PULLUP.

<image-card alt="Tinkercad Button + LED Circuit" src="Spectacular Robo.png" ></image-card>

- Wiring:
  - Pushbutton: diagonal legs → pin 2 and GND
  - LED: anode → pin 13, cathode → 220 Ω resistor → GND
- Code uses `INPUT_PULLUP` so button is HIGH (unpressed) by default
- Behavior: LED OFF when button released, ON when pressed
- Bosch tie-in: Mirrors digital sensor reading + output control in Mikrocontroller Praxisphasen
## Day 2 / Week 1: Analog Sensor + Proportional Control

**Tinkercad Circuit:**
- Potentiometer (A0) → scales LED brightness on PWM pin 9.
- Uses analogRead() + map() + analogWrite().

![Pot Low](week1/images/Spectacular Robo (2).png)
![Pot High](week1/images/Spectacular Robo (1).png)

**Python Mirror:** Simulated proportional response with adjustable Kp gain.

**Bosch / Real-World Tie-in:**
- Analog sensors (pot → position/temp/pressure) common in Bosch actuators.
- Proportional control = basic speed/position regulation before full PID in Regelungstechnik.
- Prepares for motor control, valve positioning, or sensor-based automation in Praxisphasen.
