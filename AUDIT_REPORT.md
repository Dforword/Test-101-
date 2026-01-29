# RAGU WEBSITE PROJECT - AUDIT & ACTION PLAN

**Project Date:** 29 January 2026  
**Company:** RAGU (VibeCoded brief)  
**Template:** Foresight (Webflow-exported static site)  
**Status:** Kickoff Complete - Ready for Implementation

---

## 1. PROJECT OVERVIEW

### What You Have:
- **Design Brief:** VibeCoded Website Brief.docx
  - Specifies font: Plus Jakarta Sans (regular, italic, bold, bold-italic)
  - Design system, color palette, and branding guidelines
  
- **Content Strategy:** Website (new)_Approach and Content.docx
  - Pages needed, copy approach, content flow structure
  
- **Template:** Foresight (Webflow-downloaded assets)
  - **Structure:** Static HTML/CSS/JS (export from Webflow)
  - **Pages:** 50+ template pages (home, about, services, pricing, blog, contact, auth, checkout, etc.)
  - **Assets:** CSS (normalize.css, webflow.css, custom), JS (webflow.js), SVG icons, WebP images
  
- **Company Images:** Screenshots in Images.zip (5 files extracted, webflow template has additional images)

---

## 2. TEMPLATE AUDIT

### ✅ Template Structure:
```
foresight-template/
├── index.html (home page)
├── css/
│   ├── normalize.css
│   ├── webflow.css
│   └── foresight-template-c66ef97e1e5cccee9f87.webflow.css
├── js/
│   └── webflow.js (1.5 MB - handles interactions)
├── company/
│   ├── about.html
│   ├── blog.html
│   ├── contact.html
│   └── legal.html
├── features/
│   ├── services-1.html, services-2.html, services-3.html
│   ├── pricing-1.html, pricing-2.html, pricing-3.html
│   └── customers.html
├── landing/
│   ├── landing-1.html, landing-2.html, landing-3.html
├── detail_blog-categories.html
├── detail_post.html
├── detail_product.html, detail_sku.html, detail_category.html
├── checkout.html, order-confirmation.html, paypal-checkout.html
├── user-account.html
├── log-in.html, sign-up.html, reset-password.html
├── 404.html, 401.html, access-denied.html
├── search.html
└── images/ (logo, icons, avatars, product photos)
```

### ✅ Tech Stack:
- **Type:** Static HTML/CSS/JavaScript (Webflow export)
- **CSS Framework:** Custom Webflow CSS + Normalize
- **Font:** Plus Jakarta Sans (embedded in briefs/zips)
- **No Build Step Required:** Ready to deploy as-is or adapt with build tools
- **No Backend:** Pure frontend—contact forms & integrations needed

### ⚠️ Gaps & Customization Needed:

| Item | Current | Action |
|------|---------|--------|
| **Branding** | Generic "Foresight" template | Replace colors, logo, fonts per VibeCoded brief |
| **Content** | Placeholder text | Populate with Ragu company copy from content doc |
| **Images** | Generic Webflow images | Replace with Ragu screenshots & assets |
| **Pages** | 50+ template pages | Select & customize only needed pages (e.g., Home, About, Services, Contact, Blog) |
| **Contact Form** | Static HTML (no backend) | Integrate with Formspree, Netlify Forms, or email service |
| **Analytics** | Not included | Add Google Analytics or Plausible |
| **SEO** | Template meta tags | Update with Ragu meta, OG, Twitter cards, structured data |
| **Responsiveness** | Webflow-built (good) | Verify on mobile/tablet—Webflow is mobile-first |
| **Accessibility** | Good baseline | Audit with WCAG (axe, Lighthouse) |

---

## 3. DELIVERABLES & NEXT STEPS

### Phase 1: Preparation (1–2 days)
1. **Extract & organize assets:**
   - Copy Ragu images from Images.zip → `/images/ragu-*` (renamed)
   - Download Plus Jakarta Sans font files (from brief .docx or Google Fonts)
   - Create `/brand/` folder: colors.css, branding guide
   
