### Project Presentation & Demo
Full technical walkthrough, and live demonstration video:
👉 [**View on Canva**](https://www.canva.com/design/DAGna-9DOiU/-WBc8NcdXLHUX8eQ5wp06g/edit?utm_content=DAGna-9DOiU&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)


### 1. System Overview
Designed and implemented an automated lid-opening subsystem for a touchless waste disposal unit. The primary goal was to minimize physical contact and improve hygiene in public/office environments using low-cost, high-reliability mechatronic components.

### 2. Technical Stack & Hardware
* **Controller:** Arduino Uno / ESP32
* **Sensing:** Ultrasonic Sensor (HC-SR04) for proximity detection.
* **Actuation:** Servo Motor (SG90/MG995) with a custom-linked mechanical arm for lid elevation.
* **Power Management:** Regulated 5V DC supply to handle inductive loads from the servo.

### 3. Control Logic & Implementation
* **Distance Thresholding:** Implemented a non-blocking sensing loop to detect objects within a **10cm - 20cm range**.
* **Debouncing & Signal Filtering:** Applied a **Moving Average Filter** to the ultrasonic readings to prevent "false opens" caused by sensor noise or environmental interference.
* **Servo Timing:** Programmed smooth **PWM (Pulse Width Modulation)** transitions to avoid mechanical "jerking" and reduce wear on plastic gears.

### 4. Key Engineering Challenges Solved
* **Mechanical Advantage:** Calibrated the servo horn angle and linkage length to ensure the lid opens to a full **90°** without stalling the motor.
* **Power Stability:** Solved **"brown-out"** issues where the sensor would reset during motor startup by adding a decoupling capacitor and isolating the power rails.
