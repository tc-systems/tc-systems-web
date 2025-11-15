# TC Systems Website - Build Specification

## Project Overview
Build a minimal, professional website for Taming Chaos Systems - a Platform Engineering consultancy. The site should be clean, impactful, and built with Astro + Tailwind CSS for deployment on Cloudflare Pages.

## Tech Stack
- **Framework:** Astro 5.x
- **Styling:** Tailwind CSS 4
- **Deployment:** Cloudflare Pages
- **Repository:** GitHub (new repo: `tc-systems-website`)

## Design System

### Color Palette
**Dark Mode (Primary):**
- Primary Cyan: `#06b6d4`
- Secondary Blue: `#3b82f6`
- Background Dark: `#0f172a`
- Background Card: `#1e293b`
- Text Primary: `#e2e8f0`
- Text Secondary: `#94a3b8`
- Text Muted: `#64748b`

**Light Mode:**
- Primary Teal: `#0891b2`
- Secondary Blue: `#2563eb`
- Background Light: `#f8fafc`
- Background Card: `#ffffff`
- Text Primary: `#1e293b`
- Text Secondary: `#64748b`
- Border: `#e2e8f0`

### Typography
- Font: System font stack (system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif)
- Headers: Bold (700)
- Body: Normal (400)
- Accents: Medium (500-600)

### Logo
The logo SVG is provided separately. Use the dark mode version by default, with light mode version for light backgrounds.

## Site Structure

### Pages Required
1. **Home** (`/`)
2. **Services** (`/services`)
3. **About** (`/about`)
4. **Blog** (`/blog` - index page only, no posts yet)
5. **Contact** (`/contact`)

### Navigation
Simple header with:
- Logo (left) - links to home
- Nav links (right): Services, About, Blog, Contact
- Mobile: Hamburger menu
- Sticky header on scroll

### Footer
- Logo
- Navigation links
- Contact: contact@tc.systems
- LinkedIn link
- Copyright: © 2025 Taming Chaos Systems Ltd

## Page Content

### Homepage

**Hero Section:**
- Headline: "Platform Engineering for Modern Infrastructure"
- Subheadline: "Building scalable platforms across Dev, AI, Blockchain, and Internal Systems"
- CTA Button: "Get in Touch" → /contact
- Logo/Icon prominently displayed

**What We Do (Brief Section):**
Three column cards:
1. **Platform Engineering** - "Creating robust foundations that enable teams to build and deploy with confidence"
2. **Technical Expertise** - "25+ years of software engineering and architecture experience across traditional and emerging technologies"
3. **Practical Solutions** - "From blockchain infrastructure to AI platforms - we tame complexity through proven platform engineering practices"

**CTA Section:**
- "Ready to tame your chaos?"
- Button: "Contact Us" → /contact

### Services Page

**Header:**
- Title: "Platform Engineering Services"
- Subtitle: "Specialized expertise across modern technology stacks"

**Main Services (4 sections):**

1. **Platform Engineering**
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

**Bottom CTA:**
- "Let's discuss your platform needs"
- contact@tc.systems

### About Page

**Header:**
- Title: "About Taming Chaos Systems"

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

**CTA:**
- contact@tc.systems
- LinkedIn: [Link to LinkedIn profile]

### Blog Page

**Header:**
- Title: "Insights & Technical Writing"
- Subtitle: "Thoughts on platform engineering, infrastructure, and taming complexity"

**Content:**
Empty state message:
"Articles coming soon. Follow us on LinkedIn for updates."

**Structure for future posts:**
- Set up Astro Content Collections for blog
- Support for MDX
- Tags/categories ready
- RSS feed configured

### Contact Page

**Header:**
- Title: "Get in Touch"
- Subtitle: "Let's discuss how platform engineering can help your organization"

**Content:**
Simple, centered layout:

**Email:**
contact@tc.systems

**LinkedIn:**
[LinkedIn Profile Link]

**Location:**
Crewe, UK (Remote work available)

**Response Time:**
We typically respond within 24-48 hours.

No contact form - keep it minimal.

## Design Guidelines

### Layout
- Max width: 1200px for content
- Generous padding/margins (2-4rem)
- Clean whitespace
- Responsive: mobile-first approach

### Components Style
- Minimal borders, prefer subtle shadows
- Rounded corners (0.5-1rem)
- Card-based layouts where appropriate
- Smooth transitions (200ms)
- Hover states on interactive elements

### Aesthetic
- Professional but not corporate
- Technical but approachable
- Clean, modern, minimal
- Dark mode as default
- Optional: Light mode toggle

## Technical Requirements

### Astro Setup
```bash
npm create astro@latest tc-systems-website
# Choose: Empty template, TypeScript (strict), Install dependencies
cd tc-systems-website
npm install -D tailwindcss @astrojs/tailwind
npx astro add tailwind
```

### Project Structure
```
/
├── public/
│   ├── logo-dark.svg
│   ├── logo-light.svg
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
└── package.json
```

### Cloudflare Pages Setup
- Create `wrangler.toml` for deployment config
- Add build command: `npm run build`
- Publish directory: `dist`
- Node version: 18+

### GitHub Actions (Optional)
Simple workflow for automatic deployment to Cloudflare Pages on push to main.

## Content Writing Guidelines
- Keep copy concise and impactful
- Avoid jargon unless necessary
- Focus on value, not features
- Professional tone, slightly technical
- No marketing fluff

## Accessibility
- Semantic HTML
- ARIA labels where needed
- Keyboard navigation
- Color contrast ratios meet WCAG AA
- Alt text for images/logos

## Performance Targets
- Lighthouse score: 95+ on all metrics
- Fast page loads (use Astro's static generation)
- Optimized images
- Minimal JavaScript

## SEO
- Meta titles and descriptions for all pages
- Open Graph tags
- Structured data (Organization schema)
- Sitemap.xml generated
- Robots.txt

## Deliverables
1. Complete Astro site with all pages
2. Logo SVG files integrated
3. Responsive design (mobile, tablet, desktop)
4. Dark mode implemented (light mode optional)
5. Blog structure ready (content collections configured)
6. Cloudflare Pages deployment configuration
7. README with setup and deployment instructions
8. Clean, well-commented code

## Nice to Have (If Time Permits)
- Light/dark mode toggle
- Subtle animations on scroll
- Blog post template example
- RSS feed for blog

## What NOT to Include
- Contact forms
- Case studies/portfolio (add later)
- Pricing information
- Analytics (will add separately)
- Cookie banners
- Complex animations

## Final Notes
- Prioritize simplicity and clarity
- The logo is the main visual element
- Content should breathe
- Less is more
- Focus on platform engineering messaging
- Keep it professional but not boring

---

## Logo SVG Files
(Logo SVG code will be provided separately - both dark and light versions)

## Contact Information
- Email: contact@tc.systems
- Domain: tc.systems
- Company: Taming Chaos Systems Ltd
- Location: Crewe, UK

## Brand Voice
- Confident but not arrogant
- Technical but accessible
- Professional but human
- Clear and direct
- No buzzwords or hype
