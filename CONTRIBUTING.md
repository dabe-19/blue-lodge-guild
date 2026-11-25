# Submitting & Updating Blue Lodge Guild Modules

The **Blue Lodge Guild App Store** (`catalog.json`) is an open, SHA-pinned directory of community and official modules for [Blue Lodge](https://github.com/dabe-19/blue-lodge-public).

You maintain full ownership of your module in your own GitHub repository; this catalog pins your verified release commit SHA so Blue Lodge users can install and update your module safely in one click (`/app install <id>` / `/app update <id>`).

---

## How to Publish a New Module

1. **Create your module repo** from [`dabe-19/mod-starter-template`](https://github.com/dabe-19/mod-starter-template).
2. **Meet the automated Guild CI gates:**
   - Open-source OSI license (`Apache-2.0`, `MIT`, `BSD-3-Clause`, `BSD-2-Clause`, `ISC`, or `MPL-2.0`)
   - Valid `module.json` (`schema_version: 1`, SemVer `version`, `id` matching `^[a-z0-9][a-z0-9_-]{1,48}$`)
   - Zero `shell=True`, `eval()`, `exec()`, or `__import__()` in Python tools
   - Zero `innerHTML`, `outerHTML`, `insertAdjacentHTML`, or `document.write` in UI JS
3. **Tag a release** in your module repository (`v1.0.0`, automated by `.github/workflows/auto-tag-release.yml`).
4. **Open a Pull Request here** adding your entry to `catalog.json` with your exact 40-character `commit` SHA and `https://github.com/<user>/<repo>.git` URL.
5. **Automated Guild CI** clones your exact SHA, checks your manifest & license, and runs the static security audit. Once green and merged, every Blue Lodge node discovers your module automatically!

## How to Publish a Module Update

1. Merge your changes in your own module repo (`module-ci.yml` tests + `auto-tag-release.yml` tags `vX.Y.Z`).
2. Open a small PR updating `version`, `commit`, and `updated_at` in `catalog.json`.
3. Users with your module installed will automatically see an **Update Available** badge in their Blue Lodge App Store!
