# Client compatibility matrix

Status meanings:
- **Not tested** — no reproducible test performed.
- **In progress** — test environment or implementation is being prepared.
- **Verified** — tested on the exact named client build with a recorded result.
- **Unsupported** — known not to work or intentionally excluded.

| Client family | Exact build | Launch/monitor | Profile save/load | Character/items/skills data | Automation | Status |
|---|---|---|---|---|---|---|
| Official iSRO | Not recorded yet | Not tested | Not tested | Not tested | Not tested | Not tested |
| vSRO | Per server/build | Not tested | Not tested | Not tested | Not tested | Not tested |
| Private servers | Must identify each client/build | Not tested | Not tested | Not tested | Not tested | Not tested |

## Required evidence for a verified row
1. Exact client build/version and architecture.
2. Windows version and .NET app build identifier.
3. Steps to reproduce the test.
4. Expected vs actual outcome and logs without passwords/tokens.
5. Explicit note of functionality not tested.

Compatibility with one client build does not imply compatibility with another. This project does not claim universal server support until rows have reproducible evidence.
