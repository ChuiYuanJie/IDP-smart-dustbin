Project presentation with demo

https://www.canva.com/design/DAGna-9DOiU/-WBc8NcdXLHUX8eQ5wp06g/edit?utm_content=DAGna-9DOiU&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton


Project: Intelligent Waste Management System (Smart Dustbin)
Role: Lead Hardware Integration & Control Logic (Automatic Lid Mechanism)

1. System Overview
Designed and implemented an automated lid-opening subsystem for a touchless waste disposal unit. The goal was to minimize physical contact and improve hygiene in public/office environments using low-cost, high-reliability components.

2. Technical Stack & Hardware
Controller: Arduino Uno / ESP32 (whichever you used)

Sensing: Ultrasonic Sensor (HC-SR04) for proximity detection.

Actuation: Servo Motor (SG90/MG995) with a custom-linked mechanical arm for lid elevation.

Power Management: Regulated 5V DC supply to handle inductive loads from the servo.

3. Control Logic & Implementation
Distance Thresholding: Implemented a non-blocking sensing loop to detect objects within a 10cm - 20cm range.

Debouncing & Signal Filtering: Applied a simple Moving Average Filter (or a basic counter) to the ultrasonic readings to prevent "false opens" caused by sensor noise or environmental interference.

Servo Timing: Programmed smooth PWM (Pulse Width Modulation) transitions to avoid mechanical "jerking" and reduce wear and tear on the plastic gears.

4. Key Engineering Challenges Solved
Mechanical Advantage: Calibrated the servo horn angle and linkage length to ensure the lid opens to a full 90° without stalling the motor.

Power Stability: Solved "brown-out" issues where the sensor would reset when the motor started by adding a decoupling capacitor (if you did this) or isolating the power rails.


