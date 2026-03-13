# New Client Pitch Setup Guide
**Estimated time:** 15 minutes

This template allows you to quickly customize the pitch deck for any prospective client.

---

## Quick Setup Checklist

### 1. Update CLIENT_CONFIG (5 min)
**Location:** `index.html` — lines 11-43

Update the following values:

```javascript
const CLIENT_CONFIG = {
  name: 'ClientName',                    // Client company name
  logo: 'client-logo.svg',               // Path to client logo
  date: 'Month Year',                    // Pitch date
  employeeCount: 'XX,XXX',              // Total eligible employees
  industry: 'Industry Name',             // Client's industry
  estimatedSavings: '$XXM',              // $3K x employeeCount for 2 years
  primaryContact: {
    name: 'Your Name',                   // Your name
    title: 'Your Title',                 // Your title
    email: 'your.email@sondermind.com', // Your email
    phone: '(XXX) XXX-XXXX'             // Your phone
  },
  painPoints: [                          // 3-4 client-specific pain points
    'Pain point 1',
    'Pain point 2',
    'Pain point 3'
  ],
  showTeamSlide: true,                   // Set to false to hide slide 3
  caseStudies: [{                        // Update with relevant case study
    company: 'Similar Company Type',
    employees: 'XX,XXX',
    result: 'XX% result metric',
    timeframe: 'Year X',
    quote: 'Testimonial quote here'
  }]
};
```

### 2. Replace Client Logo (2 min)
- Save client logo as SVG: `client-logo.svg` (or `.png`)
- Place in root directory
- Update `logo` field in CLIENT_CONFIG
- Logo appears on slides 1 and 16 (last slide)

### 3. Customize Slide 5: The Lockton Opportunity (3 min)
**Make it client-specific:**
- Update the title: "For [ClientName]'s X,XXX employees..."
- Adjust "Current State Challenges" section with client pain points
- Verify savings calculation: `$3K × employee count = estimated savings`
- Update industry-specific context in the challenges

### 4. Optional: Add Relevant Case Study to Slide 14 (3 min)
**Location:** Slide 14 — "Proven Success"

Update the case study card:
- Use a client from same industry or similar size
- Real metrics: "XX% reduction in behavioral health claims"
- Include specific outcomes (utilization, satisfaction, cost savings)
- Add testimonial quote if available

### 5. Update Team Slide (Optional, 2 min)
**Location:** Slide 3 — "Your Team"

Options:
- Keep existing SonderMind team
- Set `showTeamSlide: false` in CLIENT_CONFIG to hide
- Replace with client stakeholder photos for co-branded approach

---

## File Structure for Multi-Client Management

```
lockton-pitch-copy/               # Main template
├── index.html                    # Master deck
├── CLIENT-SETUP.md              # This guide
├── HANDOFF.md                   # Technical documentation
├── sondermind-logo.svg          # SonderMind logo
├── lockton-logo-white.svg       # Lockton logo
└── product-screens/             # Product screenshots

clients/                          # Organized by client
├── lockton/
│   ├── lockton-logo.svg
│   └── config-backup.js         # Save CLIENT_CONFIG values
├── acme-corp/
│   ├── acme-logo.svg
│   └── config-backup.js
└── _template/
    ├── logo-placeholder.svg
    └── config-template.js
```

---

## Slide Order (16 slides after enhancements)

| # | Slide Title | Background | Purpose |
|---|------------|------------|---------|
| 1 | Hero | Cream | Branding + date |
| 2 | Who We Are | Cream | SonderMind vision/mission |
| 3 | Meet Our Team | White | Team credibility (optional) |
| 4 | The Insight | Navy | Industry problem |
| 5 | The [Client] Opportunity | Cream | **Client-specific impact** |
| 6 | The Solution | Cream | 3-pillar overview |
| 7 | AI Coach | White | Product detail |
| 8 | Brain Training | White | Product detail |
| 9 | Self-Care Toolkit | White | Product detail |
| 10 | Engagement | Cream | Engagement programs |
| 11 | Population Insights | White | Analytics dashboard |
| 12 | AI Connect | Cream | Provider network |
| 13 | Quality Care | Cream | Capabilities + stats |
| 14 | Outcomes & ROI | Navy | Clinical + financial outcomes |
| 15 | Proven Success | White | **Case study + social proof** |
| 16 | Next Steps | Navy | **CTA + contact info** |

