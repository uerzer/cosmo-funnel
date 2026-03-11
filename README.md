# COSMO Funnel

Full Brunson-style 7-page astrology/MBTI conversion funnel. Captures leads with birthday + MBTI quiz, delivers personalized cosmic blueprint, and monetizes via three OTO price points.

## Funnel Map

| Page | File | Purpose | Price |
|------|------|---------|-------|
| 1. Lead Capture | `index.html` | Birthday + MBTI form, collects lead, routes to quiz | Free |
| 2. Quiz | `quiz.html` | Interactive astrology + MBTI personality quiz | Free |
| 3. Results + Core OTO | `results.html` | 3 free reveals + $9 paywall for full 40-page blueprint PDF | $9 |
| 4. Upsell 1 | `upsell.html` | Compatibility report OTO | $27 |
| 5. Upsell 2 | `upsell2.html` | Advanced reading OTO | $47 |
| 6. Downsell | `downsell.html` | Reduced offer for upsell declines | TBD |
| 7. Thank You | `thankyou.html` | Order confirmation + delivery | - |

## Content Assets

- `ads.html` - Ad copy and creative assets
- `tiktok-scripts.html` - TikTok content scripts for traffic

## Price Points

- **Core product:** $9 (full 40-page cosmic blueprint PDF)
- **Upsell 1:** $27 (compatibility report)
- **Upsell 2:** $47 (advanced reading)
- **Max cart value:** $83 per customer

## Payment Status

**Not yet wired.** Buy buttons currently call `purchase()` / `addCompatibility()` JS functions that redirect to the next funnel page without charging.

Payment processor decision pending: **Stripe vs Gumroad TBD.**

- Gumroad: fastest to launch, built-in PDF delivery, no-code embeds
- Stripe: more control, custom checkout, requires backend or Netlify functions

See issue #1 for tracking.

## Deploy

This is a static HTML funnel - deploy to any static host:

```bash
# GitHub Pages
git clone https://github.com/uerzer/cosmo-funnel
cd cosmo-funnel
# Enable Pages in repo Settings > Pages > main branch

# Netlify (drag & drop)
# 1. Go to netlify.com
# 2. Drag the cosmo-funnel folder onto the deploy zone
# 3. Live in 30 seconds

# Cloudflare Pages
# 1. Connect repo at pages.cloudflare.com
# 2. No build command needed (static HTML)
# 3. Deploy
```

## File Structure

```
cosmo-funnel/
├── index.html       # Step 1: Lead capture (birthday + MBTI form)
├── quiz.html        # Step 2: Interactive quiz
├── results.html     # Step 3: Results + $9 OTO paywall
├── upsell.html      # Step 4: $27 compatibility report
├── upsell2.html     # Step 5: $47 advanced reading
├── downsell.html    # Step 6: Reduced offer
├── thankyou.html    # Step 7: Order confirmation
├── ads.html         # Ad creatives and copy
└── tiktok-scripts.html  # TikTok content scripts
```

## Status

- [x] All 7 funnel pages built
- [x] Quiz flow working
- [x] Results page with 3 free reveals + paywall
- [ ] Payment processor wired (Stripe/Gumroad - see issue #1)
- [ ] PDF delivery automated
- [ ] GitHub Pages enabled
- [ ] Traffic source connected
