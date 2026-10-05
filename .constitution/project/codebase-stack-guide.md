---
status: Accepted
ratified_by: 5903b59
playbook:
  repo: wiradeltaid/ops
  path: research/wdi-ecosystem-strategy/coding-playbook/
  local: D:\Developer\wiradeltaid\ops\research\wdi-ecosystem-strategy\coding-playbook\
  rev: 5903b59
reads:
  - 01-principles.md
  - 02-architecture-and-structure.md
  - 03-essential-conventions.md
  - 04-file-size-and-cohesion.md
  - 06-tooling-and-ratchet.md
  - 07-ui-architecture-and-design-system.md
  - stack/rust.md
  - stack/react-typescript.md
excludes:
  - stack/go.md
  - stack/slint.md
  - stack/kotlin.md
  - stack/python.md
  - 05-realtime-and-sync-protocols.md
---

# stack — codebase guide

**Loaded when:** writing or reviewing code.

## 1. Toolchains & Runtimes

- **Desktop Shell & Backend:** Rust (Tauri v2) di `src-tauri/`.
- **Frontend UI:** React 19 / TypeScript 5 + Vite di `src/`.
- **Styling:** CSS Semantic Tokens & Tailwind CSS.

## 2. Command Verifikasi

```powershell
# Frontend
npm run build
npm run lint

# Tauri / Rust
cargo clippy --manifest-path src-tauri/Cargo.toml -- -D warnings
cargo test --manifest-path src-tauri/Cargo.toml
```