---

## Brand Guidelines

All changes must stay within SonderMind brand:

### Colors
- **Lake (Navy):** `#004455` — Primary brand, dark backgrounds
- **Cream:** `#F5F0E8` — Warm backgrounds
- **Gold:** `#e8bb25` — Accents, emphasis
- **Turquoise:** `#46b2b8` — Stats, checkmarks
- **White:** `#FFFFFF` — Clean sections

### Typography
- **Headings:** Playfair Display (serif, 500 weight)
- **Body:** proxima-nova
- **Emphasis:** Italic Playfair in gold (light BG) or lake (dark BG)

### Design Rules
- Alternate slide backgrounds (cream/white/navy) for visual rhythm
- Use `<em>` tags for emphasis in headings (auto-styled)
- Keep stats large and impactful
- Maintain clean white space

---

## Testing Checklist

Before sending to client:

- [ ] All CLIENT_CONFIG values updated
- [ ] Client logo displays correctly on slides 1 & 16
- [ ] Employee count appears on slide 5
- [ ] Estimated savings calculation is accurate
- [ ] Contact info displays correctly on slide 16
- [ ] All 16 slides navigate smoothly (test with arrow keys)
- [ ] Case study is relevant to client industry
- [ ] No references to "Lockton" if using for different client
- [ ] Export as PDF for leave-behind (print to PDF)

---

## Where to Get Real Data

### For Slide 5 (The Lockton Opportunity):

#### 1. Employee Count (Required)
**Sources:**
- Primary: Lockton's HR/Benefits contact (most accurate)
- Secondary: LinkedIn company page (approximate)
- Ask: "How many employees are eligible for mental health benefits?"

#### 2. Current Claims/Cost Data (Client-Specific)
**Sources:**
- Lockton's benefits team or their broker
- Request: "Current mental health/behavioral health claims trends"
- Alternative: Use industry benchmarks if client data unavailable
- Note: This is sensitive data—may require NDA

#### 3. Workforce Distribution
**Sources:**
- Lockton stakeholder conversation during discovery
- Ask: "How many offices? What % remote? Geographic spread?"

#### 4. Savings Calculation
**Formula:** `Employee Count × $3,000 = 2-Year Savings`
- Example: 10,000 employees → $30M
- Example: 15,000 employees → $45M
- Source: This $3K per member ROI is documented in SonderMind materials (HANDOFF.md)

---

### For Slide 15 (Proven Success Case Study):

#### Where to Find Real Case Studies:

**Contact these teams internally:**
1. **Sales Team** — Client success stories database
2. **Marketing Team** — Approved case studies and testimonials
3. **Customer Success** — Recent wins with documented metrics

**What to request:**
- "Do we have case studies from insurance/financial services/similar to Lockton?"
- "Which clients can we reference publicly vs. anonymized?"
- "What are our strongest verified ROI metrics?"

#### Verified Metrics to Look For:
✓ % reduction in behavioral health claims
✓ Increase in utilization vs traditional EAP (e.g., "4x higher")
✓ Member satisfaction scores (e.g., "93% satisfaction")
✓ Absenteeism reduction %
✓ Time to measurable impact (e.g., "Year 1", "6 months")

#### If No Case Study Available:
- **Option 1:** Remove slide 15 entirely (deck still works with 15 slides)
- **Option 2:** Use aggregated data: "Our clients typically see 20-40% reduction in claims"
- **Option 3:** Use anonymized: "Confidential Fortune 500 Financial Services Company"
- Mark clearly: "[Aggregated client data]" or "[Industry benchmark]"

---

## Tips for Maximum Impact

1. **Lead with their problem (Slide 5):** The more specific to their actual pain points, the better
2. **Calculate real savings:** Use their actual employee count × $3K (formula above)
3. **Match the case study:** Pick one from same industry if possible
4. **Personalize contact info:** Update your name, title, email, phone in CLIENT_CONFIG
5. **Remove what doesn't apply:** Set `showTeamSlide: false` if not relevant

---

## Support

Questions? Check:
- `HANDOFF.md` — Full technical documentation
- Original deck reference: https://vyoung603.github.io/lockton-pitch/

**Issues or bugs:** Contact dev team or file issue in repo
