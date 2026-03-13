# SonderMind Total Brain Solutions - Client Pitch Deck Template

A templatized horizontal-scroll HTML pitch deck for SonderMind's Total Brain Solutions, designed for easy customization for multiple client presentations.

## 🎯 What This Is

A single-file, self-contained HTML5 sales deck presenting SonderMind's comprehensive mental health platform. Built with scroll-snap navigation, animations, and a template system for rapid client customization.

**Live Demo:** [Original Lockton Deck](https://vyoung603.github.io/lockton-pitch/)

---

## ✨ Features

- **Tech-Solution Forward**: Digital product capabilities first, care provider network second
- **16-Slide Structure**: Problem → Solution → Product Detail → Proof → CTA
- **Template System**: CLIENT_CONFIG for rapid customization (15-min setup per client)
- **SonderMind Brand**: Lake/cream/gold palette, Playfair Display + proxima-nova fonts
- **Navigation**: Arrow keys, spacebar, Home/End, progress dots, prev/next buttons
- **Animations**: Entrance animations on scroll with staggered delays
- **Responsive**: Optimized for 1920×1080 presentation display

---

## 📁 Project Structure

```
lockton-pitch-copy/
├── index.html                    # Main deck (single file, all CSS/JS embedded)
├── README.md                     # This file
├── HANDOFF.md                    # Technical documentation & design system
├── CLIENT-SETUP.md               # 15-minute customization guide
├── sondermind-logo.svg           # SonderMind logo
├── lockton-logo-white.svg        # Client logo (Lockton example)
├── hero-slide20.png              # Hero image
├── who-we-are-photo.jpg          # Team photo
└── product-screens/              # Product screenshots
    ├── slide6.png                # AI Coach
    ├── slide7.png                # Brain Training
    ├── slide8.png                # Self-Care Toolkit
    ├── slide9.png                # Population Insights dashboard
    └── slide9a.png               # Population Insights detail
```

---

## 🚀 Quick Start

### Option 1: View Locally
1. Clone or download this repo
2. Open `index.html` in your web browser
3. Navigate with arrow keys or spacebar

### Option 2: Deploy to GitHub Pages
1. Push to GitHub (see instructions below)
2. Go to repo Settings → Pages
3. Set Source to "main branch"
4. Your deck will be live at: `https://[username].github.io/[repo-name]/`

---

## 🎨 Customizing for a New Client

**Full guide:** See `CLIENT-SETUP.md`

### Quick Steps (15 minutes):

1. **Update CLIENT_CONFIG** in `index.html` (lines 11-48)
   ```javascript
   const CLIENT_CONFIG = {
     name: 'ClientName',
     employeeCount: 'XX,XXX',        // Get from client
     estimatedSavings: '$XXM',        // employeeCount × $3K
     logo: 'client-logo.svg',
     // ... update all fields
   };
   ```

2. **Replace client logo**
   - Save as `client-logo.svg` in root directory
   - Update `logo` field in CLIENT_CONFIG

3. **Fill in placeholders** (marked with `[BRACKETS]` in gold)
   - Slide 5: Employee count, claims data, workforce info
   - Slide 15: Real case study from sales team

4. **Test the deck**
   - Open `index.html` in browser
   - Navigate through all 16 slides
   - Verify all data appears correctly

---

## 📊 Slide Breakdown

| # | Slide Title | Purpose | Customization Needed |
|---|------------|---------|---------------------|
| 1 | Hero | Branding + date | Update date in config |
| 2 | Who We Are | SonderMind vision/mission | None (keep as-is) |
| 3 | Meet Our Team | Team credibility | Optional: hide via config |
| 4 | The Insight | Industry problem | None (verified stats) |
| 5 | **The [Client] Opportunity** | **Client-specific impact** | ⚠️ **Required: Fill all placeholders** |
| 6 | The Solution | 3-pillar overview | None |
| 7 | AI Coach | Product detail | None |
| 8 | Brain Training | Product detail | None |
| 9 | Self-Care Toolkit | Product detail | None |
| 10 | Engagement | Engagement programs | None |
| 11 | Population Insights | Analytics dashboard | None |
| 12 | AI Connect | Provider network | None |
| 13 | Quality Care | Capabilities + stats | None |
| 14 | Outcomes & ROI | Clinical + financial outcomes | None |
| 15 | **Proven Success** | **Case study + social proof** | ⚠️ **Required: Add real case study** |
| 16 | Thank You | Simple closing | None |

---

## 🎨 Brand Guidelines

### Colors (CSS Variables)
```css
--lake: #004455;        /* Primary brand, navy text */
--cream: #F5F0E8;       /* Warm background */
--gold: #e8bb25;        /* Accent, emphasis */
--turquoise: #46b2b8;   /* Checkmarks, stats */
--text: #161616;        /* Body text */
```

### Typography
- **Headings**: Playfair Display (Google Fonts) — serif, 500 weight
- **Body/UI**: proxima-nova (Adobe Typekit)
- **Emphasis**: Use `<em>` tags in headings (auto-styled in gold/lake)

### Design Rules
- Alternate backgrounds: cream → white → navy for visual rhythm
- Never hardcode colors outside `:root` variables
- Use `<em>` for emphasis in headings
- Keep stats large and impactful (3-4rem font size)

---

## 🛠️ Technical Details

### Built With
- Pure HTML5/CSS3/JavaScript (no build process)
- CSS scroll-snap for horizontal navigation
- Intersection Observer API for scroll animations
- Google Fonts (Playfair Display) + Adobe Typekit (proxima-nova)

### Browser Support
- Chrome/Edge (recommended)
- Firefox
- Safari
- Optimized for 1920×1080 presentation displays

### No Dependencies
- Self-contained single HTML file
- No npm, no webpack, no build step
- Edit directly in any text editor

---

## 📚 Documentation

- **HANDOFF.md** — Complete technical documentation
  - Full CSS design system
  - Slide-by-slide breakdown
  - Image sources and specifications
  - Agent prompt for AI-assisted editing

- **CLIENT-SETUP.md** — Customization guide
  - 15-minute setup checklist
  - Where to get real data
  - Testing checklist
  - Multi-client file structure

---

## 🔒 Security & Confidentiality

- Mark final slide with: "SonderMind, Inc. Confidential. For authorized recipients only."
- Don't commit sensitive client data to public repos
- Use `.gitignore` to exclude client-specific configs
- For internal use only - verify with legal before external sharing

---

## 📦 Exporting

### As PDF (for leave-behinds)
1. Open `index.html` in Chrome/Edge
2. Print → Save as PDF
3. Set to Landscape orientation
4. Each slide becomes one PDF page

### As Static Site
Already is! Just open `index.html` — no server required.

---

## 🤝 Contributing

Internal SonderMind project. For updates or issues:
1. Contact the sales enablement team
2. Update `HANDOFF.md` with any structural changes
3. Keep CLIENT_CONFIG template up-to-date

---

## 📄 License

© 2026 SonderMind, Inc. All rights reserved.

For internal SonderMind use only. Not for public distribution.

---

## 🆘 Need Help?

1. **Quick customization questions**: See `CLIENT-SETUP.md`
2. **Technical/design questions**: See `HANDOFF.md`
3. **Can't find case study data**: Contact Sales or Marketing team
4. **Template not working**: Check that CLIENT_CONFIG is properly formatted (valid JavaScript object)

---

## 🎯 Version History

- **v2.0** (Current) — Added templating system, case study slide, simplified final slide
- **v1.0** — Original Lockton pitch deck (April 2026)

---

**Built with 💙 for SonderMind Sales Team**
