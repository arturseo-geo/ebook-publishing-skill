# Platform Reference — Complete Guide (Updated March 2026)

## MCP & API Status

| Platform | MCP | API | Notes |
|---|---|---|---|
| Gumroad | ✅ `rmarescu/gumroad-mcp` | Partial | Full product + file management |
| All others | ❌ | ❌ | Manual upload only |

---

## EBOOK PLATFORMS

### Amazon KDP
**URL**: kdp.amazon.com | **Market share**: ~80% of US ebook sales
**Royalties**: 35% ($0.99–$2.98 and $10+) | 70% ($2.99–$9.99)
**Delivery fee**: $0.15/MB deducted from 70% royalties
**Payment**: Monthly, 60-day delay | Min: $100 wire / $10 direct deposit
**Formats**: EPUB (preferred), DOCX, HTML, KPF
**Programs**:
- **KDP Select** (90-day exclusive): Kindle Unlimited page reads (KENPC rate ~$0.004–$0.005/page), Countdown Deals, Free Days
- **Author Central**: Bio, photos, claimed titles, A+ content
- **Virtual Voice**: AI audiobook narration beta (US only) — see `audiobooks.md`
- **Expanded Distribution**: Distributes print to other retailers via Ingram — **disable this** if using IngramSpark directly

**ISBN note**: KDP's free ISBN is locked to Amazon — cannot be used elsewhere. Always bring your own if publishing wide. See `isbn-strategy.md`.

**Verified gotchas (March 2026):**
- Cannot list at $0.00 directly — minimum price is $0.99 (35% royalty)
- **Permafree workaround**: list at $0.99, then report lower price from other stores (Gumroad/Payhip at $0) — Amazon price-matches to free
- DRM: select "No" for maximum distribution
- KDP Select: say "No" if publishing on other platforms (D2D, Kobo, Apple)
- Accessibility: select "This book does not contain images that are necessary for understanding the content" for text-based guides
- Review time: up to 72 hours after submission
- No daily upload limit
- Cover minimum: 1600×2560px (5:8 ratio)

---

### Apple Books
**URL**: authors.apple.com / Books Connect
**Royalties**: 70% on all prices, no delivery fee
**Payment**: Monthly, 45-day delay
**Formats**: EPUB 3 only — EPUBCheck validation is strict
**Notes**: Fixed layout EPF for children's/picture books. Apple provides one free ISBN for some territories.

---

### Kobo Writing Life
**URL**: kobo.com/us/en/writing-life
**Best for**: Canada, UK, Australia, Japan, Netherlands
**Royalties**: 70% ($1.99–$12.99) | 45% (others)
**Payment**: Monthly, 45-day delay
**Formats**: EPUB, PDF
**Features**: Kobo Plus subscription participation, promotional tools, digital narration (invite-only AI audio)

---

### Barnes & Noble Press
**URL**: press.barnesandnoble.com
**Best for**: US Nook readers, B&N marketplace
**Royalties**: 65% ($2.99–$9.99) | 40% (others)
**Payment**: Monthly
**Formats**: EPUB

---

