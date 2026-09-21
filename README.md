# Beyond Chat: Clinical AI companion site

This repository contains the Quartz source for the AI × Interclerkship Week companion site.

## Local preview

```bash
npm install
npx quartz build --serve
```

Open the local URL printed by Quartz. Source notes live in `content/`; the generated static site is written to `public/`.

## Production build

```bash
npm ci
npx quartz build
```

Before publishing, set `configuration.baseUrl` in `quartz.config.yaml` to the final hostname without `https://`.

## Content map

- `content/index.md` — landing page
- `content/course-guide.md` — complete session guide
- `content/scorecard.md` — reusable evaluation framework
- `content/glossary.md` — terminology
- `content/where-to-go-next.md` — resources and opportunities
- `content/references.md` — references and source links

Built with Quartz v5.
