# Claude Code Prompt: Build TC Systems Website

I need you to build a complete website for Taming Chaos Systems, a Platform Engineering consultancy. This should be a minimal, professional site built with Astro + Tailwind CSS for deployment on Cloudflare Pages.

## Quick Overview
- **Company:** Taming Chaos Systems Ltd
- **Focus:** Platform Engineering (across Dev, AI, Blockchain, Internal Systems)
- **Style:** Minimal, clean, professional, dark mode primary
- **Contact:** contact@tc.systems
- **Domain:** tc.systems

## Tech Stack
- Astro 5.x
- Tailwind CSS 4
- TypeScript (strict)
- Deploy to: Cloudflare Pages via GitHub

## Color Palette

### Dark Mode (Primary)
```css
--primary-cyan: #06b6d4
--secondary-blue: #3b82f6
--bg-dark: #0f172a
--bg-card: #1e293b
--text-primary: #e2e8f0
--text-secondary: #94a3b8
--text-muted: #64748b
```

### Light Mode
```css
--primary-teal: #0891b2
--secondary-blue: #2563eb
--bg-light: #f8fafc
--bg-card-light: #ffffff
--text-primary: #1e293b
--text-secondary: #64748b
--border: #e2e8f0
```

## Site Structure

Create these pages:

### 1. Homepage (`/`)

**Hero Section:**
- H1: "Platform Engineering for Modern Infrastructure"
- Subheading: "Building scalable platforms across Dev, AI, Blockchain, and Internal Systems"
- CTA button: "Get in Touch" → /contact
- Include logo prominently

**What We Do (3 cards):**
1. **Platform Engineering**
   "Creating robust foundations that enable teams to build and deploy with confidence"

2. **Technical Expertise**
   "25+ years of software engineering and architecture experience across traditional and emerging technologies"

3. **Practical Solutions**
   "From blockchain infrastructure to AI platforms - we tame complexity through proven platform engineering practices"

**Bottom CTA:**
- "Ready to tame your chaos?"
- Button: "Contact Us" → /contact

### 2. Services Page (`/services`)

**Header:**
- Title: "Platform Engineering Services"
- Subtitle: "Specialized expertise across modern technology stacks"

**Four Service Cards:**

1. **Platform Engineering** (Primary - make this stand out)
   - Core infrastructure and developer tooling
   - CI/CD pipelines and automation
   - Observability and monitoring
   - Internal developer platforms

2. **Traditional Development**
   - Software architecture and design
   - Backend systems and APIs
   - Legacy system modernization
   - Technical leadership

3. **AI Platform Engineering**
   - AI infrastructure and deployment
   - Model orchestration and MLOps
   - Multi-agent systems
   - AI development workflows

4. **Blockchain Infrastructure**
   - Ethereum execution clients (cdk-erigon contributor)
   - Node infrastructure and operations
   - Blockchain platform development
   - Web3 architecture

**Bottom:** contact@tc.systems

### 3. About Page (`/about`)

**Title:** "About Taming Chaos Systems"

**Content:**

**Who We Are:**
Taming Chaos Systems is a platform engineering consultancy focused on building the foundations that enable modern software teams to move fast without breaking things.

**Experience:**
With over 25 years of software engineering and architecture experience, we bring deep technical expertise across traditional finance, emerging blockchain technologies, and modern platform engineering practices.

**Current Work:**
- Platform Engineering Manager at Insight Investments (asset management)
- Contributing to cdk-erigon (Ethereum execution client development)
- Consulting for Gateway.fm (blockchain infrastructure)

**Approach:**
We believe in practical, proven solutions. Platform engineering isn't about following trends—it's about creating reliable, scalable infrastructure that makes developers' lives easier and businesses more resilient.

**Contact:**
- contact@tc.systems
- LinkedIn: [Add placeholder link]

### 4. Blog Page (`/blog`)

**Title:** "Insights & Technical Writing"
**Subtitle:** "Thoughts on platform engineering, infrastructure, and taming complexity"

**Empty State:**
"Articles coming soon. Follow us on LinkedIn for updates."

**Important:** Set up Astro Content Collections for future blog posts with:
- MDX support
- Tags/categories
- RSS feed configuration
- Create a sample post template in comments

### 5. Contact Page (`/contact`)

**Title:** "Get in Touch"
**Subtitle:** "Let's discuss how platform engineering can help your organization"

Simple centered layout with:
- **Email:** contact@tc.systems
- **LinkedIn:** [Placeholder link]
- **Location:** Crewe, UK (Remote work available)
- **Response Time:** "We typically respond within 24-48 hours"

