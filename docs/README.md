# Tyndar documentation

Tyndar is a planned capacity-aware IoT configuration and device shadow platform. These documents describe its proposed behavior and delivery plan; they do not establish that a feature has been implemented or validated.

## Reading guide

1. Read the [product and architecture scout](iot-digital-twin-scout.md) for the problem, market research, alternatives, and product scope.
2. Read the [software design](iot-platform-software-design.md) for the architecture and proposed behavioral contracts.
3. Use the [implementation roadmap](iot-platform-roadmap.md) for work items, dependencies, acceptance evidence, and release sequencing.

The software design owns architecture and protocol semantics. The roadmap owns delivery order and milestone gates. The scout preserves dated market evidence and explains the product direction. Resolve inconsistencies across the documents rather than treating a research observation as an implementation guarantee.

## Imported baseline and project name

The three supplied documents retain their original filenames, v0.3 technical baseline, research dates, references, and milestone identifiers. This repository edition updates the project name to **Tyndar** and replaces the unresolved naming decision. Earlier candidate names remain in the software design as explicitly superseded historical research.

Tyndar is the selected name; exact package namespaces, domains, and any necessary name clearance remain unverified. Naming changes do not mark an implementation milestone complete. The software design's companion scout checksum identifies the updated scout file in this directory.

## Maintaining these documents

- Use **Tyndar** for the project name and `tyndar` for the repository identifier.
- Keep companion links relative so they work in the repository and local Markdown viewers.
- Preserve the distinction between proposed features, measured results, and completed release gates.
- Update affected companion documents when changing requirements or milestone scope.
- Refresh the companion scout SHA-256 in the software design whenever the scout file changes.

See the [contribution guide](../CONTRIBUTING.md) and [project overview](../README.md).
