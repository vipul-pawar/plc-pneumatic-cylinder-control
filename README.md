# plc-pneumatic-cylinder-control
 PLC-based control of single &amp; double-acting pneumatic cylinders using off-delay timer and negative edge detection.



# PLC-Based Control of Single & Double-Acting Pneumatic Cylinders

## 📖 Project Overview
This project demonstrates PLC-based control of pneumatic cylinders using:
- Off-delay timer (5 seconds)
- Negative edge detection
- Sequential activation of single and double-acting cylinders

## ⚙️ Hardware Used
- Pneumatic Air Preparation Unit (FRL)
- 4/2 Solenoid Valve
- Pneumatic Manifold
- Single-acting Cylinder (Janatics ADN 32×100 mm)
- Double-acting Cylinder
- PLC (with ladder logic programming)

## 🧩 PLC Logic

### 🔖 Tag Table
<p align="center">
  <img src="images/photo_6296237832363773608_y.jpg" alt="PLC Tag Table" width="600"/>
</p>
<p><em>Tag table showing input/output addresses and variables used for cylinder control.</em></p>

---

### ⚡ Rung 1 – Off-Delay Timer
<p align="center">
  <img src="images/photo_6296237832363773611_x.jpg" alt="Rung 1 Off-Delay Timer" width="600"/>
</p>
<p><em>Rung 1 applies a 5-second off-delay timer to Cylinder 1, ensuring controlled extension before Cylinder 2 activates.</em></p>

---

### ⚡ Rung 2 – Negative Edge Detection
<p align="center">
  <img src="images/photo_6296237832363773610_x.jpg" alt="Rung 2 Negative Edge Detection" width="600"/>
</p>
<p><em>Rung 2 detects the negative edge of Cylinder 1’s signal, triggering Cylinder 2 to extend only after Cylinder 1 completes its cycle.</em></p>

---

### ⚡ Rung 3 – Reset/Return
<p align="center">
  <img src="images/photo_6296237832363773609_x.jpg" alt="Rung 3 Reset Logic" width="600"/>
</p>
<p><em>Rung 3 resets the sequence, returning both cylinders to their initial positions for repeatable operation.</em></p>

## 🛠 Skills Demonstrated
- PLC Programming (Timers, Edge Detection)
- Pneumatics (Cylinder & Valve Control)
- Industrial Automation
- Instrumentation Engineering
- Troubleshooting & Wiring

## 📂 Repository Structure
