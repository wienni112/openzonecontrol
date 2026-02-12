# OpenZoneControl

OpenZoneControl is an open-source platform for zone-based network audio control using MQTT and AES67.

It enables centralized management of distributed audio nodes through a modern web interface, making it easy to build flexible, network-based sound systems for event halls, community venues, rehearsal spaces and custom installations.

Unlike traditional audio systems, OpenZoneControl separates audio transport from control logic:

- AES67 handles low-latency network audio
- MQTT acts as the control plane
- OpenZoneControl provides orchestration, presets and zone management

The result is a modular, vendor-independent audio control system designed for reliability, automation and ease of use.

---

## Key Features

- Zone-based audio routing (hall, stage, foyer, stream, etc.)
- Centralized web interface with preset switching
- MQTT-based node control and status reporting
- Zero-touch node provisioning with token authentication
- AES67 network audio transport
- Distributed architecture (no single point of failure for audio)
- Designed for Raspberry Pi / CM4 audio nodes
- Docker-based backend stack (EMQX, PostgreSQL, API, Web UI)

---

## Architecture Overview

OpenZoneControl consists of four main components:

### Control Backend
Central orchestration service that manages nodes, zones, presets and authentication.

### MQTT Broker (EMQX)
Acts as the control bus between backend and audio nodes.

### Audio Nodes
Embedded Linux devices (Raspberry Pi / Compute Module 4) running:
- AES67 audio pipelines
- PTP synchronization
- Node agent for MQTT communication

### Web Interface
Browser-based UI for operators to switch presets and monitor system status.

Audio streams continue to run even if the backend is offline.

---

## Typical Use Cases

- Event halls
- Community centers
- Clubs and rehearsal spaces
- DIY network audio systems
- Streaming + PA integration
- Zone-based background music systems

---

## Project Goals

- Open and vendor-neutral
- Simple operation for non-technical users
- Professional-grade reliability
- Fully self-hosted
- Designed for automation and integration (Home Assistant, Node-RED, etc.)

---

## Status

OpenZoneControl is currently under active development.

---

## License

MIT (planned)

---

## Contributions

Contributions are welcome.

This project is built for real-world community and event installations — feedback and pull requests are appreciated.