2. **Map content:**
   - Identify required pages from content brief (likely: Home, About, Services, Contact, Blog)
   - Create content matrix (pages → sections → copy needs)
   - Document SEO fields (title, meta description, OG image per page)

### Phase 2: Implementation (3–5 days)
1. **Customize template:**
   - Update CSS variables for Ragu brand colors (replace Foresight colors)
   - Replace all placeholder copy with Ragu content
   - Swap template images → Ragu images
   - Customize logo, favicon, branding
   
2. **Implement forms & integrations:**
   - Contact form → Formspree/Netlify Forms (free, no backend)
   - Analytics → Google Analytics 4 or Plausible
   - Optional: Mailchimp newsletter signup
   
3. **Pages to build:**
   - Home (landing-1.html as template)
   - About (company/about.html)
   - Services (features/services-1.html)
   - Blog (company/blog.html + detail_post.html)
   - Contact (company/contact.html + form integration)
   - Legal (company/legal.html)

### Phase 3: Polish & Testing (2–3 days)
1. **SEO:**
   - Add meta tags, Open Graph, Twitter Card to each page
   - Implement structured data (Organization, BreadcrumbList, etc.)
   - Verify canonical URLs
   
2. **Accessibility:**
   - Run Lighthouse audit (aim for ≥90 performance)
   - WCAG AA contrast checks, keyboard navigation
   - Alt text for all images, semantic HTML
   
3. **QA:**
   - Cross-browser (Chrome, Safari, Firefox)
   - Mobile responsiveness (iOS Safari, Chrome Android)
   - Link validation, form testing
   - Performance: image lazy-loading, CSS/JS minification

### Phase 4: Deployment (1 day)
1. **Set up hosting:**
   - Vercel or Netlify (free tier for static sites, auto-deploy from Git)
   - Configure custom domain
   - Enable SSL (automatic on both platforms)
   
2. **Create documentation:**
   - README.md: setup, build, deploy instructions
   - Brand assets guide
   - Content editing guide
   - Known issues & maintenance notes
   
3. **Handoff:**
   - Push to GitHub repo (Dforword/Test-101-)
   - Deploy to live URL
   - Provide access & admin credentials

---

## 4. QUICK WINS (START HERE)

1. ✅ **Extract template to usable folder** (done)
2. 🎯 **Rename & organize images** → `/images/ragu-hero.webp`, etc.
3. 🎯 **Create `/src/` folder structure:**
   ```
   src/
   ├── pages/ (copy HTML files here)
   ├── css/ (theme customizations)
   ├── images/ (Ragu assets)
   ├── fonts/ (Plus Jakarta Sans)
   └── js/ (custom scripts)
   ```
4. 🎯 **Extract design brief content** → Create `content-matrix.md` mapping pages
5. 🎯 **Set up Git + GitHub** → Initialize repo, commit template baseline

---

## 5. TOOLS & SERVICES RECOMMENDED

| Tool | Purpose | Cost |
|------|---------|------|
| **Vercel or Netlify** | Hosting & auto-deploy | Free tier available |
| **Formspree or Netlify Forms** | Contact form backend | Free tier available |
| **Google Analytics 4** | Analytics | Free |
| **Lighthouse CLI** | Performance testing | Free (included w/ Node) |
| **axe DevTools** | Accessibility testing | Free browser extension |
| **ImageOptim or Squoosh** | Image optimization | Free |

---

## 6. ESTIMATED TIMELINE

- **Phase 1:** 1–2 days (prep)
- **Phase 2:** 3–5 days (build pages)
- **Phase 3:** 2–3 days (polish, test)
- **Phase 4:** 1 day (deploy)
- **Total:** 7–11 days (realistic for quality handoff)

---

## NEXT ACTION

→ **Start with Phase 1:** Extract Ragu images, create content matrix, organize folder structure.  
→ Then proceed to Phase 2: Begin customizing template pages with brand colors and copy.

---

*Report Generated: 29 Jan 2026*
