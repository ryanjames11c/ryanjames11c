# Systems I Build

Most of what is here started because I hit a limitation I could not get past.

I usually do not start with:

> "What app should I make?"

I start with:

> "What is stopping the next thing from working?"

Then I observe the system, build a model of it, test the model against reality, find the failure path, and build around it.

**Observe → Model → Test → Update**

I do not work like a traditional software developer.

I define the system, architecture, constraints, verification, failure behavior, and what the finished result needs to do. AI is my primary execution multiplier for implementation, while I remain the operator responsible for testing, troubleshooting, verification, and deciding what survives.

My work spans industrial electrical systems, PLC/HVAC automation, local AI, model inspection, MCP, hardware, recovery systems, CAD, simulation, and AI-assisted engineering.

Most repositories are private.

Source may be available under NDA or on request where it is not patent-sensitive or tied to proprietary control logic.

---

# Selected Systems

## AI Industrial Diagnostic Gateway

A passive, read-only industrial fault-diagnostic system for PLCs, VFDs, HVAC equipment, industrial robots, and safety controllers across 18 device classes.

The system reads protocols including:

- Modbus TCP / RTU
- BACnet/IP
- OPC-UA

and produces a plain-language incident report describing:

- what failed
- where the component sits on the machine
- a step-by-step troubleshooting path
- when the issue should be escalated to a specialist

The system is **read-only at the architectural level**. There is no write path to a device register.

The inference layer can be swapped at runtime, including a fully local configuration for environments where equipment or fault data cannot leave the facility.

The local-model architecture is designed around constrained reference data, operator visibility, failure containment, and escalation rather than trusting unrestricted model generation.

The updated local-AI design is being prepared for provisional patent filing.

Implementation and control details are intentionally withheld.

---

## Local AI Operations Console

A native desktop operating environment for organizing and launching my projects, models, tools, files, and verification workflows.

The console currently registers multiple independent systems and provides:

- one-click project launch
- GPU / VRAM monitoring
- local-model telemetry
- Git synchronization state
- drive and system-state monitoring
- project handoffs
- dedicated project workspaces

It also includes a multi-model **AI Council**.

The Council places multiple frontier models and me into one shared working thread, allowing models to handle different responsibilities instead of asking every model to perform the same job.

The larger workflow separates roles such as:

**vision → build → troubleshoot → observe → verify → update**

I am still the orchestration layer deciding where work moves, what gets challenged, what gets retained, and what gets decommissioned.

The system is backed by a 267-note local knowledge architecture containing operating doctrine, technical references, execution procedures, and project state so that different models can enter the environment without starting from zero.

---

## Local LLM Black Box / Interpretability Panel

A local-model inspection environment built to make model behavior more observable.

Instead of treating a neural network only as an input/output box, the panel provides instrumentation for examining internal behavior through experiments including:

- layer-by-layer inspection
- attention inspection
- logit-lens style reads
- probing and comparison
- steering experiments
- residual patching
- knock-out testing
- universality / representation comparisons
- repeatable saved experimental runs

The interface uses measurement concepts inspired by electrical troubleshooting:

**measure → disturb → compare → isolate**

The goal is not to claim that the inside of a model becomes completely understandable.

The goal is to give the operator useful instrumentation for identifying where behavior changes, testing hypotheses, and finding repeatable patterns.

The deeper detection and control logic is private.

---

## STARK Forge

A reusable build-time engineering and verification toolchain used across projects.

It exists because I kept encountering the same problem:

AI can generate something that looks correct while still being dimensionally, structurally, or logically wrong.

Forge adds independent verification around the build process.

Depending on the project, that includes:

- parametric CAD
- geometry measurement
- pixel-difference auditing
- reference-image comparison
- adversarial review
- deterministic checks
- build validation before handoff

The system is intended to reduce the distance between:

**what I envisioned → what was generated → what actually exists**

---

## Systems Recovery, Hardening, and Replication

