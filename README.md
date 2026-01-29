# Ragu AI Website

**Live URL:** https://ragu.ai (pending)  
**Built:** January 29, 2026  
**Status:** MVP Ready for Deployment

---

## Quick Start

### Local Development
```bash
npm install
npm run dev
```

Open browser to `http://localhost:3000`

### Project Structure
```
src/
├── pages/
│   ├── index.html           (Homepage)
│   ├── about.html           (About Ragu)
│   ├── services.html        (Services overview)
│   └── contact.html         (Contact form)
├── css/
│   └── ragu-brand.css       (Brand colors, typography, components)
├── images/                  (Company screenshots, assets)
├── fonts/                   (Plus Jakarta Sans - optional)
└── data/
    └── site.json            (SEO metadata)
```

---

## Brand Identity

### Colors
- **Primary Indigo:** `#2C264A` — Logo, headings, CTAs
- **Secondary Lavender:** `#D9E2FE` — Accents, links (light use)
- **Background:** `#F0F2FA` — Light sections, cards
- **Text:** `#3D3D3D` (dark gray) and `#222222` (black)
- **Accent:** `#CACCD5` (sterling gray)

### Typography
- **Font:** Plus Jakarta Sans (regular, medium, semibold, bold)
- **Headings:** Semibold (600)
- **Body:** Regular (400), min 11pt
- **Hierarchy:** Via weight, not size

### Tone
- Refined gravitas
- Softened intellect
- Cool precision
- No hype language, startup clichés, or exaggerated claims
- AP Style (initial caps, sentence case headlines)

---

## Pages & SEO

| Page | Purpose | Key Content |
|------|---------|-------------|
| **Home** | Establish credibility in 60 seconds | Locked headline: "AI that works for you" + three pillars + CTA |
| **About** | Mission, audience, approach | Why Ragu, who we serve, differentiators |
| **Services** | Three core offerings | Advisory, Platform, Custom Agents |
| **Contact** | Lead generation | Formspree form + email |

### Meta Tags
All pages include:
- Title (unique per page)
- Meta description
- Open Graph tags (og:title, og:description, og:image)
- Viewport for mobile responsiveness

---

## Features

### ✅ Implemented
- [x] Responsive HTML/CSS (no frameworks)
- [x] Ragu brand colors and typography
- [x] Four core pages (Home, About, Services, Contact)
- [x] Contact form integration (Formspree-ready)
- [x] Google Analytics snippet (GA4 placeholder)
- [x] Mobile-first design
- [x] Semantic HTML for accessibility
- [x] SEO meta tags per page

### 🔧 To-Do Before Production
- [ ] **Form Integration:** Update Formspree form ID in `contact.html` line ~90
- [ ] **Analytics:** Replace `G-XXXXX` with actual GA4 ID
- [ ] **Favicon:** Add `favicon.ico` to `src/`
- [ ] **Contact Email:** Update `hello@ragu.ai` with actual contact email
- [ ] **Domain:** Configure custom domain (ragu.ai) in Vercel/Netlify
- [ ] **Case Studies:** Add `/case-studies.html` when content ready
- [ ] **Blog:** Add `/blog/` section for thought leadership
- [ ] **LinkedIn Integration:** Add LinkedIn share buttons on blog posts

---

## Deployment (Vercel)

### Prerequisites
- GitHub account with repo access
- Vercel account (free tier available)

### Steps
1. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial Ragu website"
   git remote add origin https://github.com/Dforword/ragu-website.git
   git push -u origin main
   ```

2. **Deploy to Vercel:**
   ```bash
   npm install -g vercel
   vercel --prod
   ```

3. **Configure domain:**
   - In Vercel dashboard, add custom domain `ragu.ai`
   - Update DNS settings with your domain registrar
   - SSL auto-enabled (free)

4. **Enable auto-deploy:**
   - Vercel auto-deploys on every `main` branch push

---

## Formspree Integration

1. Go to [formspree.io](https://formspree.io)
2. Create a new form, get Form ID (e.g., `f_abcd1234`)
3. Update `contact.html` line 90:
   ```html
   <form id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
4. Replace `YOUR_FORM_ID` with actual ID
5. Test form submission locally

---

## Google Analytics Setup

1. Create GA4 property at [analytics.google.com](https://analytics.google.com)
2. Copy Measurement ID (e.g., `G-XXXXXXXXXX`)
3. Update `index.html` lines 65-67:
   ```javascript
   gtag('config', 'G-XXXXXXXXXX'); // Replace XXXXXXXXXX
   ```
4. Verify tracking via GA Real-time report

---

## Performance & Accessibility

### Lighthouse Scores (Target)
- Performance: ≥ 90
- Accessibility: ≥ 90
- Best Practices: ≥ 90
- SEO: ≥ 90

### To Improve:
- Optimize images (use WebP, lazy load)
- Minify CSS/JS for production
- Add more alt text to images
- Test with axe DevTools extension

---

## Content Updates

### Updating Copy
Edit `.html` files directly in `/src/pages/`:
- Headings, paragraphs, CTAs
- Dates, contact info, links

### Adding Pages
1. Create `new-page.html` in `/src/pages/`
2. Copy header/footer from existing page
3. Add to navigation in all pages
4. Update `site.json` with SEO metadata

### Updating Images
1. Optimize images (JPEG → WebP, resize to max 1600px wide)
2. Place in `/src/images/`
3. Reference in HTML: `<img src="/images/filename.webp" alt="description">`

---

## Maintenance Checklist

- [ ] Update contact email address if changed
- [ ] Monitor form submissions (Formspree inbox)
- [ ] Check Analytics monthly for traffic/behavior
- [ ] Update case studies quarterly
- [ ] Test contact form monthly
- [ ] Review mobile layout quarterly
- [ ] Update copyright year (currently 2026)

---

## Known Issues & Future Work

### Phase 2 (Post-Launch)
- [ ] Add case studies page with 3–4 client stories
- [ ] Launch blog/thought leadership section (from Notion)
- [ ] Integrate LinkedIn feed or share buttons
- [ ] Add testimonials section with client quotes
- [ ] Implement dark mode toggle
- [ ] Add chatbot for common questions
- [ ] Set up marketing automation (email nurture)

### Nice-to-Haves
- [ ] Appointment booking (Calendly embed)
- [ ] Newsletter signup (Mailchimp)
- [ ] Client logo grid (with permissions)
- [ ] Video testimonials
- [ ] Interactive product demo

---

## Support & Contact

- **Website Issues:** hello@ragu.ai
- **Deployment Help:** See Vercel docs at [vercel.com/docs](https://vercel.com/docs)
- **Form Issues:** See Formspree help at [formspree.io/help](https://formspree.io/help)

---

## License

© 2026 Ragu AI. All rights reserved.

---

**Built with care for leaders who demand excellence.**