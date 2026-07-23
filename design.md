# Editorial Web Design — Notes

Purpose
- Provide a concise, editorial-style design system and examples for a lightweight F1-themed site.

Design Goals
- Bold, typographic, and grid-driven layout.
- Strong visual hierarchy with large headings and compact metadata.
- High contrast palette with a signature accent color.
- Flexible cards and hero modules for editorial content.

Color Palette
- Primary accent: #E10600 (F1 red)
- Background: #15151E (very dark)
- Surfaces: #1F1F27 / #38383F (dark grays)
- Muted text: #949498
- White: #FFFFFF

Typography
- Font family: Titillium Web (or a condensed/neo-grotesque alternative)
- Scale (suggested):
  - H1: 2.2rem — display/hero
  - H2: 1.6rem — section headings
  - H3: 1.1rem — card headlines
  - Body: 0.95rem
  - Small/meta: 0.85rem

Tone & Imagery
- Photography: large, cinematic hero images; cropped action shots for cards.
- Imagery uses object-fit: cover to preserve impact.
- Accent badges (uppercase, tight letter-spacing) for categories.

Layout & Grid
- Container width: 1280px max with 20px side padding.
- Use a 12-column grid for complex layouts; simple editorial pages can use a 2-column hero (2fr / 1fr) and a responsive single column on mobile.

Components
- Header: horizontal nav, strong logo block on the left, primary CTA on the right. Sticky at top.
- Race Ticker: full-width band, subtle border, condensed metadata and countdown.
- Hero: large image block with gradient overlay and bold H1.
- News Card: image (180–220px height), headline, category badge, subtle hover lift and accent border.
- Driver Card: compact card with large rank number, team color top border, and points emphasized.

Spacing & Rhythm
- Use 12–20px spacing within cards; 20–40px between major sections.
- Tight vertical rhythm for headlines and meta to resemble print editorials.

Accessibility
- Ensure contrast ratios meet AA for body text and large headings where possible.
- Provide descriptive alt attributes for images.
- Make interactive elements keyboard focusable and visible.

Suggested CSS Snippets
```
:root {
  --accent: #E10600;
  --bg: #15151E;
  --surface: #1F1F27;
  --muted: #949498;
  --max-width: 1280px;
  --gutter: 20px;
}

body { font-family: 'Titillium Web', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; background: var(--bg); color: #fff; }
.container { max-width: var(--max-width); margin: 0 auto; padding: 0 var(--gutter); }

.hero-grid { display: grid; grid-template-columns: 2fr 1fr; gap: 20px; }
.news-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }

.news-card { background: var(--surface); border-radius: 8px; overflow: hidden; transition: transform .18s ease, border-color .18s ease; }
.news-card:hover { transform: translateY(-4px); border-bottom-color: var(--accent); }

.f1-badge { background: var(--accent); color: #fff; padding: 4px 8px; border-radius: 4px; font-weight:700; font-size: .75rem; text-transform: uppercase; }
```

Example HTML (card)
```
<article class="news-card">
  <img src="..." alt="Descriptive alt" />
  <div class="news-card-body">
    <span class="f1-badge">Feature</span>
    <h3>Card headline that’s short and punchy</h3>
  </div>
</article>
```

Responsive Notes
- Collapse hero grid to a single column at <= 900px.
- Hide secondary nav or collapse into a burger menu on small screens.

Implementation Suggestions
- Keep CSS in a separate file (e.g., `style.css`) and import Google Fonts in the head.
- Use utility classes for spacing and badges to keep components composable.

Next Steps
- I can implement a standalone `style.css` with these variables and component styles, and wire it into `index.html` if you want.
