# cisltech.com — Personal Portfolio & Blog

Ian Lazala's personal portfolio and blog, built with [Astro](https://astro.build).

**Live site:** [cisltech.com](https://cisltech.com)

## Stack

- **Framework:** [Astro](https://astro.build) 4.x
- **Content:** Astro Content Collections + Markdown/MDX
- **Styling:** Plain CSS with custom properties (no framework needed)
- **Deployment:** GitHub Pages via GitHub Actions
- **Domain:** cisltech.com (custom domain via CNAME)

## Project Structure

```
├── .github/
│   └── workflows/
│       └── deploy.yml       # Auto-deploy to GitHub Pages on push to main
├── public/
│   ├── CNAME                # Custom domain — cisltech.com
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Nav.astro
│   │   ├── Hero.astro
│   │   ├── Projects.astro
│   │   ├── Skills.astro
│   │   ├── BlogPreview.astro
│   │   └── Footer.astro
│   ├── content/
│   │   ├── config.ts        # Content collection schema
│   │   └── blog/            # Blog posts (Markdown)
│   ├── layouts/
│   │   ├── BaseLayout.astro
│   │   └── BlogLayout.astro
│   ├── pages/
│   │   ├── index.astro      # Home page
│   │   ├── 404.astro
│   │   └── blog/
│   │       ├── index.astro  # Blog listing
│   │       └── [...slug].astro
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── package.json
└── tsconfig.json
```

## Development

```bash
# Install dependencies
npm install

# Start dev server (localhost:4321)
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Adding a Blog Post

Create a new `.md` or `.mdx` file in `src/content/blog/`:

```markdown
---
title: "Your Post Title"
description: "A short description shown in previews."
pubDate: 2025-06-01
tags: ["Tag1", "Tag2"]
---

Your content here...
```

## Deployment

The site auto-deploys to GitHub Pages on every push to `main` via `.github/workflows/deploy.yml`.

For the custom domain to work, you need to configure GitHub Pages in the repo settings:
1. Go to **Settings → Pages**
2. Set source to **GitHub Actions**
3. The `public/CNAME` file handles the custom domain

## Contact

- Email: [ianlazala@gmail.com](mailto:ianlazala@gmail.com)
- GitHub: [@proavl](https://github.com/proavl) / [@CISLTECH](https://github.com/CISLTECH)
