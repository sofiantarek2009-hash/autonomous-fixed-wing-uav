# Autonomous Fixed-Wing Plane (UAV)

**Category:** Hardware / Robotics · **Compute:** NVIDIA Jetson Nano + Custom Flight Controller

> **Visibility & Public Gists:** This repository is **private** to protect custom flight-controller firmware, avionics integration notes, and mission tooling. **Public GitHub Gists** covering navigation logic and hardware architecture notes are available for technical review and personal website links.

---

## Overview

Custom-built **autonomous fixed-wing unmanned aerial vehicle (UAV)** combining an onboard **NVIDIA Jetson Nano** companion computer with a **custom flight controller** to execute autonomous flight missions.

## System Capabilities & Flight Characteristics

- **Onboard Compute & Avionics:** Dual-tier architecture pairing an NVIDIA Jetson Nano with a custom-built flight controller for low-level control actuation and telemetry.
- **Autonomous Mission Execution:** Supports pre-planned waypoint missions from launch through cruise.
- **Sensor-Based Course Correction:** Real-time closed-loop attitude and trajectory adjustments driven by onboard sensor feedback to correct drift during flight.
- **Flight Endurance:** Validated over **~15–20 minute autonomous flights**.

---

**Author:** Sofian Mousa
