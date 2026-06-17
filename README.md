# Bharni Gems Website

Dark, premium B2B diamond jewellery website. 5 pages, pure HTML/CSS/JS — no framework, no build step.

## File Structure

```
bharni_gems/
├── index.html                  ← Homepage
├── assets/
│   ├── css/
│   │   └── global.css          ← All shared styles & design tokens
│   ├── js/
│   │   └── main.js             ← Nav scroll + reveal animations
│   ├── images/                 ← Add your product images here
│   └── videos/                 ← Add your background videos here
└── pages/
    ├── manifesto.html          ← Brand manifesto / About Us
    ├── vision.html             ← Vision & pillars
    ├── collections.html        ← Product categories (tabbed)
    └── contact.html            ← Trade enquiry form
```

## Customise Before Launch

### 1. Contact Details
Search and replace the following in all files:
- `+91 XXXXX XXXXX` → your real phone number
- `info@bharnigems.com` → your real email
- `Bengaluru, Karnataka` → your full address

### 2. Add Product Images
Place images in `assets/images/`. In `collections.html`, find each card and replace:
```html
<!-- Before -->
<div class="product-card__placeholder">...</div>

<!-- After -->
<img class="product-card__img" src="../assets/images/your-image.jpg" alt="Description">
```
Recommended image sizes:
- Featured cards (wide): 1200 × 600px
- Standard cards: 600 × 600px
- Format: JPG at 80% quality for performance

### 3. Add Hero Video (optional)
In `index.html`, find the commented video block and update the file path:
```html
<video class="hero__video" autoplay muted loop playsinline>
  <source src="assets/videos/hero.mp4" type="video/mp4">
</video>
```

### 4. Product Names & Tags
In `collections.html`, update the product card names, categories, and tags to match your real catalogue.

### 5. Form Submission
The contact form currently shows a success message on submit. To actually receive enquiries, replace the `handleSubmit` function in `contact.html` with your preferred method:
- **Formspree** (free, easy): `<form action="https://formspree.io/f/YOUR_ID" method="POST">`
- **Netlify Forms**: add `netlify` attribute to the form tag
- **Custom backend**: POST to your API endpoint

### 6. Copyright Year
Update the year in each page footer if needed.

## Design Tokens (CSS Variables)

Edit `assets/css/global.css` to adjust the colour palette:
```css
--gold:        #c9a84c;   /* Primary gold */
--gold-light:  #e2c97e;   /* Lighter gold for headings */
--champagne:   #f0e6c8;   /* Main text colour */
--black:       #0a0906;   /* Page background */
--obsidian:    #111009;   /* Card/section backgrounds */
```

## Hosting

Drop the entire `bharni_gems/` folder onto any static host:
- **GitHub Pages** — push to repo, enable Pages in settings
- **Netlify** — drag & drop the folder at app.netlify.com
- **Vercel** — import the folder via CLI or dashboard
- **Any web host** — upload via FTP/cPanel
