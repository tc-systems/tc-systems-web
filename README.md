# Taming Chaos Systems - Website

Professional platform engineering consultancy website built with Astro & Tailwind CSS.

## Tech Stack

- **Astro 5.x** - Static site generation
- **Tailwind CSS 3** - Styling
- **TypeScript** - Type safety (strict mode)
- **Cloudflare Pages** - Deployment target

## Project Structure

```
/
├── public/              # Static assets (logos, favicon)
├── src/
│   ├── components/      # Reusable UI components
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── Logo.astro
│   │   └── Card.astro
│   ├── layouts/
│   │   └── Layout.astro # Main layout w/ SEO
│   ├── pages/          # Site pages (auto-routed)
│   │   ├── index.astro
│   │   ├── services.astro
│   │   ├── about.astro
│   │   ├── contact.astro
│   │   └── blog/
│   ├── content/        # Content collections
│   │   └── config.ts   # Blog schema
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── tailwind.config.mjs
└── wrangler.toml       # Cloudflare config
```

## Development

### Prerequisites

- Node.js 18+
- npm

### Setup

```bash
npm install
```

### Run Dev Server

```bash
npm run dev
```

Site runs at `http://localhost:4321`

### Build for Production

```bash
npm run build
```

Output → `dist/`

### Preview Production Build

```bash
npm run preview
```

## Deployment

### Cloudflare Pages (GitHub Integration)

1. Push to GitHub
2. Connect repo to Cloudflare Pages
3. Build settings:
   - Build command: `npm run build`
   - Output directory: `dist`
   - Node version: 18+

Site deploys automatically on push to main.

### Manual Deployment

```bash
npm run build
npx wrangler pages deploy dist
```

## Logo Files

Located in `public/`:

- `logo-dark.svg` - Icon (dark mode)
- `logo-light.svg` - Icon (light mode)
- `logo-wordmark-dark.svg` - Full logo (dark)
- `logo-wordmark-light.svg` - Full logo (light)
- `favicon.svg` - Browser favicon

## Content Editing

### Pages

Edit `.astro` files in `src/pages/`:
- Homepage → `index.astro`
- Services → `services.astro`
- About → `about.astro`
- Contact → `contact.astro`

### Blog Posts (Future)

1. Create `.md` or `.mdx` files in `src/content/blog/`
2. Include frontmatter:

```yaml
---
title: "Your Post Title"
description: "Brief description"
pubDate: 2025-01-15
tags: ["platform-engineering", "devops"]
---
```

3. Uncomment blog post rendering in `src/pages/blog/index.astro`

## SEO

All pages include:
- Meta titles & descriptions
- Open Graph tags
- Structured data (Organization schema)
- Sitemap (auto-generated)
- Robots.txt

Edit SEO per page via Layout props.

## Styling

### Color Palette

Dark mode (primary):
- Cyan: `#06b6d4` → `text-cyan-400`, `bg-cyan-500`
- Background: `#0f172a` → `bg-dark-bg`
- Card: `#1e293b` → `bg-dark-card`
- Text: Slate variants

### Customization

Edit `tailwind.config.mjs` for theme changes.
Global styles → `src/styles/global.css`

## Performance

Target: Lighthouse 95+
- Static site generation
- Minimal JavaScript
- Optimized assets
- Semantic HTML

## License

© 2025 Taming Chaos Systems Ltd
