Features
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

