# Hi, I'm Damian – Automation Engineer

**Specialization:** Klipper firmware automation, real-time print monitoring, ML-driven quality control for 3D printing systems.

## 🎯 Focus Areas

- **Printer Automation**: Klipper configuration optimization, Moonraker API integration, dynamic runtime adjustments
- **Real-time Monitoring**: Python-based telemetry collection, hardware integration (GPIO displays, camera feeds), anomaly detection
- **ML Integration**: YOLOv8 computer vision for print failure detection, local model optimization (quantized inference)
- **Infrastructure**: Linux system administration, API-first architecture, automated calibration pipelines

## 📊 Current Projects

### 1. **Klipper Automation Suite**
Real-time printer control via Moonraker API with dynamic velocity adjustments, eliminating manual configuration restarts.

**Tech Stack:** Python 3.10+, WebSocket (Moonraker), Klipper (firmware), Mainsail (UI)  
**Key Achievement:** Reduced iteration time for velocity tuning from 15–20 min to <2 min per test cycle

### 2. **ML-Based Print Quality Monitoring**
Multi-modal monitoring system combining G-code trajectory analysis + computer vision for closed-loop failure prevention.

**Tech Stack:** PyTorch, OpenCV, YOLOv8 (quantized), NVIDIA CUDA, Raspberry Pi 4B+ + CSI camera  
**Key Metrics:** 10 Hz sampling via Moonraker WebSocket, <100ms latency tolerance for passive analysis  
**Hardware:** TURZX IPS 3.5" GPIO display for real-time status visualization

### 3. **ERCF V2 DIY Integration (In Progress)**
4-color multimaterial extruder system with Klipper macro automation and tool-change optimization.

**Scope:** Sub-500 PLN budget, mechanical integration, G-code deduplication, safety interlocks  
**Target:** Reduce filament waste during tool changes through automated pressure advance tuning

---

## 🔧 Technical Competencies

| Category | Skills | Tools |
|----------|--------|-------|
| **Firmware** | Klipper config optimization, Input Shaper calibration, macro automation | Mainsail, SSH, Git |
| **APIs** | RESTful design, WebSocket streaming, payload optimization | Moonraker, Python requests/asyncio |
| **ML/AI** | Computer vision pipelines, model quantization, local inference | YOLOv8, PyTorch, OpenCV, GGUF |
| **Hardware** | GPIO integration, I2C/CSI protocols, Linux device drivers | Raspberry Pi 4B+, camera modules |
| **DevOps** | Systemd services, log aggregation, backup automation | Bash scripting, Git versioning |

---

## 📈 Metrics

- **Printer Uptime Optimization:** 95%+ reliability after config consolidation (removed 7 conflicting macros)
- **Calibration Automation:** Bash pipeline for flow/pressure-advance tuning → 60% reduction in manual iteration
- **API Integration:** Moonraker WebSocket stability → <10ms latency for telemetry collection
- **Hardware Integration:** 3-device stack (RPi display + camera + printer) with unified control interface

---

## 🎓 Approach

1. **Root Cause Analysis** – Systematic diagnosis before implementation (e.g., oozing problem → premature nozzle heating root cause)
2. **Complete Solutions** – Deployment packages include error handling, logging, rollback procedures
3. **Safety First** – All critical changes tested in isolated configs before production rollout
4. **Automation Over Manual** – Every repetitive task gets a script; minimize human intervention

---

## 💻 Hardware Stack

| Component | Spec | Role |
|-----------|------|------|
| Printer | Anycubic Kobra 2 Neo | 3D print platform |
| Controller | Raspberry Pi 4B+ | Klipper host, Moonraker API server |
| GPU (workstation) | RTX 4060 8GB, Windows 11 | ML model training/inference |
| Monitoring | 5MP CSI camera + TURZX GPIO display | Real-time visual feedback |
| Calibration | ADXL345 accelerometer (planned) | Vibration analysis for closed-loop tuning |

---

## 📚 Key Learnings

- **Input Shaper constraints matter:**
- Y-axis 34 Hz limit fundamentally caps acceleration profiles – respect hardware limits
- **Strategy selection:**
- Moonraker API (Strategy A) suitable for passive monitoring; direct ADXL passthrough (Strategy B) required for active vibration control
- **Configuration management:**
- Git versioning + atomic commits + backup before every change = zero unrecoverable states
- **Safety protocols:** Incorrect printer configs can damage hardware or create fire hazards – implement interlocks before automation

---

## 🔗 Connect

- **Email:** damian.misko@windowslive.com
- **Location:** Bydgoszcz, Poland 🇵🇱

---
