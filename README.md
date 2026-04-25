# plc-pneumatic-cylinder-control
 PLC-based control of single &amp; double-acting pneumatic cylinders using off-delay timer and negative edge detection.



# PLC-Based Control of Single & Double-Acting Pneumatic Cylinders

## 📖 Project Overview
This project demonstrates PLC-based control of pneumatic cylinders using:
- Off-delay timer (5 seconds)
- Negative edge detection
- Sequential activation of single and double-acting cylinders

## ⚙️ Hardware Used

<table>
  <tr>
    <td style="vertical-align:top; width:50%;">
      <ul>
        <li>Pneumatic Air Preparation Unit (FRL)</li>
        <li>4/2 Solenoid Valve</li>
        <li>Pneumatic Manifold</li>
        <li>Single-acting Cylinder (Janatics ADN 32×100 mm)</li>
        <li>Double-acting Cylinder</li>
        <li>PLC (Siemens CPU 1215C)</li>
      </ul>
    </td>
    <td style="vertical-align:top; text-align:right; width:50%;">
      <img src="images/photo_6293941154436813075_w.jpg" alt="FRL Unit" width="120"/>
      <img src="images/photo_6293941154436813078_w (1).jpg" alt="4/2 Valve" width="120"/>
      <img src="images/photo_6293941154436813074_y.jpg" alt="Manifold" width="120"/>
      <img src="images/photo_6293941154436813077_w.jpg" alt="Cylinder" width="120"/>
    </td>
  </tr>
</table>



## 🧩 PLC Logic

### 🔖 Tag Table
<p align="center">
  <img src="images/photo_6296237832363773608_y.jpg" alt="PLC Tag Table" width="600"/>
</p>
<p><em>Tag table showing input/output addresses and variables used for cylinder control.</em></p>

---

### ⚡ Network 1 – Start Push Button
<p align="center">
  <img src="images/photo_6296237832363773611_x.jpg" alt="Network 1 Start PB" width="600"/>
</p>
<p><em>Pressing Start_PB (%I0.0) sets MemoryBit (%M0.0) to begin the sequence.</em></p>

---

### ⚡ Network 2 – Off-Delay Timer
<p align="center">
  <img src="images/photo_6296237832363773609_x.jpg" alt="Network 2 Off-Delay Timer" width="600"/>
</p>
<p><em>MemoryBit triggers a TOF timer with 5s preset, controlling SolenoidValve (%Q0.2) for Cylinder 1.</em></p>

---

### ⚡ Network 3 – Negative Edge Detection
<p align="center">
  <img src="images/photo_6296237832363773610_x.jpg" alt="Network 3 Negative Edge Detection" width="600"/>
</p>
<p><em>After Cylinder 1 completes, ExtendedSensor (%I0.3) detects the negative edge and activates SecondValve (%Q0.1) for Cylinder 2.</em></p>


## 🛠 Skills Demonstrated
- PLC Programming (Timers, Edge Detection)
- Pneumatics (Cylinder & Valve Control)
- Industrial Automation
- Instrumentation Engineering
- Troubleshooting & Wiring

## 📂 Repository Structure
