# 🧭 The Free Fractional CTO — 90-Day Blueprint

A self-directed curriculum that reproduces the CTOx **attract → convert → serve** arc using only free resources, with a built-in progress tracker (saved to `localStorage`).

**Live:** https://fcto-blueprint.netlify.app/

## What's in here

| File | Purpose |
| --- | --- |
| `index.html` | The curriculum site — single file, no build step, vanilla JS + CSS |
| `og-image.png` | 1200×630 social card (LinkedIn / X / Slack preview) |
| `og-image.svg` | Source for the social card |
| `playbook.html` | Long-form companion "field manual" (separate document) |
| `playbook-print.html` | Print-optimized variant of the playbook |
| `playbook.pdf` | Rendered PDF of the playbook |
| `netlify.toml` | Netlify build config (no build; publish root) |

## Local preview

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

## Deploy

Site is linked to Netlify — pushing to `main` auto-deploys.

Manual deploy:
```bash
npx netlify-cli deploy --dir=. --prod
```

## Editing the curriculum

All items live in the `data` object near the bottom of `index.html`. Each item:

```js
{ id: "uniqueId", star: true, tag: "blog", title: "…", url: "https://…", desc: "…" }
```

- `id` **must be stable** — it's the localStorage key. Change it and you'll reset users' progress for that item.
- `tag`: one of `book | blog | podcast | video | course | network`
- `star: true` marks a non-negotiable (⭐)
