# ebook-publishing-skill

> Built by **[Artur Ferreira](https://github.com/arturseo-geo)** @ **The GEO Lab** · [𝕏 @TheGEO\_Lab](https://x.com/TheGEO_Lab) · [LinkedIn](https://linkedin.com/in/arturgeo) · [Reddit](https://www.reddit.com/user/Alternative_Teach_74/)

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![Licence](https://img.shields.io/badge/licence-MIT-green)
![Platforms](https://img.shields.io/badge/platforms-11-orange)
![Claude Code](https://img.shields.io/badge/Claude_Code-skill-blueviolet)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](https://github.com/arturseo-geo/ebook-publishing-skill/blob/main/CONTRIBUTING.md)

The most comprehensive ebook and audiobook self-publishing skill for Claude Code.
Covers the full lifecycle: write → format → convert → distribute → launch.

## What Makes This the "Ultimate" Skill

Most publishing skills cover one thing — EPUB conversion, or KDP setup, or cover specs.
This skill covers everything, including things no other skill addresses:

- ✅ HTML→PDF Puppeteer screenshot workflow (WeasyPrint/page.pdf() warnings included)
- ✅ Verified cover specs for 11 platform/format combinations with ratio and DPI
- ✅ AI audiobook production (ElevenLabs Studio, KDP Virtual Voice, distribution matrix)
- ✅ INaudio/Findaway Voices (rebranded August 2025) — wide audiobook distribution
- ✅ Google Play Books via PublishDrive
- ✅ ISBN strategy — the KDP free ISBN trap, buying your own, KDP+IngramSpark dual strategy
- ✅ IngramSpark 2026 update — upload fee removed, 1.875% Market Access Fee
- ✅ Permafree strategy and BookBub eligibility requirements
- ✅ Series pricing and read-through economics
- ✅ Gumroad MCP automation (`rmarescu/gumroad-mcp`)
- ✅ Python EPUB generation script (inspired by smerchek/claude-epub-skill, MIT)
- ✅ Full EPUB tool chain with Pandoc commands and epub-styles.css
- ✅ Platform MCP/API status for all platforms
- ✅ **Production-tested** — part of the [**The GEO Lab**](https://thegeolab.net) toolkit for AI-assisted content operations

## Platforms Covered

### Ebook Retailers
| Platform | API/MCP |
|---|---|
| Amazon KDP | ❌ Manual |
| Apple Books | ❌ Manual |
| Kobo Writing Life | ❌ Manual |
| Barnes & Noble Press | ❌ Manual |
| Google Play Books | ❌ Manual (via PublishDrive) |
| Gumroad | ✅ `rmarescu/gumroad-mcp` |
| Payhip | ❌ Manual |

### Aggregators
| Platform | Reaches |
|---|---|
| Draft2Digital | Amazon, Apple, Kobo, B&N, Scribd, Tolino, libraries |
| PublishDrive | 400+ stores, 240k libraries, Google Play, international |
| StreetLib | Europe, Latin America, Middle East, Africa |

### Print-on-Demand
| Platform | Best for |
|---|---|
| KDP Print | Amazon marketplace |
| IngramSpark | Bookstores, libraries, hardcovers |
| Bookvault | UK/Europe print |

### Audiobook Distribution
| Platform | Notes |
|---|---|
| ACX | Amazon/Audible — human narration preferred |
| INaudio (formerly Findaway Voices) | Wide — Spotify, Apple, Google, 30+ platforms |
| PublishDrive Audio | 50 distribution partners |
| KDP Virtual Voice | Amazon AI narration (US beta) |
| ElevenLabs | Production tool + ElevenReader distribution |

## Install

### Via Claude Code plugin marketplace
```bash
/plugin marketplace add YOUR_GITHUB_USERNAME/ebook-publishing-skill
/plugin install ebook-publishing@ebook-publishing-skill
```

### Manual install
```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/ebook-publishing-skill.git ~/.claude/skills/ebook-publishing
```

### Via skills CLI
```bash
npx skills add YOUR_GITHUB_USERNAME/ebook-publishing-skill
```

## File Structure

```
ebook-publishing/
├── SKILL.md                        # Main skill — always loaded (~100 tokens)
├── project-context.md              # Your brand + publishing setup (edit this)
└── references/
    ├── platforms.md                # All platforms, royalties, API status (2026)
    ├── cover-specs.md              # Verified cover dimensions for 11 platforms
    ├── formatting.md               # EPUB tool chain, HTML→PDF, Pandoc, Python script
    ├── audiobooks.md               # ACX, ElevenLabs, KDP VV, INaudio, distribution matrix
    ├── isbn-strategy.md            # ISBN buying guide, KDP trap, KDP+IS dual strategy
    └── promotion.md                # BookBub, permafree, series, ARC, launch playbook
```

## Contributing

Platform specs change constantly — royalties shift, fees change, new platforms emerge.
PRs with sourced updates are always welcome.

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.
Use the issue templates for:
- [Platform spec updates](https://github.com/arturseo-geo/ebook-publishing-skill/issues/new?template=platform-update.md)
- [Bug reports](https://github.com/arturseo-geo/ebook-publishing-skill/issues/new?template=bug-report.md)
- [New platform requests](https://github.com/arturseo-geo/ebook-publishing-skill/issues/new?template=new-platform.md)

---

## Attributions & Licence

Built and maintained by **[Artur Ferreira](https://github.com/arturseo-geo)** · Part of the **[The GEO Lab](https://thegeolab.net)** toolkit.

---

### Best Practice Attribution

This skill was built following the open source Best Practice Approach —
reading community work for inspiration, then writing original content,
and crediting every source.

**Based on:**
- [Agent Skills specification](https://github.com/anthropics/skills) by Anthropic (Apache 2.0)

**Inspired by community repos researched during development:**
- [`smerchek/claude-epub-skill`](https://github.com/smerchek/claude-epub-skill) — Markdown→EPUB3 conversion with Python (MIT) — Python script pattern in `references/formatting.md`
- [`coreyhaines31/marketingskills`](https://github.com/coreyhaines31/marketingskills) — marketing skill patterns (MIT)
- [`alirezarezvani/claude-skills`](https://github.com/alirezarezvani/claude-skills) — skill structure conventions (MIT)
- [`ThomasHoussin/Claude-Book`](https://github.com/ThomasHoussin/Claude-Book) — multi-agent fiction writing with EPUB/MOBI build

**Platform data compiled from official documentation:**
- Amazon KDP, Apple Books, Kobo Writing Life, Gumroad, Payhip, Draft2Digital, B&N Press, IngramSpark, Google Play Books, PublishDrive, StreetLib
- Audiobook sources: ElevenLabs, INaudio (formerly Findaway Voices), ACX, KDP Virtual Voice
- Industry sources: Reedsy, ALLi (Alliance of Independent Authors), IngramSpark Blog, selfpublishing.com

All skill content is original writing. No files were copied or adapted from any source. MIT licence.

---

Found this useful? ⭐ Star the repo and connect:
[🌐 thegeolab.net](https://thegeolab.net) · [𝕏 @TheGEO_Lab](https://x.com/TheGEO_Lab) · [LinkedIn](https://linkedin.com/in/arturgeo) · [Reddit](https://www.reddit.com/user/Alternative_Teach_74/)

## Changelog

### v2.0.0 (March 2026) — The Ultimate Edition
**Added:**
- Complete audiobook reference — ElevenLabs Studio workflow, KDP Virtual Voice (US beta), INaudio/Findaway Voices (rebranded Aug 2025), AI narration distribution matrix
- ISBN strategy reference — the KDP free ISBN trap, buy your own (Bowker/Nielsen), KDP+IngramSpark dual publish strategy
- Promotion & launch reference — permafree mechanics, BookBub eligibility, series read-through economics, ARC strategy, email list building from back matter
- Google Play Books, PublishDrive (400+ stores), StreetLib platforms
- IngramSpark 2026 update — upload fee removed, 1.875% Market Access Fee
- Python EPUB generation script (inspired by `smerchek/claude-epub-skill`, MIT)
- EPUB CSS template (`epub-styles.css`)
- Kindle Unlimited KENPC mechanics

**Updated:**
- Cover specs expanded to 11 platform/format combinations
- Platforms reference restructured with aggregators and POD as separate sections
- Royalty calculator updated for all platforms

### v1.1.0 (March 2026)
- Added HTML→PDF Puppeteer screenshot workflow (6-step, with WeasyPrint/page.pdf() warnings)
- Updated cover specs to 9 platforms with ratio and DPI columns
- Added Gumroad MCP documentation (`rmarescu/gumroad-mcp`)
- Added platform API/MCP status table for all platforms
- Added DPI requirements table by output type
- Added interactive elements strategy for designed ebooks

### v1.0.0 (March 2026) — Initial release
Core skill built from scratch following the Agent Skills specification.
Covers: book structure, EPUB formatting, cover design, metadata, pricing, launch strategy.
Platforms: Amazon KDP, Apple Books, Gumroad, Payhip, Draft2Digital, Kobo, B&N Press, IngramSpark.

## Licence

MIT — see LICENSE

---

Built and maintained by **[Artur Ferreira](https://github.com/arturseo-geo)** · Part of the **[The GEO Lab](https://thegeolab.net)** toolkit · [MIT License](LICENSE)
