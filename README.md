# Autonomous Fixed-Wing Plane (UAV) (Public Showcase)

> **Public Runnable Proof Gist:** [**Execute & Inspect Live SIL Flight Proof Gist ->**](https://gist.github.com/sofiantarek2009-hash/5a2fe80e4b6eb7809202c54b7a337255)  
> **Visibility Policy:** Physical KiCad avionics schematics, airframe CAD, and onboard board firmware stay in **private** repositories (`FPV-Plane`, `Custom-Flight-Controller-PCB`). The public Gist publishes the closed-loop Software-in-the-Loop (SIL) L1 guidance, 100 Hz 2-state attitude EKF, and low-voltage RTL failsafe suite.

---

## Run the Reproducible SIL Proof Locally (Zero Dependencies)

Requires **Python 3.9+ standard library only**:

```bash
gh gist clone 5a2fe80e4b6eb7809202c54b7a337255 fixed-wing-uav-sil-proof
cd fixed-wing-uav-sil-proof
python3 fixed_wing_guidance_sil.py --test
```

## Verified Closed-Loop SIL Telemetry (`18-Minute Mission`, `5.5 m/s` Crosswind)

- **Companion L1 Guidance (`20 Hz`):** Full **`5/5`** polygon waypoint capture across **`4` laps** (`1080s`, `22` total hits) with **`1.01 m` straight-leg cross-track RMS** (`< 15.0 m` bound).
- **Custom FC Attitude EKF (`100 Hz`, `108,000` ticks):** Fuses `0.8 deg/s` noisy MEMS gyro (+ `0.025 rad/s` constant bias) with `2.0 deg` noisy accelerometer roll -> **`0.449 deg` Roll RMS error** and **`0.02488 vs 0.02500 rad/s` learned gyro bias** (`0.00012 rad/s` error).
- **Flight Envelope Protection:** Load-factor-compensated throttle preserves minimum airspeed at **`17.98 m/s`** above the `13.5 m/s` stall floor with **`0.00 m` altitude RMS error**.
- **Low-Voltage Failsafe:** Watchdog triggers cleanly at `t = 110s` -> **`RTL_LOITER`**, holding an orbit within **`93.2 m`** of home.
- **Hardware Validation (Private Repos):** Dual-compute **NVIDIA Jetson Nano** + **custom flight controller** validated over **~15–20 minute autonomous flights**.

## Proof Bundles & Related Systems

- **Alpha Genesis (EGX Trading Engine):** [Showcase Repo](https://github.com/sofiantarek2009-hash/alpha-genesis-overview) · [Runnable Proof Gist](https://gist.github.com/sofiantarek2009-hash/a342d001d6ee81478a3e33519afaed29)
- **Polymarket Statistical Models:** [Showcase Repo](https://github.com/sofiantarek2009-hash/polymarket-prediction-models) · [Runnable Proof Gist](https://gist.github.com/sofiantarek2009-hash/9b62a1b39b175a7574452c393e16f71f)
- **AI Legal NLP, Biotech & Forecasting:** [Showcase Repo](https://github.com/sofiantarek2009-hash/ai-legal-compliance-nlp) · [Runnable Proof Gist](https://gist.github.com/sofiantarek2009-hash/66bcce759395d549fa402d0ee4411cd8)
- **Autonomous Fixed-Wing UAV (SIL):** [Showcase Repo](https://github.com/sofiantarek2009-hash/autonomous-fixed-wing-uav) · [Runnable Proof Gist](https://gist.github.com/sofiantarek2009-hash/5a2fe80e4b6eb7809202c54b7a337255)
- **Apodictic Public Verification Harness (10 Proof Bundles + CI):** [apodictic-verified-proofs](https://github.com/sofiantarek2009-hash/apodictic-verified-proofs)
- **Live Explorer & AI Agent Specs:** [www.apodictic.dev/proofs](https://www.apodictic.dev/proofs) · [`llms.txt`](https://www.apodictic.dev/llms.txt) · [`.well-known/agent.json`](https://www.apodictic.dev/.well-known/agent.json) · [GitHub Profile](https://github.com/sofiantarek2009-hash)
---

**Author:** Sofian Mousa · **Contact:** `sofianmousa@apodictic.dev`
