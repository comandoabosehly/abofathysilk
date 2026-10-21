# Roadmap — abose7ly Silkroad Hub

## Phase 0 — Repository foundation
- [x] Document goals, boundaries, and honest compatibility status.
- [ ] Add a WPF solution and verify it builds on Windows with .NET 8.
- [ ] Add automated unit tests and a Windows CI build.

## Phase 1 — Client/profile manager
- Model named profiles with server label, client executable path, optional build label, and display language.
- Validate configured paths before launch.
- Start and monitor only user-selected executables; never inject code into the game client.
- Add tests for missing paths, invalid profiles, and concurrent process tracking.

## Phase 2 — iSRO compatibility baseline
- Record the exact official client build, launcher flow, architecture, and test environment.
- Validate launch/close/process status without bypassing the official launcher or anti-cheat.
- Determine which character/item/skill information is available via documented or user-authorized data sources.
- Mark every unsupported data field as unavailable instead of fabricating values.

## Phase 3 — Profiles, data, and plug-ins
- Import/export profiles with schema versioning and safe defaults.
- Add a plug-in manifest with ID, version, supported client builds, permissions, and integrity hashes.
- Disable untrusted or incompatible plug-ins by default.
- Add clear user-visible logs and error messages.

## Phase 4 — File verification and updates
- Verify files against a trusted manifest obtained from a trusted release channel.
- Reject malformed manifests and mismatches; never self-bless files by calculating their hashes as the source of truth.
- Make updates opt-in, with backup and recovery guidance.

## Phase 5 — Automation and wider client coverage
- Add only server-rule-compliant repetitive actions and only through supported interfaces.
- Test specific iSRO builds first, then separately test each named vSRO/private-server build.
- Publish a compatibility matrix based on repeatable tests, not assumptions.

## Release gates
A release is not complete until Windows build, unit tests, launch smoke test, profile persistence tests, file-integrity tests, and manual iSRO compatibility tests are all recorded. Setup.exe is a later deliverable after a reproducible successful build.
