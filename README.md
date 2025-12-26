
# Hey, I'm Damian

I'm an automation engineer in the making – fascinated by how to automate 3D printers. Learning Klipper firmware + ML is something I've never done before – but that's exactly what makes it interesting.

## What I'm working on now

I have an Anycubic Kobra 2 Neo with Klipper and I'm running 3 projects in parallel:

**1. Klipper Automation via API** 
Problem I found: Every time I want to test a different print speed, I have to edit `printer.cfg`, restart Klipper, wait 2–3 minutes. It's frustrating.

Solution: I'm learning Moonraker API so I can send parameters live instead. Cut testing time from 15–20 minutes down to <2 minutes.

Status: ✅ Prototype works; 🔄 now learning asyncio and WebSockets

---

**2. ML for 3D Printing (Computer Vision)**
Observation: My printer sometimes does weird things (layer shifts, nozzle clogs) and I don't see it until I go check manually.

Idea: Mount a camera, learn YOLOv8, teach a model to recognize "something went wrong". If the system spots it → sends me an alert + pauses the print.

Status: 🔄 Ordering camera; learning PyTorch; never done this before

---

**3. ERCF V2 (4-Color Printing)**
I want to print in 4 colors for <$20 USD (~500 PLN). ERCF is probably the best open-source solution.

Challenge: Integration with Klipper means writing macros I've never written before. Lots of thinking about details (tool changes, safety checks).

Status: 🚧 Gathering parts; learning Klipper macros

---

## Why I'm talking about this publicly

1. **It forces me to document better** – Writing this makes me more thorough
2. **I want feedback** – If I'm doing something dumb, I'd rather know early
3. **Community** – The Klipper/3D printing community is awesome, I want to be part of it
4. **Maybe it inspires someone** – If you also want to automate your printer

## What I've accomplished so far (lessons learned)

### ✅ What worked:

- **Input Shaper calibration** (X: 54.8 Hz, Y: 34.0 Hz) – Measured with ADXL345, now I understand what it means
- **Macro deduplication** – Found 7 conflicting macros in my config. Cleaned them up.
- **Nozzle heating fix** – Problem: nozzle heated before bed = excessive oozing. Solution: heat bed first, then nozzle. Documented.
- **Bash script for calibration** – Automated pressure advance testing (no fancy UI, but it works)

### ❌ What taught me lessons:

- **Editing .cfg without backup** – Before Git, I had a mess. Now Git for everything.
- **Premature optimization** – Wanted "perfect config" from day one. Now I prefer "working + ugly" over "broken + nice"
- **Ignoring Input Shaper** – Thought it was advanced stuff for nerds. Turns out it's the KEY constraint for everything I do.

## Technical stack (what I'm picking up)

| Topic | Level | How I'm learning |
|-------|-------|------------------|
| **Python** | 🌱 Basics | YouTube + ChatGPT |
| **Klipper config** | 🌱 Basics | Docs + trial & error |
| **APIs** | 🌱 Just starting | Moonraker docs + Stack Overflow |
| **Machine Learning** | 🌱 Just starting | Fast.ai + YouTube |
| **Linux/Raspberry Pi** | 🌳 Solid (SSH, bash) | Work experience |
| **Electronics/Hardware** | 🌳 Medium (GPIO, I2C) | DIY builds, datasheets |
| **Git** | 🌳 Good (commits, branches) | Daily use |

## Hardware I have

- **Printer:** Anycubic Kobra 2 Neo (new, testing it)
- **Controller:** Raspberry Pi 4B+ running Klipper
- **Workstation:** Xeon E5-2650 V4, 32GB RAM, RTX 4060 8GB (Windows 11) – for ML stuff
- **Camera:** 5MP Raspberry Pi CSI (on order)
- **Display:** TURZX 3.5" IPS GPIO (already have)

## What I want to learn in 6 months

- ✅ Moonraker API – what interface does it have, how to use it
- ✅ YOLOv8 – training, quantization, local inference
- ✅ ERCF integration – macros, safety, servo control
- ⏳ Closed-loop vibration control (ADXL345 pass-through) – this is the hard part
- ⏳ Contributing to Klipper – maybe I'll have something to propose

## Where I can be wrong

I don't have experience with:
- Production ML code (only tutorials)
- C++/embedded systems (Klipper core)
- Commercial API integration (doing this for myself)
- Mechanical engineering (ERCF needs this)

If you see me doing something wrong → please write an Issue on GitHub.

---

## 🔗 Connect with me

- **Email:** damian.misko@windowslive.com (fastest response)
- **GitHub:** github.com/dornvite92
- **LinkedIn:** linkedin.com/in/dornvite92 -- IN PROGRESS 
- **Location:** Bydgoszcz, Poland 🇵🇱

If you're doing something similar or want to learn Klipper → would be cool to connect.

---

*Last updated: December 2025 | Still learning; repos are WIP*
