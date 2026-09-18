# Qvik Git + Claude Code Workshop

A small [Astro](https://astro.build) + [Tailwind CSS](https://tailwindcss.com) app used as a
practice ground for the everyday git flow: **branch → commit → push → pull request**.

Everyone in the workshop owns **one page**. Because nobody edits the same file, all of our pull
requests merge cleanly — which is exactly the point.

## Getting started

```bash
npm install   # download dependencies (only needed once)
npm run dev   # start the dev server
```

Then open the printed URL (usually http://localhost:4321).
Edit a file, save, and the browser updates instantly.

Other commands:

```bash
npm run build     # build the production site into dist/
npm run preview   # preview that production build locally
```

## Your page

You are assigned one file in `src/pages/app/` — for example `src/pages/app/inbox.astro`.
That file *is* the route: it shows up at `/app/inbox` and appears in the left sidebar
automatically. **Edit only that file.**

There are ten pages:

| Page | File | URL |
| --- | --- | --- |
| Analytics | `src/pages/app/analytics.astro` | `/app/analytics` |
| Billing | `src/pages/app/billing.astro` | `/app/billing` |
| Calendar | `src/pages/app/calendar.astro` | `/app/calendar` |
| Dashboard | `src/pages/app/dashboard.astro` | `/app/dashboard` |
| Inbox | `src/pages/app/inbox.astro` | `/app/inbox` |
| Profile | `src/pages/app/profile.astro` | `/app/profile` |
| Reports | `src/pages/app/reports.astro` | `/app/reports` |
| Settings | `src/pages/app/settings.astro` | `/app/settings` |
| Tasks | `src/pages/app/tasks.astro` | `/app/tasks` |
| Team | `src/pages/app/team.astro` | `/app/team` |

## Ready-made components

Don't start from a blank page. `src/components/ui/` contains a kit of styled components —
Button, Card, Badge, Alert, Input, Textarea, Label, Avatar, Stat, Table, Tabs, Accordion,
Switch, Progress and Breadcrumb.

Open **[/components](http://localhost:4321/components)** in the running app to see every one of
them rendered, with a copy-pasteable snippet underneath.

To use one, import it at the top of your page:

```astro
---
import Button from '../../components/ui/Button.astro';
import Card from '../../components/ui/Card.astro';
---

<Card>
  <span slot="title">My section</span>
  <p>Some content.</p>
  <div slot="footer"><Button size="sm">Do the thing</Button></div>
</Card>
```

## Don't touch these

These are shared — changing them causes merge conflicts for everyone:

- `src/layouts/` — the app shell and sidebar
- `src/components/` — the component kit
- `src/pages/index.astro` and `src/pages/components.astro`
- `astro.config.mjs`, `package.json`, `package-lock.json`

Also: **no new dependencies**. Tailwind classes and the existing kit are enough.

## The git flow

1. **Get the latest main**

   ```bash
   git checkout main
   git pull
   ```

2. **Make your own branch** — name it after your page and yourself:

   ```bash
   git checkout -b inbox-alex
   ```

3. **Edit your page**, then check it in the browser (`npm run dev`).

4. **Commit** your work:

   ```bash
   git add src/pages/app/inbox.astro
   git commit -m "Add message filters to the inbox page"
   ```

5. **Push** your branch:

   ```bash
   git push -u origin inbox-alex
   ```

6. **Open a pull request** — git prints a link after pushing, or use the GitHub website, or:

   ```bash
   gh pr create --fill
   ```

7. Someone reviews it, and it gets merged into `main`. 🎉

## Doing this with Claude Code

Claude Code can do all of the above with you. Useful things to ask:

- *"What does my page look like right now? Walk me through the file."*
- *"Add a stats row and a table of recent messages to my page, using the component kit."*
- *"Create a branch, commit my change with a good message, and push it."*
- *"Open a pull request for me."*

`CLAUDE.md` in this folder tells Claude the workshop rules, so it will warn you if a change would
touch a shared file.
