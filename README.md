# skpm Web

**[skpm.org](https://skpm.org)** — the package manager for Skript.

> The static frontend for skpm — package discovery, version browsing, and the project landing page.

---

## Pages

| File | URL | Description |
|---|---|---|
| `index.html` | `/` | Landing page — overview, feature showcase, FAQ |
| `packages.html` | `/packages` | Browse and search all published packages |
| `package.html` | `/package?name=<pkg>` | Per-package detail — versions, files, checksums, requirements |
| `changelog.html` | `/changelog` | Release notes for skpm itself |
| `style.css` | — | Global stylesheet shared across all pages |

---

## How it works

- **No build step.** Every page is plain HTML/CSS/JS — open it in a browser and it runs.
- **All data is live.** Pages fetch directly from `https://registry.skpm.org` at runtime. There is no local data or pre-rendering.
- **No dependencies.** No npm, no bundler, no framework. `style.css` is the only shared asset.

---

## Running locally

Any static file server works:

```bash
# Python
python3 -m http.server 8000

# Node
npx serve .

# Or just open index.html directly in your browser
```

---

## Structure

```
web/
├── index.html       ← landing page
├── packages.html    ← package browser (client-side search + sort)
├── package.html     ← single package view (?name=<pkg>)
├── changelog.html   ← skpm release notes
└── style.css        ← shared styles
```

---

## Related

- **[skpm-dev/cli](https://github.com/skpm-dev/cli)** — CLI tool for publishing packages
- **[skpm-dev/plugin](https://github.com/skpm-dev/plugin)** — Bukkit plugin for installing packages in-game
- **[skpm-dev/registry](https://github.com/skpm-dev/registry)** — Registry API and data store
