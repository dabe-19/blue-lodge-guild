## Guild Module Submission / Update

- **Module ID:** `<my-module>`
- **Version:** `vX.Y.Z`
- **Repository:** `https://github.com/<user>/mod-<my-module>`
- **Pinned Commit SHA (40 chars):** `<sha>`
- **License:** Apache-2.0 / MIT / BSD / ISC / MPL-2.0

### Checklist
- [ ] `module.json` `version` matches `catalog.json` `version`
- [ ] Module CI & unit tests pass on the pinned commit
- [ ] Zero `shell=True`, `eval`, `exec`, or DOM `innerHTML` sinks
- [ ] Zero hardcoded secrets, personal paths, or private endpoints
