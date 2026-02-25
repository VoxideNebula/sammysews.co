# The Stitch Studio — Astro Website

A one-page static website for a seamstress/alterations business.

## Getting Started

```bash
npm install
npm run dev       # Start dev server at localhost:4321
npm run build     # Build for production → ./dist
npm run preview   # Preview production build
```

## Customization Checklist

### 1. Brand Name
Search and replace `The Stitch Studio` in `src/pages/index.astro`
with your actual business name.

### 2. Images
Place your images in `public/images/` with these filenames:

| File | Description |
|---|---|
| `hero.jpg` | Main hero image — a beautiful garment or work-in-progress shot |
| `portrait.jpg` | Photo of the seamstress (About section) |
| `logo.png` | Logo (optional — uncomment the `<img>` tag in the nav) |
| `work-1.jpg` through `work-7.jpg` | Gallery photos of finished work |
| `texture-1.jpg` through `texture-3.jpg` | Close-up fabric/detail shots |

All images will gracefully fall back to colored placeholder boxes if not found.

### 3. Personal Info
In `src/pages/index.astro`, update:

- **[Your Name]** — seamstress name (appears in About section and signature)
- **[Your City]** — location
- **hello@yourstudio.com** — email address
- **(555) 000-0000** — phone number
- **@yourstudio** — Instagram handle
- **About paragraph text** — personalize the bio

### 4. Logo in Nav
Find this block in the nav section and swap the comment:
```html
<!-- Uncomment to use logo image -->
<!-- <img src="/images/logo.png" alt="Studio Logo" class="nav-logo" /> -->
<span class="nav-logo-text">The Stitch Studio</span>
```

### 5. Contact Form
The form is currently a static UI. To make it functional, use:
- **Netlify Forms** (free): Add `data-netlify="true"` and `method="POST"` to the form
- **Formspree** (free tier): Set `action="https://formspree.io/f/YOUR_FORM_ID"`

### 6. Colors
All colors are CSS variables at the top of the `<style>` block:
```css
--plum: #3d2130;       /* Dark backgrounds, headers */
--cream: #f5f0e8;      /* Light backgrounds */
--gold: #b89060;       /* Accents, labels */
--dusty-rose: #c9a79a; /* Soft accent */
```

## Deployment

This is a static Astro site. It works on:
- **Netlify** — drag & drop the `dist/` folder, or connect your repo
- **Vercel** — `vercel --prod`
- **GitHub Pages** — push `dist/` to gh-pages branch
- **Any static host** — upload the `dist/` folder

## Project Structure

```
seamstress-site/
├── public/
│   └── images/        ← Put your photos here
├── src/
│   └── pages/
│       └── index.astro ← The entire site lives here
├── astro.config.mjs
└── package.json
```
