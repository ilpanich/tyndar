# Tyndar

<p align="center">
  <img src="docs/assets/tyndar-logo.png" alt="Tyndar logo: connected blue and teal twin profiles beneath two gold stars" width="640">
</p>

**Capacity-aware IoT configuration and device shadows.**

Tyndar is an open-source project for managing configuration and state across constrained IoT devices. Its goal is to define typed configuration once, resolve it for each device, check that it fits the device's hardware budgets, and track the exact revision the device reports running.

> **Project status:** planning and repository bootstrap. This repository currently contains the product research, software design, and implementation roadmap. The platform, WebUI, transports, and SDKs described below are planned capabilities; no runnable application or test suite is included yet.

## What Tyndar is designed to do

- Model device families, immutable type versions, typed configuration tables, and reading schemas.
- Check row, storage, RAM, staging, and transfer budgets before deploying configuration.
- Keep desired configuration, device-specific projections, and reported state distinct.
- Deliver configuration with resumable synchronization, safe activation, and explicit recovery behavior.
- Support typed synchronous and asynchronous commands, durable results, and WebRTC signaling.
- Give operators an admin WebUI for definitions, fit reports, deployments, commands, and readings.
- Use AXIAM for identity and authorization, with tenant isolation and device credential lifecycle management.

The initial scope is operational device shadows and configuration reconciliation. Simulation, physics, and 3D visualization are outside that scope.

## Planned architecture

| Area | Design direction |
| --- | --- |
| Backend | Rust modular server; Actix-Web HTTPS and Tonic/Prost gRPC |
| Admin WebUI | Rust/WASM with Leptos, bundled with the server |
| Operational storage | PostgreSQL, with transactional inbox/outbox |
| Identity and authorization | [AXIAM](https://github.com/ilpanich/axiam), integrated as a separate system |
| Device connectivity | HTTPS first, followed by MQTTS and gRPC over TLS; device mTLS where applicable |
| Data contracts | Typed Protobuf and JSON, with versioned schemas and bounded compact framing |
| SDK targets | Rust, TypeScript, Python, Java, Kotlin, C#, PHP, Go, Swift, C, and C++ |

The software design owns the proposed behavior. Integration qualification, version pins, hardware measurements, and conformance tests are roadmap work, rather than established support claims.

## Documentation

Start with the [documentation guide](docs/README.md), or open a document directly:

| Document | Purpose |
| --- | --- |
| [Product research and architecture scout](docs/iot-digital-twin-scout.md) | Motivation, market evidence, alternatives, and product boundaries |
| [Software design](docs/iot-platform-software-design.md) | Architecture, domain model, protocol semantics, security, and verification requirements |
| [Implementation roadmap](docs/iot-platform-roadmap.md) | Milestones M0–M7, dependencies, deliverables, and release gates |

## Development status and next steps

The first implementation work is M0: establish the Rust and WebUI workspaces, qualify AXIAM and broker integrations, pin compatible tools, and define protocol and device recovery contracts. The first external developer preview is planned for M2: capacity-checked HTTPS deployment to a real device, basic commands and readings, and an operator WebUI.

There are currently no dependency installation, build, run, or test commands. Those instructions will be added with the implementation. See the [first implementation iteration](docs/iot-platform-roadmap.md#10-first-implementation-iteration) for the planned sequence.

For documentation and future implementation contributions, see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

Tyndar is licensed under the [Apache License 2.0](LICENSE). Third-party components retain their own licenses; dependency selection and license inventory are part of the implementation roadmap.
