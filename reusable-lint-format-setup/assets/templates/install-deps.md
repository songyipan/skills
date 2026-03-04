# Install Dev Dependencies

Use one block based on your stack.

## Shared baseline (all stacks)

```bash
pnpm add -D eslint prettier eslint-plugin-prettier eslint-config-prettier typescript-eslint eslint-plugin-simple-import-sort eslint-plugin-unused-imports eslint-plugin-unicorn
```

## Expo + React Native

```bash
pnpm add -D eslint-config-expo eslint-plugin-tailwindcss eslint-plugin-react-compiler
```

Notes:
- If you do not use NativeWind/Tailwind, skip `eslint-plugin-tailwindcss`.
- If you do not use React Compiler, skip `eslint-plugin-react-compiler`.

## React + Vite

```bash
pnpm add -D @eslint/js eslint-plugin-react-hooks eslint-plugin-react-refresh
```

## Next.js

```bash
pnpm add -D @eslint/js @next/eslint-plugin-next eslint-plugin-react-hooks
```

## Vue (Vue 3 + TS)

```bash
pnpm add -D @eslint/js eslint-plugin-vue vue-eslint-parser
```

## NestJS

```bash
pnpm add -D @eslint/js
```

## Optional VSCode extensions sync

Copy:

- `assets/templates/tooling/vscode/extensions.json` -> `.vscode/extensions.json`
- one of `assets/templates/tooling/vscode/settings.*.json` -> `.vscode/settings.json`

## Quick verify

```bash
pnpm eslint .
pnpm prettier . --check
```
