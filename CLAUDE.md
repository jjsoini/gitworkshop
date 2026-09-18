# Qvik Git + Claude Code Workshop

Each participant is assigned ONE page under `src/pages/app/`. Build and edit only that page.

## Rules
- Only edit your assigned file in `src/pages/app/`.
- You MAY import and use any component from `src/components/ui/`.
- Do NOT modify shared files: `src/layouts/`, `src/components/`, `src/pages/index.astro`,
  `src/pages/components.astro`, `astro.config.*`, `package.json`, or the lockfile.
- Do NOT add new dependencies. Use Tailwind classes and the existing component kit only.
- Keep every change inside your own page so all work merges without conflicts.

## Tech
- Astro + Tailwind, file-based routing. Adding a file to `src/pages/app/` auto-creates its route
  and its sidebar link.

## Working in this repo
- Run `npm install` once, then `npm run dev` and open the printed URL.
- Browse `/components` (or `src/pages/components.astro`) to see every available component with
  example usage before writing markup from scratch.
- Work on a branch named after your page, e.g. `git checkout -b inbox-alex`.
- Commit, push, and open a pull request on GitHub. Keep the diff to your one page.

## For Claude Code
If the participant asks for a change that would touch a shared file, say so and suggest a way to
do it inside their own page instead. Explain git steps in plain language — many participants are
new to branches and pull requests.
