# Farzad Mirbashiri
### Full-Stack IoT Engineer & Technical Project Manager
AWS Solutions Architect · Certified ScrumMaster · Certified Scrum Product Owner

I take connected products from idea to shipped system — hardware, firmware, cloud, and mobile — and I run the teams that build them.

Over the past ten-plus years I've worked every layer of that stack: laying out PCBs and writing firmware, designing serverless backends on AWS, building the mobile apps on top, and managing the Scrum teams that carry all of it to release. I've done this in healthcare startups, at Canada's leading medical research hospital, and in consulting — usually at the seam between disciplines, which is where I'm most useful.

**What I bring**
- **One owner across the stack.** ESP32 firmware, custom antennas, AWS serverless backends, Flutter apps — and, more importantly, the interfaces between them.
- **AWS built from zero.** Complete IoT backends designed and deployed from an empty account, with real-time device state over MQTT and Device Shadows instead of a fleet of servers.
- **Delivery, not just design.** As a CSM and CSPO I turn problem statements into roadmaps and backlogs, run several cross-functional teams at once, and make the trade-off calls that keep a release on schedule.

[LinkedIn](https://www.linkedin.com/in/mirbashiri/) · [mirbashiri@gmail.com](mailto:mirbashiri@gmail.com)

---

## Currently building

**A personal quantitative trading platform for crypto perpetuals** — thirteen cooperating Python services that collect real-time market data (full-depth order books over websockets into tens of gigabytes of SQLite), analyze on-chain wallets and score their signals, run paper and live execution against exchange APIs, and monitor the whole thing.

What the work actually looks like:
- **Data engineering under load** — multiple writer processes on multi-gigabyte SQLite files, WAL tuning, per-table database splitting, and crash forensics from macOS diagnostic reports (SIGSEGV, SIGBUS) back to root causes.
- **A shared rules engine** — every scoring, gating, and classification rule lives once, as JSON + a pure Python function + a JavaScript twin with parity tests, and every service calls it instead of reimplementing it.
- **Service architecture** — asyncio, websockets, MCP servers for tool-driven access, Telegram and TradingView integrations, watchdogs that distinguish an upstream outage from an internal stall.
- **AI-agent-driven development** — **the codebase is built and maintained with Claude Code and AI agent sessions**, with per-service `CLAUDE.md` conventions, changelogs, and hard rules that encode lessons learned the hard way.

---

## Selected work

### PALLY — IoT medicine tracker <sup>2022</sup>
A smart supplement and medicine tracker built on NFC, with reminders and monitoring. I designed and built the whole system from scratch: device, cloud, and app.
- **Device** — ESP32 on FreeRTOS, custom 13.56 MHz NFC antenna, SPI 240x240 display, single capacitive touch button, 2-layer D75 mm PCB, OTA updates.
- **Cloud** — Fully serverless on AWS: IoT Core (MQTT + Device Shadows) for real-time state sync, Lambda and API Gateway for the API, Cognito for auth, DynamoDB and S3 for data, Amplify for the app backend.
- **App** — Flutter, iOS and Android.

![PALLY 3D concept](/assets/images/PALLY.png)

### P202 — IoT pH meter <sup>2022</sup>
A cloud-connected digital pH meter: two-point calibration, 12-bit ADC at ±(0.1–0.01%) accuracy, isolated power supply, IPS SPI 240x240 display, three capacitive touch buttons, 2-layer 40x70 mm PCB, OTA updates.
*ESP32 · C/C++ · AWS · Flutter*

![P202 3D concept](/assets/images/P202.png)

### SOLO2 — open-source AI-powered tracked robot <sup>2022</sup>
An open-source tracked robot platform for AI experiments. [Details and downloads →](https://github.com/mirbashiri/SOLO2)

![SOLO2 dimensions](/assets/images/SOLO2_DIM.png)

---

## Experience

**Pally, Toronto — Technical Lead & AWS Solutions Architect**
Biomedical startup. Architected and built the AWS backend and mobile app for the PALLY tracker from the ground up, led three Scrum teams through a full compliance-driven product lifecycle, and acted as the technical Subject Matter Expert across teams.

**Hygienic Echo Inc. — Hardware Engineer & Engineering Lead**
Owned firmware validation and release readiness. As Product Owner, brought hardware, front-end, back-end, and cloud teams onto a single backlog and turned business problem statements into user stories.

**KITE-UHN — Technical System Analyst**
Canada's leading medical research hospital. Facilitated four cross-functional teams and senior management, shaped product roadmaps, and unblocked product owners on scope and deadlines.

**zadsolutions — Project Tech Lead**
Led end-to-end physical product development, coordinating mechanical, hardware, software, and mobile teams against customer requirements.

## Toolbox

| | |
|---|---|
| **AWS** | IoT Core (MQTT, Device Shadows), Lambda, API Gateway, Cognito, DynamoDB, S3, Amplify |
| **Embedded** | ESP32, ESP8266, STM32, AVR · FreeRTOS, ESP-IDF, Keil, MPLAB, STM32 tools |
| **Software** | C/C++, C#, Swift, Dart/Flutter, React.js, Node.js |
| **Hardware & CAD** | Altium Designer, Autodesk Eagle, Rhinoceros 3D, LabVIEW |
| **Process** | Scrum, Jira, Confluence, GitHub |

**Education** — BSc, Industrial Engineering and Industrial Technology

---

Open to conversations about full-stack IoT, technical project leadership, and building things that ship.