No contact form - keep it minimal.

## Components to Create

### Header
- Logo (left, links to home)
- Nav: Services, About, Blog, Contact
- Mobile: Hamburger menu
- Sticky on scroll
- Dark background

### Footer
- Logo
- Nav links
- contact@tc.systems
- LinkedIn link
- Copyright: © 2025 Taming Chaos Systems Ltd

### Logo Component
- Accept `variant` prop: 'dark' | 'light'
- Use the logo SVGs I'll provide
- Should work inline in header

### Card Component
- Reusable for services, features
- Subtle border/shadow
- Hover effect
- Responsive

## Design Guidelines

- **Max width:** 1200px for content
- **Spacing:** Generous (2-4rem padding/margins)
- **Typography:** System font stack
- **Cards:** Rounded (0.5-1rem), subtle shadows
- **Transitions:** Smooth (200ms)
- **Responsive:** Mobile-first
- **Aesthetic:** Professional, minimal, clean

## Technical Requirements

1. **Astro Config:**
   - Static site generation
   - Cloudflare adapter
   - TypeScript strict mode

2. **Tailwind Config:**
   - Custom color palette (use variables above)
   - Typography plugin
   - Forms plugin (if needed)

3. **SEO:**
   - Meta titles/descriptions all pages
   - Open Graph tags
   - Sitemap.xml
   - Robots.txt
   - Structured data (Organization schema)

4. **Performance:**
   - Target Lighthouse 95+ on all metrics
   - Optimized images
   - Minimal JavaScript

5. **Accessibility:**
   - Semantic HTML
   - ARIA labels where needed
   - Keyboard navigation
   - WCAG AA color contrast

## Cloudflare Pages Setup

Create `wrangler.toml`:
```toml
name = "tc-systems"
compatibility_date = "2024-01-01"

[build]
command = "npm run build"
publish = "dist"
```

## Project Structure
```
/
├── public/
│   ├── logo-dark.svg
│   ├── logo-light.svg
│   ├── logo-wordmark-dark.svg
│   ├── logo-wordmark-light.svg
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Header.astro
│   │   ├── Footer.astro
│   │   ├── Logo.astro
│   │   └── Card.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   ├── services.astro
│   │   ├── about.astro
│   │   ├── contact.astro
│   │   └── blog/
│   │       └── index.astro
│   ├── content/
│   │   ├── config.ts
│   │   └── blog/
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── tailwind.config.mjs
├── tsconfig.json
└── package.json
```

## README Requirements

Include in README.md:
- Project overview
- Setup instructions
- Development commands
- Deployment steps (Cloudflare Pages)
- Logo files explanation
- Content editing guide

## What NOT to Include
- Contact forms
- Case studies/portfolio
- Pricing
- Analytics (will add later)
- Cookie banners
- Complex animations
- External dependencies beyond Astro/Tailwind

## Logo Files

I'll provide these SVG files separately:
- `logo-dark.svg` - Icon only (dark mode)
- `logo-light.svg` - Icon only (light mode)
- `logo-wordmark-dark.svg` - Full logo with text (dark)
- `logo-wordmark-light.svg` - Full logo with text (light)
- `favicon.svg` - Simplified for favicon

Place these in the `public/` directory.

## Key Points

1. **Keep it minimal** - Less is more
2. **Dark mode primary** - Light mode optional
3. **Content should breathe** - Generous whitespace
4. **Platform Engineering is the hero** - Make this the focus
5. **Professional but not boring** - Clean and modern
6. **Mobile responsive** - Test all breakpoints
7. **Fast loading** - Optimize everything

## Deliverables

- [ ] Complete Astro site with all 5 pages
- [ ] Responsive design (mobile, tablet, desktop)
- [ ] Dark mode implemented
- [ ] All components created
- [ ] Blog structure ready (no posts)
- [ ] SEO configured
- [ ] Cloudflare Pages config
- [ ] Clean, commented code
- [ ] Comprehensive README

## Success Criteria

- Site loads fast (< 2s)
- Lighthouse scores 95+
- Mobile-friendly
- Professional appearance
- Easy to maintain
- Ready for Cloudflare deployment
- Blog ready for future posts

---

**Start by:**
1. Creating the Astro project with TypeScript
2. Installing and configuring Tailwind
3. Setting up the project structure
4. Creating the Layout component
5. Building Header and Footer
6. Creating each page systematically
7. Testing responsive design
8. Adding SEO elements
9. Creating deployment config

Let me know when you're ready and I'll provide the logo SVG files to add to the project.
