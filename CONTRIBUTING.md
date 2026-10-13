# Contributing to Pullr

Thanks for helping. Pullr is Apache-2.0 licensed; by contributing you agree your work is released under the same license.

## Setup
```
npm install
npm run dev
```
Checks (the same ones CI runs): `npm run lint && npm run typecheck && npm test && npm run build`.

## Ground rules
- **Layers.** `src/core` is pure TypeScript: no DOM, no Three.js. `src/io` depends on `core` only. See [docs/architecture.md](docs/architecture.md).
- **Every document change is a Command.** Tools never mutate the mesh directly.
- **Tolerance.** Use `EPS` from `src/core/eps.ts`; never compare floats with `===`.
- **Tests.** Geometry operations need unit tests, and `validateMesh` must return no errors afterwards.
- **No network calls or telemetry.** Everything runs client-side.
- **Original assets only.** Do not copy branding, icons, cursors or colors from other modeling tools.
- Keep commits small with clear messages.

## Reporting bugs
Use the issue template and attach an exported project file when geometry is involved.
