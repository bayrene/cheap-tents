# CheapTents.com — Budget Tent Review & Affiliate Site

A static affiliate website reviewing the best budget camping tents, monetized through Amazon Associates. Designed for deployment on GitHub Pages.

## Quick Start

1. **Clone the repo**
   ```bash
   git clone https://github.com/bayrene/cheap-tents.git
   cd cheap-tents
   ```

2. **Replace the affiliate tag**
   Do a global find-and-replace across all `.html` files:
   - Find: `YOURTAG-20`
   - Replace with: your actual Amazon Associates tracking tag (e.g., `mysite-20`)

   On Mac/Linux:
   ```bash
   sed -i 's/YOURTAG-20/mysite-20/g' *.html
   ```

   On Windows (PowerShell):
   ```powershell
   Get-ChildItem *.html | ForEach-Object { (Get-Content $_) -replace 'YOURTAG-20','mysite-20' | Set-Content $_ }
   ```

   Or use your text editor's "Find and Replace in Files" feature.

3. **Deploy to GitHub Pages**
   - Push the repo to GitHub
   - Go to **Settings > Pages**
   - Set Source to "Deploy from a branch"
   - Select **main** branch, **/ (root)** folder
   - Click Save
   - Your site will be live at `https://yourusername.github.io/cheap-tents/` within a few minutes

4. **Custom domain (optional)**
   - In GitHub Pages settings, enter your custom domain (e.g., `cheaptents.com`)
   - Add a `CNAME` record with your DNS provider pointing to `yourusername.github.io`
   - GitHub will auto-provision an SSL certificate

## Site Structure

```
index.html                          — Homepage with all 5 product reviews
best-cheap-tents-under-50.html      — "Cheap tents under $50" keyword page
best-cheap-tents-for-camping.html   — "Best cheap camping tents" keyword page
best-cheap-tent-for-backpacking.html — "Cheap backpacking tent" keyword page
best-family-tent-under-150.html     — "Best family tent under $150" keyword page
buying-guide.html                   — "How to Choose a Budget Tent" guide
about.html                          — About page (E-E-A-T signals)
privacy.html                        — Privacy policy
disclaimer.html                     — Affiliate disclosure (required by FTC/Amazon)
style.css                           — Shared stylesheet
sitemap.xml                         — XML sitemap for search engines
robots.txt                          — Crawler directives
```

## Products Reviewed

| Tent | ASIN | Price Range | Target Buyer |
|------|------|-------------|--------------|
| Coleman Sundome 4-Person | B014LSDUA8 | ~$55–$75 | Best overall / beginners |
| Coleman Skydome 4P Dark Room | B0DJCF5L53 | ~$90–$130 | Hot weather / comfort |
| Naturehike Cloud-Up 2 | B08L3XPMVL | ~$70–$110 | Backpackers / ultralight |
| CORE 6-Person Instant Cabin | B0B18R5TKH | ~$110–$140 | Families |
| Wakeman 2-Person Pop-Up | B07DNSJ8CP | ~$25–$40 | Festivals / ultra-budget |

## Tech Stack

- Pure static HTML/CSS/JS — no build tools, no frameworks, no npm
- Google Fonts (Fraunces + DM Sans)
- Mobile-first responsive design
- JSON-LD structured data for rich snippets
- GitHub Pages compatible (no server-side code)

## SEO Features

- Unique title tags and meta descriptions per page
- Self-referencing canonical tags
- Open Graph tags for social sharing
- Product + Review schema markup (JSON-LD)
- XML sitemap + robots.txt
- Semantic HTML with proper heading hierarchy
- Internal linking between all pages

## Amazon Associates Compliance

- Affiliate disclosure on every page with product links
- Dedicated disclaimer page
- No fake urgency, countdown timers, or misleading discounts
- Approximate price ranges (not exact prices)
- `rel="nofollow noopener"` on all affiliate links
- Required Amazon trademark notice in footer

## Customization

- **Colors:** Edit CSS custom values in `style.css` — search for hex codes like `#1e3a2b` (dark green), `#c95d2e` (orange CTA), `#faf6f1` (cream background)
- **Content:** Each HTML file is self-contained and can be edited independently
- **Add pages:** Create a new `.html` file following the same header/footer structure, and add it to `sitemap.xml`
- **Analytics:** Add your Google Analytics snippet to each page's `<head>` section

## License

This project is provided as-is for personal/commercial use. Content is original and may be modified freely.
