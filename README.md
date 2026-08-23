# Thermoelectric Ice-Cream Chest Thermal & CFD Analysis
---
**Tools:** ANSYS Fluent 2024 R1 | CAD Modelling | Computational Fluid Dynamics |
**Type:** Self-Directed Learning Project (2024)

## Project Overview & Design Intent
Street ice-cream vendors often operate without reliable access to grid electricity, relying on heavy, passive cold packs or direct power setups that limit mobility. This project was an independent undergraduate research exercise which models a prototype thermoelectric (Peltier-based) refrigeration system. The primary design goal was to stabilize internal cooling, improve the Coefficient of Performance (COP), and reduce energy demands by utilizing an integrated battery and dynamo system driven by the cart's movement.

Beyond the physical application, this project served as my primary gateway into practical Computational Fluid Dynamics (CFD). I used it as an early, hands-on opportunity to learn geometry preparation, mesh consideration, boundary condition setup, and post-processing visualization within ANSYS Fluent.

## Engineering Considerations
To maximize cooling performance before running simulations, the physical structure was designed with Key thermal strategies in mind:
* **Material Selection:** Polyurethane was selected as the outer shell material for its thermal resistance and low thermal conductivity.
* **Geometric Optimization:** Standard rectangular chests often suffer from stagnant "heat pockets" in sharp 90° internal corners. The cavity was modelled with rounded, filleted internal corners to encourage smooth motion along the perimeter boundary layers.
* **Evaluation Objectives:** Assess internal air velocity, evaluate convective transport patterns, compare the effectiveness of two distinct Peltier module arrangements.

---

## Configuration Analysis

### 1. Two-Peltier Setup (Long Wall Array)
* **Setup:** Two thermoelectric modules placed side-by-side along one of the long side walls.
* **Velocity Dynamics:** Airflow velocity peaked at 95.1 m/s near the act
* **Thermal Behavior:** Maintained a remarkably uniform temperature field
* **Key Finding:** While thermal distribution was even, omitting active cooling on the opposing short wall left the far end dependent on secondary boundary currents, making it ideal for low-power steady-state holding rather than fast pull-down.

### 2. Three-Peltier Setup (Multi-Wall Array)
* **Setup:** Two modules positioned along the long wall and one added to the adjacent short wall.
* **Velocity Dynamics:** Produced higher localized forced convection velocity (~194.7 m/s peak localized scale) and introduced a complex, asymmetrical multi-directional flow loop.
* **Thermal Behavior:** Generated deeper localized cooling drops (~270.9 K / -2.2°C) and rapidly dispersed cold air throughout the main volume.
* **Key Finding:** The asymmetrical layout dramatically increased mixing and reduced transient cooling times, providing superior pull-down performance when surplus power is available from the dynamo.

---

## Key Learning Outcomes
* **Boundary Layer Flow:** Confirmed through streamline post-processing that internal corner fillets successfully eliminated flow stagnation, allowing cold air currents to hug the insulation walls smoothly.
* **CFD Workflow Mastery:** Gained practical, self-taught experience in defining thermal-fluid boundary conditions, analyzing convergence, and interpreting velocity contours and 3D streamline plots in ANSYS Fluent.
* **Trade-off Evaluation:** Demonstrated how numeric simulation guides real-world engineering decisions—balancing thermal pull-down performance against system power consumption in off-grid mobile applications.
