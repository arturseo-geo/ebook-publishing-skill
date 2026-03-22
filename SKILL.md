---
name: ebook-publishing
description: >
  The complete ebook and audiobook self-publishing skill — write, format,
  convert, and publish across all major platforms. Use this skill whenever
  the user asks about Amazon KDP, Apple Books, Gumroad, Payhip, Kobo,
  Draft2Digital, IngramSpark, Barnes & Noble Press, Google Play Books,
  PublishDrive, StreetLib, ACX, ElevenLabs audiobooks, KDP Virtual Voice,
  INaudio (formerly Findaway Voices), EPUB formatting, HTML-to-PDF Puppeteer
  workflow, book cover design specs, ISBN strategy, KDP Select vs wide
  distribution, permafree strategy, BookBub, series pricing, royalty
  calculations, book descriptions, Amazon A+ content, keyword research,
  ARC readers, or any launch strategy. Also trigger for lead magnet ebooks,
  digital downloads, online courses packaged as ebooks, audiobook production
  with AI narration, print-on-demand, or any content intended for digital
  or print distribution and sale. MCP available for Gumroad only
  (rmarescu/gumroad-mcp). All other platforms require manual upload.
---

# Ultimate Ebook Publishing Skill

Covers the complete lifecycle: write → format → convert → publish → distribute → launch.
Includes ebooks, print-on-demand, and AI-narrated audiobooks.

## Reference Files — Load When Relevant

| Topic | File | Load when... |
|---|---|---|
| All platforms + royalties | `references/platforms.md` | Choosing where to publish, royalty questions |
| Cover design specs | `references/cover-specs.md` | Designing or sizing covers for any platform |
| Formatting + conversion | `references/formatting.md` | EPUB, PDF, HTML→PDF, Pandoc, Puppeteer |
| Audiobooks | `references/audiobooks.md` | ACX, ElevenLabs, KDP Virtual Voice, INaudio |
| ISBN strategy | `references/isbn-strategy.md` | Buying ISBNs, KDP trap, dual KDP+IS strategy |
| Promotion + launch | `references/promotion.md` | BookBub, permafree, series, ARC, launch plan |

---

## Project Context

If `project-context.md` exists in the skill directory or `.claude/` folder, read it
before any task. It contains brand voice, publishing setup, platform credentials
paths, and infrastructure details — avoids re-explaining context each session.

---

## Workflow Overview

```
1. Write & Structure
2. Format (EPUB / PDF / HTML→PDF)
3. Cover Design
4. ISBN Decision
5. Platform Strategy (wide vs exclusive, ebook + print + audio)
6. Metadata & SEO
7. Pricing & Royalties
8. Pre-launch + Launch + Post-launch
```

---

## EPUBCheck Compliance (EPUB 3.0)

EPUBs must pass EPUBCheck for D2D, Apple Books, Kobo, and most aggregators. Common errors and fixes:

| Error | Fix |
|---|---|
| `<script>` tags | Remove all — EPUB content docs don't allow JavaScript |
| `<button>` tags | Remove all |
| `<input>`, `<select>`, `<textarea>`, `<form>` | Remove all form elements |
| Event handlers (`onclick`, `onmouseover`, etc.) | Remove all `on*` attributes |
| Orphan `<dt>`/`<dd>` outside `<dl>` | Convert to styled `<p>` tags (see below) |
| CSS unbalanced braces | Remove `@media` blocks (limited EPUB reader support), validate brace count |
| Broken fragment identifiers (`href="#id"` where id missing) | Convert `<a>` to `<span>`, remove `href` |
| OPF-014 "scripted" property | Caused by script tags — removing scripts fixes it |

