# EdgeSight — Distributed Edge AI for Environmental Anomaly Detection

**EdgeSight** is a prototype IoT platform that demonstrates lightweight, privacy-preserving edge inference and a centralized event dashboard. Agents (real devices or simulators) compute tiny, local anomaly scores and only send compact alerts and metadata to a server through MQTT. The server stores events and broadcasts them to a dashboard through WebSockets.

This repo is designed for local testing and extension; it contains a device simulator, a tiny anomaly detector suitable for low-power devices, and a central server with a real-time dashboard API.

---

## Project highlights / why it’s interesting
- **Edge-first**: minimizes bandwidth by running a compact model on the device.
- **Privacy-friendly**: raw sensor streams can remain on-device; only alerts + summaries are sent.
- **Extensible**: swap the `anomaly_model` with a TinyML model (TensorFlow Lite), or add additional sensor types.
- **Local dev environment**: `docker-compose` brings up an MQTT broker and server for testing.
- **OTA-ready design**: includes a stubbed OTA update mechanism pattern for real deployments.

---

## Repo layout
.
