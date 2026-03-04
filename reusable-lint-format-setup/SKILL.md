---
name: reusable-lint-format-setup
description: Build or migrate reusable ESLint, Prettier, and VSCode tooling for JavaScript/TypeScript projects. Use when standardizing code style across Expo React Native, React with Vite, Next.js, Vue, and NestJS apps, or when extracting project lint/format settings into reusable templates.
---

# Reusable Lint/Format Setup

Create a cross-framework lint and format baseline with small framework-specific overlays.

## Workflow

1. Read the current project configs:
   - `eslint.config.*` or `.eslintrc*`
   - `.prettierrc*` or `prettier.config.*`
   - `.vscode/settings.json` and `.vscode/extensions.json`
2. Extract shared rules into a base layer:
   - import ordering
   - unused imports and vars
   - TypeScript type import preference
   - filename conventions
   - Prettier rules
3. Add framework overlays only when required:
   - Expo/RN: `eslint-config-expo`, RN-specific ignores, NativeWind/tailwind rules
   - Vite React: browser + React hooks + optional tailwind rules
   - Next.js: `@next/eslint-plugin-next` and app/pages directory constraints
   - Vue: `eslint-plugin-vue` + `vue-eslint-parser`
   - NestJS: Node/TS server-side constraints and API folder layout
4. Keep VSCode setup aligned with ESLint flat config and explicit save actions.
5. Provide copy-ready templates and a migration checklist.

## Required Outputs

- `assets/templates/tooling/eslint/` with base + framework variants.
- `assets/templates/tooling/vscode/` with shared and framework variants.
- `assets/templates/tooling/eslint/prettier.config.cjs` as formatter baseline.
- A short migration doc that explains what to copy for each stack.

## Guardrails

- Prefer ESLint flat config (`eslint.config.mjs`) for new setups.
- Avoid stack-specific plugins in the base config.
- Keep Prettier minimal and stable.
- Default to explicit code actions on save; avoid auto-fixing everything implicitly.

## References

- Use [framework-matrix.md](references/framework-matrix.md) for plugin mapping.
- Use [migration-checklist.md](references/migration-checklist.md) for rollout steps.
- Use [install-deps.md](assets/templates/install-deps.md) for stack-specific `pnpm add -D` commands.
