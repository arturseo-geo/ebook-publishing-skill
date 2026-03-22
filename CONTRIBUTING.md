# Contributing to ebook-publishing-skill

Thanks for helping keep this skill accurate and useful. Platform specs, royalty rates,
and distribution policies change constantly — community contributions are what keep
this the most up-to-date publishing skill available.

## What We Welcome

### ✅ High-value contributions
- **Platform spec updates** — royalty rate changes, new file format requirements, fee changes, cover dimension updates
- **New platforms** — emerging self-publishing or distribution platforms worth adding
- **Audiobook updates** — AI narration policies, new distribution partners, platform acceptance changes
- **Bug fixes** — incorrect commands, broken workflows, outdated instructions
- **New reference sections** — well-researched additions to any reference file

### ❌ What we don't accept
- Unverified data (guesses, approximations without sources)
- Promotional content for specific services
- Changes to `project-context.md` (that's brand-specific to The GeoLab)
- Breaking changes to the SKILL.md frontmatter format without discussion first

---

## How to Contribute

### 1. Check existing issues first
Someone may already be tracking the change you spotted.
→ [Open Issues](https://github.com/arturseo-geo/ebook-publishing-skill/issues)

### 2. Fork and create a branch
```bash
git clone https://github.com/YOUR_USERNAME/ebook-publishing-skill.git
cd ebook-publishing-skill
git checkout -b update/kdp-royalty-rates-2026
```

### 3. Make your changes
- Keep edits focused — one topic per PR
- Always include your source (official platform docs, not blog posts)
- Update the date reference in the file if the data changed (e.g. `Updated March 2026` → `Updated June 2026`)
- Add an entry to the relevant section in `README.md` changelog if it's a significant change

### 4. Submit a Pull Request
Use the PR template — it asks for source links and a brief explanation.
We review all PRs within 7 days.

---

## File Guide

| File | What it contains | How often it changes |
|---|---|---|
| `SKILL.md` | Main skill — workflow overview, quick refs | Rarely |
| `references/platforms.md` | Royalties, fees, API status | Frequently |
| `references/cover-specs.md` | Cover dimensions per platform | Occasionally |
| `references/formatting.md` | EPUB/PDF conversion workflows | Rarely |
| `references/audiobooks.md` | AI narration, distribution matrix | Frequently (fast-moving space) |
| `references/isbn-strategy.md` | ISBN buying, dual strategy | Rarely |
| `references/promotion.md` | BookBub, permafree, launch | Occasionally |

**Most common update target**: `references/platforms.md` and `references/audiobooks.md` —
platform policies and AI narration acceptance change regularly.

---

## Versioning

We follow [Semantic Versioning](https://semver.org/):
- **Patch** (2.0.x): Data corrections, typo fixes, small clarifications
- **Minor** (2.x.0): New platforms, new reference sections, new workflows
- **Major** (x.0.0): Structural changes to SKILL.md, breaking changes to file layout

---

## Code of Conduct

Be accurate, be useful, cite your sources. That's it.

---

## Questions?

Open a [Discussion](https://github.com/arturseo-geo/ebook-publishing-skill/discussions)
or reach out via [𝕏 @TheGEO_Lab](https://x.com/TheGEO_Lab).