**Critical dt/dd fix:** Do NOT wrap orphan `<dt>`/`<dd>` in `<dl>` — the source HTML often has them as siblings in a `<div>`, and grouping consecutive ones can create `<dl>` with only `<dt>` (missing required `<dd>`), which also fails EPUBCheck. Instead:
- Convert orphan `<dt>` → `<p style="font-weight:700;margin-bottom:0.2em">`
- Convert orphan `<dd>` → `<p style="margin-left:1em;margin-top:0">`

---

## Step 1: Book Structure

### Non-Fiction
```
Front Matter:
  Title page · Copyright · Dedication (opt) · TOC · Foreword (opt)
Body:
  Introduction (promise) → Chapters (Hook → Concepts → Examples → Takeaways)
Back Matter:
  Conclusion/Next Steps · About the Author · Also by · Resources · Index (tech books)
```

### Fiction
```
Front matter: Title · Copyright · Dedication · TOC (optional)
Act structure: Three-act / Hero's Journey / Save the Cat
Back matter: Acknowledgements · About the Author · Also by · Newsletter CTA
```

### Lead Magnet / Short Ebook (10–50 pages)
Title + promise → Problem → 3–7 steps → Quick wins → CTA (email, product, service)

---

## Step 2: Format & DPI Requirements

| Output type | DPI | Notes |
|---|---|---|
| EPUB (digital reading) | 72–150 | Higher = larger file, no screen benefit |
| PDF (digital download) | 150 | Sharp on retina, reasonable file size |
| PDF (print-ready) | 300 | Required for KDP Print, IngramSpark |
| All covers | 300 | Always 300 — displayed at many sizes |

**File formats quick reference:**

| Platform | Accepted | Preferred |
|---|---|---|
| Amazon KDP | EPUB, DOCX, HTML, MOBI | EPUB 3 |
| Apple Books | EPUB only | EPUB 3 (strict validation) |
| Gumroad / Payhip | Any file | PDF for designed ebooks |
| Draft2Digital | DOCX, EPUB | EPUB 3 |
| Kobo / B&N Press | EPUB, PDF | EPUB 3 |
| IngramSpark | EPUB (digital), PDF (print) | EPUB 3 |
| Google Play Books | EPUB, PDF | EPUB 3 |
| PublishDrive | EPUB | EPUB 3 |

See `references/formatting.md` for full EPUB tool chain, HTML→PDF Puppeteer workflow,
and Pandoc conversion commands.

---

## Step 3: Cover Design

**Universal shortcut**: design at **2560 × 1600 px, 300 DPI** — covers all platforms.

See `references/cover-specs.md` for verified specs across all 9 platforms.

Quick reference:

| Platform | Dimensions | Ratio | DPI |
|---|---|---|---|
| Amazon KDP ebook | 1600 × 2560 | 5:8 | 72 min |
| Amazon KDP paperback | KDP template | varies | 300 |
| Apple Books | 1400 × 2100 | 2:3 | 150+ |
| Kobo / D2D | 1600 × 2400 | 2:3 | 150+ |
| Gumroad product | 1280 × 1920 | 2:3 | 150+ |
| Gumroad thumbnail | 900 × 900 | 1:1 | 150+ |
| Payhip | 2560 × 1600 | 8:5 | 300 |
| B&N Press | 2000 × 3000 | 2:3 | 300 |
| Google Play Books | 1600 × 2400 | 2:3 | 300 |

---

## Step 4: ISBN Decision

See `references/isbn-strategy.md` for the full guide. Quick rules:

- **Never use KDP's free ISBN** if you plan to publish elsewhere — it locks you to Amazon
- **Buy your own**: Bowker (US) · Nielsen (UK) · Library and Archives Canada · other national agencies
- **Each format needs its own ISBN**: ebook ≠ paperback ≠ hardcover ≠ audiobook
- **Best strategy**: own ISBNs → publish KDP first (disable Expanded Distribution) → then IngramSpark

---

## Step 5: Platform Strategy

### Decision Tree

