# Framework Matrix

## Shared baseline

- `eslint-plugin-simple-import-sort`
- `eslint-plugin-unused-imports`
- `typescript-eslint`
- `eslint-plugin-prettier` + `eslint-config-prettier`
- `eslint-plugin-unicorn` (optional, but useful for naming consistency)

## Expo + React Native

- `eslint-config-expo/flat`
- `eslint-plugin-tailwindcss` (if NativeWind/Tailwind is used)
- Ignore generated native folders: `ios/`, `android/`, `.expo/`

## React + Vite

- `@eslint/js` + `typescript-eslint` flat config
- `eslint-plugin-react-hooks`
- `eslint-plugin-react-refresh` (optional but recommended for Vite)

## Next.js

- `@next/eslint-plugin-next`
- `eslint-plugin-react-hooks`
- Keep Next rules only in this variant; do not place in base

## Vue

- `eslint-plugin-vue` with flat config
- `vue-eslint-parser` for `.vue` files
- Use TypeScript parser inside Vue parser options when TS is enabled

## NestJS

- `@eslint/js` + `typescript-eslint` flat config
- Node/server directories usually require extra ignores (`dist`, generated artifacts)
- Keep API/server rules in NestJS variant only

## Notes

- Keep one Prettier config shared across all frameworks.
- If React Compiler is used, add `eslint-plugin-react-compiler` only where needed.
