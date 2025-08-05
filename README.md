Robot Arm Torque Calculation Report
1. Introduction
This report presents the torque calculations and motor selection for a robotic arm. The arm consists of three segments with the following lengths: 15 cm, 10 cm, and 4 cm. The goal is to lift a 1 kg weight, and then evaluate if the same motors can handle a 2 kg load.
2. Arm Dimensions
Segment lengths:
• Base to Joint 1: 15 cm
• Joint 1 to Joint 2: 10 cm
• Joint 2 to Gripper: 4 cm
3. Torque Calculations
Torque is calculated using the formula:
Torque (Nm) = Force (N) × Distance from joint (m)
Assuming g = 9.81 m/s², the force from a 1 kg mass = 9.81 N.

• Joint 3 (Gripper): Torque = 9.81 N × 0.04 m = 0.392 Nm
• Joint 2: Torque = 9.81 N × (0.10 + 0.04) m = 1.3734 Nm
• Joint 1: Torque = 9.81 N × (0.15 + 0.10 + 0.04) m = 2.8929 Nm

Recommended to add 30% safety margin:
• Joint 3: ~0.51 Nm
• Joint 2: ~1.79 Nm
• Joint 1: ~3.76 Nm
4. Servo Motor Selection
Based on the required torque values:
• Joint 3: MG90S Micro Servo (Torque ~2.2 kg·cm ≈ 0.22 Nm) — Not enough
• Joint 2: MG996R Servo (Torque ~11 kg·cm ≈ 1.08 Nm) — Also not enough
• Joint 1: High-torque servo like DS3218 or industrial-grade required

Suggested options (with enough margin):
• Joint 3: MG996R Servo (1.08 Nm)
• Joint 2: DS3218 Servo (19.5 kg·cm ≈ 1.91 Nm)
• Joint 1: Industrial servo (≥4 Nm)

Links to purchase:
- https://www.aliexpress.com/item/1005001662495412.html
- https://www.servocity.com/hs-7954sh-servo/
5. Evaluation for 2kg Load
If the robot arm is required to lift 2 kg instead of 1 kg, the required torque doubles:
• Joint 3: ~1.02 Nm
• Joint 2: ~3.58 Nm
• Joint 1: ~7.52 Nm

Problems:
- Motors may overheat or fail
- Arm may move slowly or lose precision

Solutions:
- Use stronger motors
- Add gear ratios to reduce load on motor
- Use counterweights to balance the load

# Robotic-arm-Torque