### Google Play Books
**URL**: play.google.com/books/publish
**Best for**: Android users globally, chart algorithm advantages (free downloads count toward charts)
**Royalties**: 70% (publisher keeps 52% after Google's share)
**Access**: Direct account approval is slow/difficult — use PublishDrive as the reliable route
**Formats**: EPUB, PDF
**Advantage**: Free downloads count toward ranking charts — strong for permafree Book 1 in a series

---

### Gumroad
**URL**: gumroad.com | **MCP**: `rmarescu/gumroad-mcp` ✅
**Fees**: 10% + 2.9% + $0.30 payment processing
**Payment**: Weekly (Friday), min $10
**Formats**: Any (PDF, EPUB, ZIP, video, etc.)
**Features**: Memberships, bundles, discount codes, affiliates, workflow emails, pay-what-you-want
**Best for**: Designed PDF ebooks, lead magnets, premium bundles, direct audience sales

**Verified gotchas (March 2026):**
- Description format: plain text only (no HTML accepted)
- Custom domain: may verify successfully but `/l/slug` product URLs can 404 — known routing bug
- Workaround: use `thegeolab.gumroad.com/l/slug` links instead of custom domain
- Fix attempt: remove and re-add custom domain (may get "already in use" error — contact Gumroad support)
- Gumroad Discover: requires at least 1 successful sale + Risk Review — won't work for free ($0+) products
- MCP limitations: rmarescu/gumroad-mcp can read products, manage offer codes, enable/disable — but CANNOT create or update products
- Cover: 816×1302px works but 1280×1920px recommended

---

### Payhip
**URL**: payhip.com
**Fees**: 5% (free) | 2% ($29/mo Plus) | 0% ($99/mo Pro)
**Payment**: Instant via PayPal/Stripe
**Formats**: Any
**Features**: Coupons, affiliates, upsells, EU VAT auto-collection, PDF stamping
**Cover**: Landscape orientation (2560×1600) — unique, requires separate design

**Verified gotchas (March 2026):**
- Description format: PLAIN TEXT only (no HTML)
- Description limit: 50–4,000 characters
- Description rules: no email addresses, no hyperlinks, no prices, no promotions
- Category: no dedicated "E-Books" category — check dropdown for closest match
- Has blog post feature for content marketing

---

---

## AGGREGATORS (Distribute to Multiple Platforms)

### Draft2Digital (D2D)
**URL**: draft2digital.com
**Fee**: 10% of list price
**Distributes to**: Apple Books, Kobo, B&N, Scribd, Tolino, Vivlio, OverDrive, Smashwords, cloudLibrary, Hoopla, Fable, Gardners, Bookshop.org, BorrowBox, libraries
**Formats**: DOCX (D2D formats it), EPUB
**Features**: Universal Book Links, free ISBN, auto back-matter (Also by list)
**Note**: Cannot distribute to Amazon if enrolled in KDP Select
**Best for**: Going wide without managing separate accounts (except Google Play)

**Verified gotchas (March 2026):**
- Daily submission limit: 3 new titles per 24 hours — creating additional accounts to bypass = account termination
- Description limit: 50–4,000 characters
- Description rules: no email addresses, no hyperlinks, no prices, no promotions
- EPUBCheck validation required: must pass EPUB 3.0
- Free ISBN available (D2D-assigned)
- Rights confirmation required: "I am the original creator of this content"
- Print book option available but optional (D2D Print)
- Cover minimum: 1600×2400px
- Categories use BISAC codes (e.g., BUSINESS & ECONOMICS / Marketing / Search Engine Optimization)
- No dedicated Kobo account needed — D2D distributes there

### PublishDrive
**URL**: publishdrive.com
**Fee**: Flat $9.99/month (keep 100% royalties) — free for first book (limited features)
**Distributes to**: 400+ stores, 240,000+ libraries globally — **the only aggregator with Google Play access**
**Formats**: EPUB
**Features**: Built-in marketing tools, in-store promotions, detailed analytics, royalty management
**International**: Strong in Eastern Europe, China (DangDang), India, Middle East
**Unique identifier**: Uses its own ID (not ISBN) but globally accepted in stores
**Best for**: Authors prioritising Google Play, international markets, high-volume sellers

### StreetLib
**URL**: streetlib.com
**Fee**: Takes a percentage (higher than D2D/PublishDrive)
**Best for**: Europe and Latin America, Middle East, South Asia, Africa
**Features**: Author portals in multiple languages, regional distribution partners
**Best for**: International-focused authors who need non-English market penetration

---

## PRINT-ON-DEMAND

### KDP Print (formerly CreateSpace)
**URL**: kdp.amazon.com
**Fee**: Per-copy print cost deducted from royalties
**Royalties**: ~60% (list price minus print cost) for Amazon sales | 40% for Expanded Distribution
**Formats**: PDF (interior + cover)
**Best for**: Amazon marketplace, fast setup
**Tip**: Disable "Expanded Distribution" if using IngramSpark — they use Ingram too and it creates conflicts

### IngramSpark
**URL**: ingramspark.com
**Fee**: **Upload fee removed as of February 2026** — now charges 1.875% Market Access Fee on sales
**Royalties**: Varies — approximately 45-55% after print cost for direct sales
**Distributes to**: 40,000+ retailers and libraries globally (the Ingram catalog)
**Formats**: PDF (interior + cover), EPUB (digital distribution)
**ISBN**: Required — buy your own (IngramSpark's free ISBN lists "Indie Pub" as imprint)
**Best for**: Bookstore/library distribution, hardcovers with dust jackets, international print
**KDP+IS dual strategy**: See `isbn-strategy.md` — use both for maximum reach

### Bookvault
**URL**: bookvault.app
**Best for**: UK-based authors, European print distribution, hardcovers
**Integrates with**: D2D, other aggregators

---

## PLATFORM SELECTION GUIDE

| Goal | Recommended |
|---|---|
| Maximum ebook reach | KDP + D2D (wide) |
| Maximum direct revenue | Gumroad + Payhip |
| Kindle Unlimited readers | KDP Select (exclusive, 90-day) |
| Google Play access | PublishDrive |
| EU audience / VAT handled | Payhip |
| Print + bookstores + libraries | KDP Print + IngramSpark |
| International (non-Western markets) | PublishDrive + StreetLib |
| Lead magnet / permafree | Gumroad (PWYW) or wide at $0.00 via D2D |
| Library distribution | IngramSpark or D2D |
| Audiobook wide | INaudio (Spotify network) or PublishDrive |
| MCP automation | Gumroad only |
| BookBub eligibility | Must be wide (not KDP Select exclusive) |

---

## ROYALTY CALCULATOR — $4.99 Ebook

| Platform | Author Earns | Notes |
|---|---|---|
| Amazon KDP (70%) | ~$3.15 | After ~$0.34 delivery fee |
| Apple Books (70%) | $3.49 | No delivery fee |
| Kobo (70%) | $3.49 | |
| Google Play (70%) | ~$3.49 | Via PublishDrive: minus their fee |
| Gumroad (90%) | ~$4.05 | After 10% + payment processing |
| Payhip (95%) | ~$4.44 | After 5% + payment processing |
| D2D (90%) | ~$4.49 | D2D's share — retailer may take more |
| PublishDrive | ~$4.99 | You keep 100%; pay flat monthly fee |