Recovered 176 GB from a corrupted Windows user profile using backup-mode copy to bypass permissions tied to the dead installation.

Before reclaiming the original drive, I built a scripted zero-pass process that would not execute unless multiple independent conditions passed first, including verification that the recovered copy actually existed.

The principle was simple:

**never destroy the source because one check said the backup worked.**

I later built local-first peer-to-peer synchronization between two Windows systems over LAN with encrypted device-to-device transfer and conflict-preserving writes.

The design went through adversarial review before implementation.

That review found three failure paths, including a silent data-loss route, and the system was rebuilt around those failures rather than around the happy path.

---

## Algorithmic Trading Research System

A multi-ticker paper-trading research system with:

- local-model quantitative gating
- exchange-calendar awareness
- repeated-fault automatic halt
- dead-man watchdog
- phone escalation
- realistic spread and slippage modeling
- no look-ahead
- fixed out-of-sample testing

Three strategy hypotheses were tested against historical data.

The result was not a trading product.

The evidence showed no durable edge strong enough to justify deploying the capital, so the conclusion was to retire the strategies and favor indexing instead.

The useful result was the research system and the discipline to stop when the evidence stopped supporting the idea.

---

## Interactive Physics and Math Learning Lab

A self-directed learning environment built around reconstruction rather than passive reading.

The application organizes open problems in physics into a structured ledger and combines them with:

- mathematical notation practice
- graded reconstruction exercises
- conceptual decomposition
- self-testing

The lab is a learning instrument.

It is not a claim that I solved the problems it contains.

---

## MCP Systems

I currently use multiple custom MCP servers as part of my daily workflow.

One includes a 637-term plain-language technical translation layer designed to convert unfamiliar terminology into language I can connect to systems I already understand.

My MCP work is increasingly becoming the connective tissue between:

- models
- projects
- local knowledge
- tools
- live system state
- verification
- operator decisions

I treat MCP less as a chatbot extension and more as an interface layer for orchestrated work.

---

# Other Builds

Also built or actively developing:

- ESP32 network-scanning device
- self-built OPTA PLC + Emerson VFD industrial system
- input-telemetry system using 1.6M+ samples to derive mouse sensitivity
- Godot 4.x multiplayer game
- local-first machine replication
- automated CAD and geometry-verification pipelines
- multi-model build / troubleshoot / verify workflows
- local LLM deployment and testing infrastructure
- technical knowledge systems in Obsidian

---

# Industrial Background

My technical background started outside software.

I have worked directly with:

- 24V–480V electrical systems
- industrial wiring
- board-level troubleshooting
- electrical diagnostics without schematics
- Siemens S7-1200 / S7-1500 PLCs
- Siemens TIA Portal
- G120 VFDs
- Desigo CC
- ProfiNet
- HMI systems
- Modbus
- BACnet
- Trane HVAC
- chillers
- air handlers
- cooling towers
- ERUs
- embedded hardware

Safety and trade training includes NFPA 70E, OSHA LOTO, and EPA 608 Universal.

---

# How I Work

I am not trying to make one AI do everything.

I divide work according to the strengths of the system performing it.

A project may have:

- a builder
- a troubleshooting operator
- an independent verifier
- a local observation layer
- a shared AI council
- me as the operator orchestrating the whole system

If something works, I keep it.

If something fails, I try to understand why.

If the component can be tuned, I tune it.

If it cannot justify remaining in the system, I decommission it and keep whatever is still useful.

I am less interested in finding a perfect component than building a system that remains useful when individual components are imperfect.

---

# Current Direction

My current work is moving toward:

**AI orchestration + local models + verification + industrial systems + operator-centered tooling**

The long-term goal is not autonomous AI replacing operators.

It is building systems where AI gives a competent human better visibility, faster access to information, stronger verification, and more leverage without removing accountability from the operator.

---

**Observe. Model. Test. Update.**
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