```
Fiction writer? → Consider KDP Select (Kindle Unlimited) for 90-day windows
Non-fiction / established author? → Go Wide from day one
Want bookstore + library distribution? → KDP Print + IngramSpark (same ISBN)
Want maximum direct revenue? → Gumroad/Payhip for PDF, D2D for wide ebook
Want audiobook? → See references/audiobooks.md
Want Google Play? → Via PublishDrive ($9.99/mo) or direct (complex approval)
EU audience? → Payhip handles VAT automatically
International markets? → PublishDrive (400+ stores, 240k libraries) or StreetLib
```

### MCP Automation Status

| Platform | MCP | Notes |
|---|---|---|
| Gumroad | ✅ `rmarescu/gumroad-mcp` | Create/update products, upload files |
| All others | ❌ | Manual upload required |

---

## Step 6: Metadata & SEO

### Book Description (Amazon / Apple / Kobo / Google Play)
1. **Hook** (1–2 sentences): who this is for + what they'll get
2. **Problem** (2–3 sentences): the pain without this book
3. **Solution teaser** (5–7 bullets)
4. **Social proof** (if available)
5. **CTA**: "Download your copy today" / "Get your copy now"

Amazon supports HTML in descriptions:
```html
<h2>Are you struggling with X?</h2>
<p>Most people who want Y fail because Z...</p>
<ul><li>✓ How to...</li><li>✓ The secret to...</li></ul>
<p><b>Scroll up and click Buy Now</b></p>
```

### Amazon Keywords (7 fields, 50 chars each)
- Long-tail phrases only — not single words
- Include: use cases, audience type, difficulty level
- Never repeat words from title/subtitle
- Research: Publisher Rocket, Amazon autocomplete, "Customers also bought"

### Categories (Amazon)
- 2 during upload; request up to 10 via Author Central support
- Strategy: one broad + one narrow lower-competition niche
- Browse category bestseller lists first

---

## Step 7: Pricing & Royalties

### Amazon KDP Ebook
| Price | Royalty | Notes |
|---|---|---|
| $0.99–$2.98 | 35% | Loss leader / entry point |
| $2.99–$9.99 | 70% | Sweet spot — use this |
| $10.00+ | 35% | Drops back |

### Pricing Strategy by Format
| Format | Typical Range | Notes |
|---|---|---|
| Lead magnet | Free – $0.99 | List building |
| Standard non-fiction | $2.99–$4.99 | Volume + visibility |
| Comprehensive guide | $7.99–$9.99 | Max 70% royalty tier |
| Premium PDF (Gumroad) | $9.99–$29.99 | Direct = higher margin |
| Paperback (KDP Print) | $9.99–$17.99 | Check print cost first |
| Audiobook (ACX) | $14.99–$24.99 | ACX suggests based on length |

### Series Pricing
- Book 1: permafree or $0.99 (loss leader — drives series read-through)
- Books 2+: full price ($3.99–$5.99)
- Calculate read-through value: if 30% of Book 1 readers buy Book 2 at $4.99, each Book 1 reader is worth $1.50

See `references/promotion.md` for permafree mechanics and BookBub strategy.

---

## Step 8: Launch

See `references/promotion.md` for the full launch playbook.

### Quick Checklist
**Pre-launch (4–6 weeks):**
- [ ] Email list with early access offer
- [ ] 10–20 ARC readers lined up for reviews at launch
- [ ] Amazon Author Central page set up
- [ ] Social content scheduled (cover reveal, excerpts, testimonials)

**Launch week:**
- [ ] 3-email sequence: announcement → reminder → last chance
- [ ] KDP promotion (Countdown Deal or Free Days if KDP Select)
- [ ] Submit to BookBub, Freebooksy, BargainBooksy
- [ ] Outreach to podcast / newsletter partners

**Post-launch:**
- [ ] Request reviews via email (never inside the book — Amazon TOS)
- [ ] A/B test cover and description
- [ ] Annual content refresh
- [ ] Expand formats: audio, print, translations
