# ISBN Strategy Reference

## What Is an ISBN?
An International Standard Book Number (ISBN) is a unique 13-digit identifier
for a specific edition and format of a book. Each format requires its own ISBN:
ebook ≠ paperback ≠ hardcover ≠ audiobook — they are separate products.

---

## The KDP Free ISBN Trap

Amazon KDP offers a free ISBN. **Do not use it if you plan to publish elsewhere.**

From Amazon's own terms: *"This free ISBN can only be used on KDP for distribution
to Amazon and its distribution partners. It cannot be used with another publisher
or self-publishing service."*

**Consequences of using KDP's free ISBN:**
- Cannot upload the same book to IngramSpark (ISBN already in Ingram's system as Amazon's)
- IngramSpark will reject the upload
- You are locked to Amazon's distribution network
- The "publisher" listed in metadata will be Amazon, not your imprint

**When KDP's free ISBN is acceptable:** if you are intentionally Amazon-only and have no plans to go wide or sell to bookstores/libraries.

---

## Buy Your Own ISBN

### By Country
| Country | Agency | Cost |
|---|---|---|
| United States | Bowker (myidentifiers.com) | $125 single / $295 for 10 / $575 for 100 |
| United Kingdom | Nielsen (isbn.nielsenbook.co.uk) | £89 single / £164 for 10 |
| Canada | Library and Archives Canada | Free (one per title, form required) |
| Australia | Thorpe-Bowker | AU$44 single |
| New Zealand | National Library | Free |
| Most others | National ISBN agency | Varies |

**Bulk buying**: If you plan to publish multiple books or multiple formats, buy 10 at once — the per-ISBN cost drops dramatically (Bowker: from $125 to $29.50 each for 10).

### What Owning Your ISBN Means
- The "publisher" field in all retailer metadata shows your imprint name (e.g., "Dark Mountain Press")
- You retain full control — can move the book between platforms
- Professional appearance to bookstore buyers who see Ingram catalog listings
- Required for IngramSpark if you want your own imprint shown

---

## Per-Format ISBN Assignment

| Format | Needs own ISBN? | Notes |
|---|---|---|
| Ebook (EPUB/MOBI) | Yes | Different from print |
| Paperback | Yes | Different from hardcover |
| Hardcover | Yes | Different from paperback |
| Audiobook | Yes | Each platform may want its own |
| Large print | Yes | Separate edition |
| Translation | Yes | Each language is a separate product |

---

## KDP + IngramSpark Dual Strategy

The recommended approach for maximum reach: **use both platforms with your own ISBN.**

### Why Both?
- **KDP**: sells to Amazon customers (80% of ebook market); cheapest print cost for Amazon orders; easy dashboard
- **IngramSpark**: lists in Ingram catalog → 40,000+ bookstores and libraries can order your book; better quality hardcovers; better international print distribution

### Step-by-Step: Publish to Both

**Step 1: Buy your own ISBN** (Bowker/Nielsen)

**Step 2: Publish on Amazon KDP first**
- Use your own ISBN (not Amazon's free one)
- Set up ebook and/or print
- **CRITICAL**: in KDP Print settings, **uncheck "Expanded Distribution"** — KDP's Expanded Distribution goes through Ingram anyway, and it will conflict with your IngramSpark setup
- Wait for the book to go live on Amazon (24–72 hours)

**Step 3: Publish on IngramSpark**
- Use the same ISBN you used on KDP (for print — this is fine because you own the ISBN)
- Upload your print-ready PDF and cover
- Ingram will distribute to bookstores and libraries
- Set the discount: 55% is standard for bookstores (they expect 40–50% minimum to stock)
- Enable "Allow Returns" for bookstore orders (required for shelf stocking)

**Step 4: Result**
- Amazon orders fulfilled by KDP (cheaper, faster for Amazon customers)
- Bookstore/library orders fulfilled by Ingram (your IngramSpark setup)
- Same book, same ISBN, maximum distribution

### Important: Avoid the Duplicate Amazon Problem
If IngramSpark tries to distribute to Amazon with an ISBN that KDP already has,
Amazon may list two versions. Prevent this:
- On IngramSpark, in distribution settings, **exclude Amazon** (or KDP Expanded Distribution handles Amazon, not IS)
- Some authors leave it — Amazon detects the duplicate ISBN and merges them — but excluding is cleaner

---

## ASIN vs ISBN

- **ASIN** (Amazon Standard Identification Number): Amazon's internal ID, assigned automatically to every ebook on KDP — not a real ISBN, only works on Amazon
- **ISBN**: Universal — used by all other retailers, libraries, bookstores, the Ingram catalog

KDP ebooks get a free ASIN automatically. You don't need an ISBN for a KDP ebook, but you need one for the print version and for IngramSpark.

---

## ISBN for IngramSpark (2026 Update)

IngramSpark removed the per-title upload fee as of **February 2026**.
They now charge a **1.875% Market Access Fee** on sales instead.

If you use IngramSpark's free ISBN (rather than your own):
- Your imprint shows as "Indie Pub" or similar generic text
- You cannot move this title to another service without a new ISBN
- Strongly recommend buying your own ISBN for any serious publishing

---

## Quick Decision

```
Publishing only to Amazon forever? → Use KDP's free ISBN/ASIN, saves cost
Publishing wide (anywhere except Amazon only)? → Buy your own ISBN from Bowker/Nielsen
Publishing print to bookstores and libraries? → Buy own ISBN + dual KDP/IngramSpark strategy
Multiple books planned? → Buy 10 ISBNs from Bowker ($295) — saves vs singles
```
