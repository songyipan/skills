# Migration Checklist

1. Copy one ESLint variant from `assets/templates/tooling/eslint/` to project root as `eslint.config.mjs`.
2. Copy `assets/templates/tooling/eslint/prettier.config.cjs` to project root.
3. Update `package.json` scripts:
   - `lint`: `eslint . --ext .js,.jsx,.ts,.tsx,.vue`
   - `format`: `prettier . --write`
4. Install missing deps for selected variant.
5. Copy one VSCode settings template to `.vscode/settings.json`.
6. Copy `assets/templates/tooling/vscode/extensions.json` to `.vscode/extensions.json`.
7. Run:
   - `pnpm eslint .`
   - `pnpm prettier . --check`
8. Fix remaining violations, then enable CI check.
