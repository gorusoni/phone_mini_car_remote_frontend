Smart RC Car with Seatbelt Safety System

A web-based control dashboard for an RC car that simulates a real vehicle safety feature — the car’s speed is restricted unless the “seatbelt” is properly fastened using touch sensors.

This project combines UI design, logical sensor validation, and vehicle control simulation.

📌 Features
🪢 Seatbelt Safety Logic

The system uses 4 touch sensors (c1, c2, c3, c4) to detect whether the seatbelt is worn correctly.

Seatbelt is considered VALID ONLY IF:

c1 AND c3 are pressed (and c2, c4 are not)
OR

c2 AND c4 are pressed (and c1, c3 are not)

Any other combination = ❌ Invalid seatbelt

💡 Visual Indicators
Condition	Green Light	Red Light	Message
Seatbelt Valid	ON	OFF	Belt is OK – Safe Driving
Seatbelt Invalid	OFF	ON	Wear belt properly – Speed Restricted
🎮 RC Car Controller

The interface includes directional controls:

Forward

Backward

Left

Right

Stop

These simulate movement commands that can later be sent to an ESP32 via Bluetooth.

🏎 Speed Control Logic
Seatbelt Status	Maximum Speed
❌ Not Worn Properly	35% (Restricted Mode)
✅ Worn Properly	100% (Full Speed Mode)

The speedometer bar updates in real-time based on the safety status.

🖥 How It Works

User presses seatbelt touch buttons (c1–c4).

System checks if the pressed combination matches a valid belt pattern.

If valid:

Green light turns ON

Full speed allowed

If invalid:

Red light turns ON

Speed is limited

When a direction button is pressed, speed is set based on belt status.

🔧 Technologies Used

HTML – Structure

CSS – Styling and dashboard design

JavaScript – Sensor logic, safety validation, speed control

🔌 Future Hardware Integration

This front-end is designed to connect with:

ESP32 / Arduino

Bluetooth Module (HC-05 / BLE)

Motor Driver (L298N, etc.)

Touch Sensors in seatbelt strip

Future version will:

Send speed + direction data via Bluetooth

Physically restrict motor speed if belt is not worn
