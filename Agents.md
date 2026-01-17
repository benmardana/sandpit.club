# Agents.md (Draft)

## Project summary
Sandpit Club is a simple, single-page website for a Melbourne dads community.
The site is intentionally minimal, readable, and easy to maintain.

## Tech stack
- Astro for static pages.
- Tailwind CSS v4 for utilities.
- DaisyUI for components and theme styling.
- `astro-seo` for metadata.

## Repo layout (key paths)
- `src/pages/index.astro`: primary page content.
- `src/assets/app.css`: Tailwind, DaisyUI, and global styles.
- `public/`: static assets (favicon, opengraph).

## Design goals (non-negotiable)
- Simple and straightforward layout.
- Minimal code and minimal complexity.
- Prefer DaisyUI or plain HTML/CSS.
- JS/TS only as a last resort.

## Content and layout guidelines
- Keep content in `index.astro` unless a second page is truly needed.
- Prefer semantic HTML (`main`, `section`, `header`, `footer`).
- Keep components flat; avoid deep component trees.
- Use clear typography and generous spacing.

## Styling guidelines
- Use DaisyUI components and Tailwind utilities first.
- Add custom CSS only when utilities cannot express the design.
- Keep all custom CSS in `src/assets/app.css`.
- Avoid custom fonts or extra font files unless required for readability.

## Interactivity guidelines
- Avoid JS where native HTML works (links, forms, buttons).
- If JS is required, use small, inline scripts in the page.
- No client frameworks unless unavoidable.

## SEO and metadata
- Use `astro-seo` on any new pages.
- Keep titles and descriptions concise and consistent.

## Build and preview
- `pnpm dev` for local dev.
- `pnpm build` for production build.
- `pnpm preview` to verify the build.

## Deployment
- The project is deployed via **Cloudflare Pages**.
- Pushing to `main` triggers a production deployment.
- Pushing to any other branch triggers a preview deployment.
- Preview deployments generate unique URLs for testing changes before merging to main.
