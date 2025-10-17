# Repository Guidelines

## Project Structure & Module Organization
- `index.html` houses the full single-page layout, Tailwind CDN setup, and inline scripts; keep new sections grouped by comment blocks already in place (e.g., `<!-- SERVICES -->`).
- `portada.webp` stores the hero artwork; add new media alongside it and reference with relative paths for lightweight deployments.
- Create new partials or experiments inside a temporary `drafts/` folder when needed, then merge the final markup back into `index.html` before committing.

## Build, Test, and Development Commands
- `python3 -m http.server 4173` serves the site locally for quick smoke checks without additional tooling.
- `npx live-server --port=4173` (optional) enables hot reload while editing HTML; install locally with `npm install --save-dev live-server` if frequent previews are required.
- `npx prettier --write index.html` keeps indentation and attribute alignment consistent when large edits are made; add Prettier only for collaborative sessions.

## Coding Style & Naming Conventions
- Use two-space indentation and wrap attributes at sensible breakpoints to maintain readability in deep component blocks.
- Favor semantic HTML elements (`section`, `header`, `nav`) and keep Tailwind utility classes grouped from layout → spacing → color for clarity.
- Name new assets with lowercase-hyphenated patterns (e.g., `compliance-diagram.webp`) and keep them in the repository root until an `assets/` folder becomes necessary.

## Testing Guidelines
- Manually verify anchors, smooth scrolling, and responsive states at 360px, 768px, and 1280px viewports using browser dev tools.
- Run the page through browser Lighthouse audits and fix any performance or accessibility regression before merging.
- Confirm the hero background still loads by checking network requests; replace the external URL with a local asset if availability becomes an issue.

## Commit & Pull Request Guidelines
- Keep commits focused: follow the existing short, imperative style (`inicio`, `add services grid`) and write in English or Spanish consistently through the PR.
- Reference related tickets or context in the pull request body; include before/after screenshots for visual tweaks and list manual QA steps run locally.
- Request at least one peer review before merging; call out sections that need close attention (animations, navigation, responsiveness).
