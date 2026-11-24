# Blue Lodge Guild — Sovereign Module Catalog

This repository is the SHA-pinned App Store index (`catalog.json`) consumed by Blue Lodge nodes via `/app catalog` and `/app install <module_id>`.

Every entry pins an exact Git commit SHA and passes mandatory static security auditing (`lib/tools/module_audit.py`) and supply-chain wheel verification (`lib/tools/venv_pkg_guard.py`) before activation.

## Official Modules
- **`hunting-buddy`** (`mod-hunting-buddy`): Sovereign parcel GIS, wind & thermal scent cones, offline Leaflet map, bidirectional onX GPX/KML, and Android/PWA mobile GPS & compass heading bridge.
- **`poshtracker`** (`mod-poshtracker`): AI resale appraisal, haggle/offer ML, sell-likelihood scoring, brand knowledge wiki, sourcing watchers, and dynamic MariaDB sidecar/hypervisor switching (Python FastAPI only — zero Blazor).
