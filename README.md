# Ryan J. Park

**Industrial electrical & HVAC technician. Automation / PLC. Systems builder. U.S. Army veteran.**
Richmond Hill, GA · Founder, Stark Diagnostics LLC

---

I learned electrical, embedded, and industrial automation by teardown, experimentation, and
primary-source research. Most of what's below started the same way: I hit something I couldn't
get past, and built the thing that got me past it.

Pattern and spatial reasoning first, language second. I don't learn linearly — I build.

**Repositories here are private.** The work is described below; source is available under NDA
or on request where it isn't patent-restricted.

---

## Selected work

### MOV Systems 3D Training Simulator — *ongoing*
Interactive 3D maintenance trainer for Limitorque SMB-family motor-operated valve actuators.
Five modeled systems with clickable components, an X-ray operating mode that reveals the live
drive train, a dependency-gated assembly bench, and a 29-step procedure player.

Held to a **1:1 dimensional standard** — geometry is corrected against measurements of the
physical unit rather than approximated, and every source fact carries an explicit
*verified / assumed / unknown* tag rather than a guess. Automated geometry and proportion
audits gate each build. An adversarial review pass caught and corrected a mounting error the
model had inherited from a misread drawing.

Ongoing work is closing the remaining gap between model and physical unit.

---

### AI Industrial Diagnostic Gateway — *patent pending*
Read-only fault-diagnostic platform for PLCs, VFDs, HVAC, industrial robots, and safety
controllers across 18 device classes. Reads Modbus TCP/RTU, BACnet/IP, and OPC-UA registers and
returns a plain-English incident report: what failed, where it sits on the machine, a
step-by-step fix, and an escalation flag when a specialist is required.

**Read-only at the architectural level** — no write path to any device register. No OEM warranty
exposure, no integrator conflict, and no liability from an AI-triggered action, because the
system never takes one.

The inference layer is provider-swappable at runtime, including a fully local, air-gap-compatible
option for classified, ITAR, and nuclear-adjacent sites where fault data cannot leave the
building.

Provisional patent filed with the USPTO, May 2026. *Implementation details withheld.*

---

### Trading System — algorithmic trading research
Multi-ticker equity bot on paper trading with a local-model quant gate that blocks any entry
failing its checks, an exchange-holiday-aware market clock, automatic halt on repeated faults, a
dead-man watchdog, and phone push escalation.

Built a backtesting lab with a realistic cost model — spread plus slippage, no look-ahead, fixed
out-of-sample parameters — and tested three strategy hypotheses against history. Mean reversion
proved regime-dependent, overnight drift was cost-killed, and cross-sectional momentum lagged
buy-and-hold.

**Concluded no durable edge and recommended indexing the capital rather than trading it.**
The deliverable is the research lab and the discipline to retire a strategy on evidence.

---

### STARK Exoskeleton
Native desktop command deck registering 12 personal systems with one-click launch, live GPU/VRAM
and local-model telemetry, Git sync state, and drive-mount monitoring — backed by a 267-note
knowledge architecture that lets any model, frontier or local, execute engineering work at a
consistent grade and survive model transitions without losing context.

Includes a council view that convenes multiple frontier models plus the operator in one shared
thread, each answering in sequence and able to hand work to whichever is strongest, followed by a
cross-talk round where a model replies only if it has a material correction.

---

### Systems recovery, hardening, and replication
Recovered 176 GB from a corrupted Windows installation's user profile using backup-mode copy to
bypass access-control entries tied to a dead account, then reclaimed the drive with a scripted
zero-pass format that refuses to run unless four independent conditions verify first — including
that the recovered copy actually exists — so the source is never destroyed on an assumption.

Built local-first peer-to-peer synchronization between two Windows machines over LAN with TLS
device-to-device transfer and conflict-preserving writes. Put the design through adversarial
review *before* implementation, which returned three failure verdicts including a silent
data-loss route, and built from those findings rather than from the working path.

---

### Also built
MCP servers (two pure-stdlib stdio JSON-RPC servers in daily use, one serving a 637-term
plain-language technical translation layer) · a reusable build-time CAD and verification
toolchain · an input-telemetry tool deriving optimal mouse sensitivity from 1.6M+ samples ·
a Godot 4.6 game in development · a self-built OPTA PLC and Emerson VFD industrial system ·
an ESP32 network-scanning device

---

## Background

**Industrial** — 24V to 480V systems, board-level diagnostics, troubleshooting without schematics
or live power. Siemens PLC and Desigo CC building management, Trane HVAC and variable frequency
drives, chillers, air handlers, cooling towers, ERUs. NFPA 70E, OSHA LOTO, EPA 608 Universal.

**Automation** — Siemens TIA Portal, S7-1200/1500, G120 VFD configuration, Ladder Logic,
ProfiNet, HMI configuration, Modbus TCP/RTU, BACnet/IP.

**Software** — Python, Flask, pywebview, three.js, SQLite/PostgreSQL, pandas, local model
deployment, MCP server development, parametric CAD, automated verification engineering.

**Service** — U.S. Army, 173rd Airborne Brigade, 2021–2025. Mortar Team Leader. 28 parachute
jumps. Army Commendation Medal. Secret clearance, inactive and eligible for reinstatement.

---

## Contact

Open to contract work in industrial AI, diagnostics, and systems engineering.

📧 ryanjames0125@icloud.com

<!--
**ryanjames11c/ryanjames11c** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
