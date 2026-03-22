# Cover Design Specs — Verified All Platforms (March 2026)

## Universal Shortcut
Design at **2560 × 1600 px, 300 DPI** → crop/export per platform.
One master file covers everything except the KDP paperback (needs template).

---

## Verified Specs

| Platform | Dimensions (px) | Ratio | DPI | Format | Notes |
|---|---|---|---|---|---|
| Amazon KDP ebook | 1600 × 2560 | 5:8 | 72 min | JPG/TIFF | sRGB; max 50MB |
| Amazon KDP paperback | KDP template | varies | 300 | PDF | Download from KDP — depends on trim + page count |
| Apple Books | 1400 × 2100 | 2:3 | 150+ | JPG/PNG | Must match interior trim |
| Kobo Writing Life | 1600 × 2400 | 2:3 | 150+ | JPG/PNG | |
| D2D / Writing Life | 1600 × 2400 | 2:3 | 150+ | JPG/PNG | Same as Kobo |
| Google Play Books | 1600 × 2400 | 2:3 | 300 | JPG/PNG | |
| Gumroad product image | 1280 × 1920 | 2:3 | 150+ | JPG/PNG | Main product page image |
| Gumroad thumbnail | 900 × 900 | 1:1 | 150+ | JPG/PNG | Search/marketplace display |
| Payhip | 2560 × 1600 | 8:5 | 300 | JPG/PNG | **Landscape** — unique orientation |
| B&N Press | 2000 × 3000 | 2:3 | 300 | JPG/PNG | Strictest digital platform |
| IngramSpark (digital) | 1600 × 2400 | 2:3 | 300 | JPG/PNG | |
| IngramSpark (print) | KDP-style template | varies | 300 | PDF | Download from IS — front+spine+back |
| PublishDrive | 1600 × 2400 | 2:3 | 300 | JPG/PNG | |

---

## Platform-Specific Notes

### Amazon KDP ebook
- Minimum: 1000 × 625 px (never use this — quality is poor)
- Recommended: 1600 × 2560 px or higher (2400 × 3840 also accepted)
- Colour: sRGB — never CMYK for digital
- File size: under 50MB

### Amazon KDP paperback
- **Download the exact template from KDP** — spine width depends on page count
- Template covers: front cover + spine + back cover
- Spine text safe only if > 130 pages
- Submit as print-ready PDF with all fonts embedded
- Bleed: 0.125" on all sides

### Apple Books
- Cover embedded in EPUB: referenced in OPF manifest as `<item properties="cover-image">`
- Fixed layout EPF format for children's/illustrated books

### Gumroad — Two Images Required
- **Product image** (1280 × 1920): main product page visual
- **Thumbnail** (900 × 900): marketplace search results
- With `rmarescu/gumroad-mcp`: Claude can upload both automatically

### Payhip — Landscape Orientation
- Only platform using landscape (wider than tall)
- Standard portrait cover will not fill frame correctly
- Best approach: mockup scene (ebook on desk/device) or split layout (cover right, title/tagline left)

### IngramSpark print cover
- Includes front, spine, back as one PDF
- Back cover: ISBN barcode + description + author photo (optional)
- Spine: text only safe if > 130 pages; IS calculates spine width

---

## Verified Working Sizes (March 2026)

From real publishing session — these sizes were accepted:
- **Gumroad**: 816×1302px accepted (below recommended 1280×1920, but works)
- **Payhip**: 2560×1600px LANDSCAPE required (unique orientation)
- **KDP**: 1600×2560px minimum — upscaled from 816×1302 using AI upscaler
- **D2D**: 1600×2400px minimum — EPUBCheck validates cover dimensions

**Upscaling tip:** If original covers are too small, use AI upscalers (Topaz Gigapixel, upscale.media, etc.) to reach platform minimums. Quality is acceptable for digital distribution.

---

## Export Checklist

Before uploading any cover:
- [ ] Colour mode: sRGB (never CMYK for digital)
- [ ] File size: under 50MB (covers typically 2–8MB)
- [ ] Thumbnail test: shrink to 60×90px — is title still readable?
- [ ] No text within 0.25" of edges (safety zone for bleed)
- [ ] Contrast: check on both white and black backgrounds
- [ ] Font licences: commercial use confirmed

## Design Principles

- **Thumbnail rule**: design for the 60×90px thumbnail first, then scale up
- **Genre signals**: cover should feel at home in your exact category's top 10
- **1–2 fonts max**: one display font for title, one for author name
- **Author name**: smaller than title unless you are the brand
- **Colour psychology**: follow your genre's conventions, not personal preference
- **High contrast**: dark text on light, or light on dark — never mid-tones on mid-tones
- **Series consistency**: same font treatment, colour palette, layout style across all books
