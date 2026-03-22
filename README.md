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

## Day 3 / Week 1: Threshold + Proportional Control (Two LEDs)

**Tinkercad Circuit Update:**
- Pot on A0 → proportional brightness on LED pin 9.
- Threshold >700 → second "alarm" LED on pin 10 turns ON.

![Low](week1/images/tinkercad-pot-two-leds-low.png)
![Mid](week1/images/tinkercad-pot-two-leds-mid.png)
![High](week1/images/tinkercad-pot-two-leds-high.png)

**Python Simulation:** Added threshold alarm + gain (Kp) experiments.

**Bosch / Real-World Tie-in:**
- Threshold logic = safety interlocks, over-current/temp warnings in Bosch controllers.
- Proportional + threshold combo = common in motor drives (speed control + stall/over-limit protection).
- Builds intuition for hybrid continuous/discrete control in Regelungstechnik & automation praxis.
- Prepares for full PID (derivative term next week) and unstable systems like inverted pendulum.

Learnings: Higher Kp makes response faster but can cause instability in closed-loop systems.

## Day 4: Error-Based Proportional Control (Closed-Loop Intro)

**Tinkercad:** Setpoint tracking with error → brightness + alarm  
**Python Lab:** Tuned Kp=0.5 to 4.0 — saw stability vs oscillation

**Bosch Tie-in (Praxisphasen gold):**
- Exact same error = setpoint – actual used in every Bosch motor controller and automation system.
- This is Regelungstechnik Semester 2/3 in action: P-control before adding I and D terms.
- When I show this in my next Praxis report, mentor will see I already understand closed-loop systems.

GitHub video tip: Record 20 sec screen (Tinkercad + Python running side-by-side).
