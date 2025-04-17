# Simulink Model – Boiler with Valve Control for Two Rooms (Relay/Algebraic Loop Issue)

This repository contains a Simulink model simulating a **boiler heating system** with **two temperature-controlled zones (rooms)**. Each room has a **valve** that regulates the flow of thermal liquid, controlled by a **Relay block** based on the room's temperature.

---

## ❗ Problem Description

The model uses **two Relay blocks** (one per room) to control the opening and closing of valves depending on each room's temperature.

This setup leads to:

- An **algebraic loop** warning/error due to direct feedthrough in the Relay blocks.
- **Simulation instability**, **discontinuities**, or **solver failures**.

I'm looking for a solution to preserve the switching logic while maintaining simulation stability.

---

## 🧠 What I'm Trying to Do

- Simulate a **boiler system** with **2 separate heating zones**.
- Use Relay blocks to **open/close valves** based on each room’s temperature.
- Accurately model the control dynamics without algebraic loops.

---

## 💬 What I Need Help With

- How to **break the algebraic loop** while keeping relay-like switching behavior.
- Better modeling approach for **valve control** based on temperature.
- Possible use of **Unit Delay**, **Memory**, or other Simulink blocks to resolve this.
- Whether switching to a **smoothed transition** (e.g. using a `Saturation` or `Transfer Function`) is better than a hard relay.

---

## 🔧 Model Details

- **File**: `boiler_valve_control.slx`
- **MATLAB Version**: R2024b
- **Toolboxes**:
  - Simulink
  - Simscape (if you're simulating thermal behavior physically)

---

## ▶️ How to Run

1. Open MATLAB R2024b.
2. Load the Simulink model: `boiler_valve_control.slx`
3. Run the simulation.
4. Check the error log for algebraic loop notifications.

---

## 📂 Files

- `boiler_valve_control.slx` – Simulink model
- `README.md` – Project description

---

## 📸 (Optional Screenshot)

_You can add a screenshot of the model layout here._

---

## 🤝 Contributions

If you've worked on similar thermal zone control systems or found ways around algebraic loops with relay logic, feel free to share advice, submit issues, or fork the model. I appreciate any help!

