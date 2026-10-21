# abose7ly Silkroad Hub

A Windows desktop companion project for organizing Silkroad Online client profiles, safely launching configured clients, managing plug-in metadata, and validating local files.

**Status: foundation / not yet build-verified.** This repository is a starting point, not a completed bot or a claim of compatibility with every Silkroad server.

## Initial target

- First compatibility target: official iSRO client.
- Later targets: selected vSRO/private-server client builds, each tracked and tested independently.
- UI languages: Arabic and English.
- Proposed desktop stack: C# / WPF on .NET 8.

## Planned modules

1. **Client profiles** — named profiles with client path, server label, character label, and per-profile settings.
2. **Multi-client manager** — launch and monitor explicitly configured client processes; no credential capture.
3. **Client compatibility adapters** — per-build adapters selected by an explicit version/profile; unsupported clients must report `not verified`.
4. **Character/item/skill information** — only through documented, user-authorized data sources or formats; no bypassing game protections.
5. **Plug-in registry** — metadata, versioning, compatibility declaration, enable/disable, and trust checks.
6. **File validation and updates** — SHA-256 verification against a trusted manifest. Never treat a locally generated hash as proof of authenticity.
7. **Automation** — only permitted, safe repetitive actions, subject to client compatibility and server rules.

## Compatibility policy

“Supports all servers” is a goal, not a verified statement. Silkroad clients can differ by build and server-side configuration. Track each tested client separately using `docs/COMPATIBILITY.md`; do not report compatibility without a reproducible test.

## Build prerequisites

- Windows 10/11
- .NET 8 SDK (Windows Desktop workload)
- Visual Studio 2022 or `dotnet` CLI

This repository is currently a planning and source foundation. A successful build, runtime test, installer, and iSRO integration have **not** yet been verified.

## Security

- Do not store game passwords or session tokens.
- Do not disable or evade anti-cheat/security protections.
- Only use plug-ins you trust and have permission to run.
- Verify update manifests through a trusted release channel before applying updates.

## Roadmap

See [docs/ROADMAP.md](docs/ROADMAP.md) and [docs/COMPATIBILITY.md](docs/COMPATIBILITY.md).
