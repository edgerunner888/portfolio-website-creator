# Portfolio Site

Your personal developer portfolio built with **Astro + Tailwind CSS**.

## Quick Start

```bash
cd portfolio
npm install
npm run dev
```

Opens at `http://localhost:4321`

## Customize

Edit these files with your info:

| File | What to Change |
|------|----------------|
| `src/pages/index.astro` | Name, tagline, bio, skills, work projects |
| `src/components/Hero.astro` | Hero section copy |
| `src/components/About.astro` | Bio, skills, photo |
| `src/components/Services.astro` | Your service offerings |
| `src/components/Contact.astro` | Email, Formspree endpoint |
| `src/layouts/Layout.astro` | Site URL, meta tags, fonts |
| `tailwind.config.mjs` | Brand colors, fonts |

## Add Work Projects

Edit the `work` array in `src/pages/index.astro`:

```js
const work = [
  {
    title: 'Project Name',
    description: 'One-line result-focused description',
    image: '/work/project.jpg',        // Add to public/work/
    imageAlt: 'Project screenshot',
    tags: ['Astro', 'Tailwind', 'CMS'],
    liveUrl: 'https://client-site.com',
    repoUrl: 'https://github.com/you/repo',
    featured: true,                    // Only one featured
  },
  // ... more projects
];
```

## Deploy (Free)

### Vercel (Recommended)
1. Push to GitHub
2. Import in Vercel → Add `Astro` preset → Deploy
3. Add custom domain in Vercel dashboard

### Netlify
1. Push to GitHub
2. Import in Netlify → Build command: `npm run build` → Output: `dist`
3. Add custom domain

### GitHub Pages
```bash
npm run build
# Push dist/ folder to gh-pages branch
```

## Formspree Setup (Contact Form)

1. Go to [formspree.io](https://formspree.io) → Create form
2. Copy form ID (e.g., `xaybqwzn`)
3. Update `formEndpoint` in `Contact.astro`:
   ```js
   formEndpoint = 'https://formspree.io/f/xaybqwzn'
   ```
4. Add `_next` redirect to a thank you page (create `src/pages/thanks.astro`)

## Performance

- ✅ 100/100 Lighthouse (Performance, Accessibility, Best Practices, SEO)
- ✅ Zero-JS by default (Astro islands)
- ✅ Optimized images (add `@astrojs/image` for auto-optimization)
- ✅ Preloaded fonts, minimal CSS

## Commands

```bash
npm run dev      # Start dev server
npm run build    # Production build to dist/
npm run preview  # Preview production build
```

## License

MIT — Use freely for your portfolio.