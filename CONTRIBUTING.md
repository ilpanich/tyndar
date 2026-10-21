# Contributing to Tyndar

Tyndar is currently at the planning and repository bootstrap stage. The most useful initial contributions are design clarifications, review of protocol and recovery contracts, and focused implementation work tied to the roadmap.

## Before making a change

Read the [project overview](README.md), [documentation guide](docs/README.md), and relevant [roadmap work item](docs/iot-platform-roadmap.md). For implementation, also review the corresponding [software design](docs/iot-platform-software-design.md) requirements and acceptance evidence.

Keep changes focused. For architecture or scope changes, explain the problem and tradeoffs in an issue or pull request, and update the affected design and roadmap sections together. Historical research and external references should remain distinguishable from current project decisions.

## Documentation changes

- Use **Tyndar** consistently as the project name.
- Use relative links for repository files and check that their targets and section anchors exist.
- Describe planned capabilities as planned until implementation and relevant validation exist.
- Preserve source dates and reference provenance when updating research.
- If changing the scout, update its companion SHA-256 in the software design.

## Implementation changes

Follow the roadmap's initial vertical slice and keep the software design's domain, transport, storage, and identity boundaries explicit. Include meaningful validation for the behavior introduced, and report what was run and what remains unverified in the pull request.

No build system or test suite is present yet. The initial implementation must add reproducible toolchain, setup, build, and test instructions alongside the code.

## License

Contributions are made under the repository's [Apache License 2.0](LICENSE). Identify third-party dependencies and their licenses when introducing them.
