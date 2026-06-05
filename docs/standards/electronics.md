---
# File: docs/standards/electronics.md
title: "Electronics Standards"
parent: Standards
nav_order: 4
---

# Electronics Standards

This document defines standards for electronics work across all Redbird Robotics projects. Since most of our systems are built from **Arduinos, motor controllers, off-the-shelf sensors, and power electronics**, our focus is on **safe wiring, consistent documentation, and reliable integration**.

---

## 1. General Guidelines

- Every electronics subteam should try to encorage:
  - A **wiring diagram** (block or schematic style).
  - A **Bill of Materials (BOM)** with part numbers, quantities, and vendors.
  - **Setup notes** (voltage levels, pinouts, jumper settings, firmware dependencies).

- Use **English** for all notes and labels.  
- Keep work modular: power distribution, control, and actuation should be separate blocks.  
- Never leave undocumented wires or connections.

---

## 2. Schematics & Diagrams

- **Preferred tools**: KiCad (schematic only), Fritzing, or simple block diagrams in Draw.io/PowerPoint.  
- **File naming**: lowercase-with-dashes (e.g., `arm-wiring-diagram.png`, `drone-power.sch`).  
- Always label:
  - Voltage levels (`+12V`, `+5V`, `3.3V`)  
  - Ground  
  - Signal lines (with Arduino pin numbers if applicable)  

- Keep diagrams clean: avoid wire crossings, use labels when possible.  

---

## 3. Wiring Standards

- **Wire colors** (ideal):
  - Red → Positive power (5V, 12V, etc.)  
  - Black → Ground  
  - sensors use one color scheme
  - affectors use secondary color scheme

- Secure wiring to avoid strain on solder joints or headers.  
- Document connector pinouts in the repo (image or table).  

---

## 4. Microcontrollers & Modules

- **Arduinos** (Uno, Mega, Nano, etc.):
  - Pin usage should be documented in a table (`pin-mapping.md`).
  - Avoid “magic numbers” in code; tie pin numbers to schematic labels.  

- **Off-the-shelf modules** (motor drivers, sensors, IMUs, etc.):
  - Include a datasheet or library reference in a BOM.  
  - Note any special requirements (e.g., logic level, supply voltage).  

---

## 5. Power Systems

- All power rails must be clearly documented:
  - Voltage, maximum current, and what devices are on each rail.  
  - Fuse ratings.  

- Never mix logic and motor power without clear separation.  
- Include diagrams of battery connections and main power routing.  
- Always have a fuse gating your logic power (such as a fuse for your arduino) to prevent burning out expensive logic devices.
---

## 6. Version Control & Documentation

- Store **schematics, wiring diagrams, BOMs, and test notes** in GitHub under `/electronics`.  
- Do **not** commit vendor datasheets — link them in the BOM instead.  
- Commit **early and often**:
  - ✅ `Added wiring diagram for arm claw control`  
  - ❌ `stuff`  

---

## 7. Testing & Safety

- Before powering a system:
  - Verify all grounds are connected.  
  - Check polarity on every power connection.  
  - Inspect for shorts with a multimeter if possible.  

- Always test subsystems individually before full integration.  
- Document expected voltages at key test points.  
- Use fuses or resettable PTCs on battery-powered systems whenever possible.  

---

## 8. Best Practices Summary

- Lowercase-with-dashes file naming  
- Every project should have: **wiring diagram + BOM + pin mapping**  
- Use consistent wire colors and label connectors  
- Document power rails and current draw  
- Track all electronics docs in GitHub (`/electronics` folder)  
- Always test subsystems before full system integration  

> Following these standards ensures that any team member can read, build, or troubleshoot electronics safely and quickly.
