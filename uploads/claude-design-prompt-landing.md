# Claude Design prompt — Amazon listing design landing page

*Copy everything below the line into Claude Design as a single message. Attach 6–9 of your best example images alongside it.*

---

Build a single-page website for a freelance Amazon design service. English only. This page is the entire sales funnel: sellers scan a QR code on a printed letter, land here on their phone, and either book a call or email me. There is no second page.

## Who this is for

Amazon sellers on Amazon.de and other EU marketplaces — small and mid-size brand owners, plus e-commerce agencies who outsource production. They are not designers. They are looking at a listing that is underperforming and they can tell the images are the problem, but they cannot articulate why. The page has to make them feel understood in about four seconds, then make ordering feel low-risk.

## Tone

Direct, quietly confident, no agency-speak. No "elevate your brand," no "unlock your potential," no rocket emojis. Short sentences. Every claim is concrete and checkable. Sentence case throughout, never Title Case On Headlines.

---

## Visual direction — follow this precisely

The visual system comes from an existing offer document I send to clients. Match it. This is not a free brief.

**Palette (use these exact values):**
- `#FFFFFF` — page background. Pure white. Do not use cream, off-white, or a warm tint.
- `#111111` — primary text and headlines
- `#6B7280` — secondary text, captions, labels
- `#3B82F6` — the single accent. Bright cornflower blue. Used for: large numerals, key figures, card outlines, links, the primary button, and hand-drawn marks. Nothing else.
- `#E5E7EB` — hairline dividers between sections. 1px, full-width, never a thick rule or a colored band.
- `#F7F8FA` — the only permitted fill tint, used sparingly for image placeholder wells.

No gradients. No colored section backgrounds. No dark mode section. The white is the design — the page should feel like a well-set document, not a SaaS marketing site.

**Typography:**
- One geometric grotesque family for everything. Use Figtree, or General Sans if available. Fallback Inter.
- Headlines: Bold (700), tight tracking (roughly −0.02em), tight leading. Large but not enormous.
- Body: Regular (400), comfortable leading (1.6), max line length 68 characters.
- Labels above sections: 12px, Bold, `#111111`, sentence case, with a colon — matching the offer document's `New deal:` / `Calculations:` treatment. Not uppercase, not letter-spaced eyebrows.
- Figures and prices: set large, in `#3B82F6`, with the currency symbol at a noticeably smaller optical size than the numeral.

**Components:**
- Outlined cards: 2px `#3B82F6` border, 12px radius, white fill, one soft low-opacity shadow offset downward. These are the signature container — use them for service names and package names, not for every block.
- Everything else sits directly on white, separated by whitespace and hairlines. Resist the urge to put things in boxes.
- Generous vertical rhythm: roughly 96px between sections on desktop, 64px on mobile. Whitespace is the main compositional tool.

**Signature element — the hand annotation.** The offer document has one deliberate imperfection: a hand-drawn blue scribble-underline beneath the total figure, plus a small four-point sparkle. Reproduce this as inline SVG, hand-drawn in feel (irregular stroke, slightly overshooting the word), in `#3B82F6`. Use it exactly twice on the whole page: once under the key figure in the hero, once under the bundle price. It is the one warm human mark on an otherwise precise page. Do not turn it into a repeating decorative motif — the restraint is the point.

**Motion:** minimal. A short fade-and-rise on scroll for section content, staggered. Draw the hand-annotation SVG stroke once when it scrolls into view. Nothing else. Respect `prefers-reduced-motion`.

---

## Structure and copy

Use this copy as written. Adjust only for line-breaks and fit.

### 1. Nav
Sticky, thin, white with a hairline bottom border once scrolled. Left: `Boris Onofrei` in Bold. Right: `Work` · `Pricing` · `About` and a small solid blue button `Get a quote`. On mobile the links collapse — keep only the button.

### 2. Hero
Full-width, generous top padding, left-aligned. No hero image, no product mockup, no stock photo.

Headline: **Most listings lose the sale in the gallery.**

Subhead: Gallery images and A+ Content for Amazon sellers — designed by a UX designer who has spent five years working out why people click and why they don't.

Below, a single line of three facts separated by hairline vertical dividers:
`5 years in German product teams` · `English & German` · `2–7 days turnaround`

Two buttons: solid blue `Get a quote`, and a text link with arrow `See the work`.

Somewhere in this block, one large figure in blue with the hand annotation under it — use `2–7 days` as the figure, with the small label `from brief to delivery` beneath. This is the hero's one moment of scale.

### 3. What I do
Label: `Services:`

Two outlined blue cards side by side (stacked on mobile):

**Gallery images** — The seven slots that decide whether someone scrolls or leaves. Hero shot, feature breakdowns, size and scale, lifestyle context, comparison. Built to Amazon's specs, readable at thumbnail size.

**A+ Content** — The section below the fold that closes the sale for considered purchases. Modular layouts, comparison tables, brand story, technical detail — structured so it answers objections in the order buyers raise them.

Under the two cards, one line of plain text: Most sellers need both. They are priced together for that reason.

### 4. Also included
Label: `Every project includes:`

Four short items, no icons, no cards — just a hairline-separated list with a Bold lead-in and one line of text:

- **Any language.** Layouts built for English and German first, but any target market. I handle the typography so translated copy doesn't break the design.
- **Any category.** Consumer electronics, furniture, beauty, tools, home. The research changes; the method doesn't.
- **Any number of products.** No cap on volume. Variations are priced separately because they are real design work, not a colour swap.
- **Raw files.** You get the editable source, not just flattened JPGs. The work stays yours.

### 5. Work
Label: `Selected work:`

A gallery of case blocks. Three products, each with a short heading, a one-line note, and a row of images.

- **Height-adjustable desk** — Full German-language gallery set. Scenario-led structure: work, study, gaming.
- **Premium fragrance** — Gallery concept for a category where the image has to carry the entire product experience.
- **2-in-1 laptop** — Bilingual set for a technical product with a feature list that had to stay scannable.

**Important:** below this section, in `#6B7280` at 13px, place this exact line: *Concept work, produced independently. Not affiliated with or commissioned by the brands shown.*

Images: use placeholder wells in `#F7F8FA` with a thin `#E5E7EB` border and the dimensions labelled inside. Square 1:1 for gallery images, 970×600 for A+ modules. I will drop the real files in myself. On mobile, make each product's row a horizontal swipe strip rather than a stacked column — it mirrors how the Amazon gallery itself behaves, and it stops the page becoming endless.

### 6. How it works
Label: `Process:`

A four-step horizontal sequence with numbered markers — numbering is justified here because the order genuinely matters to the buyer's understanding of the timeline.

1. **You send the product.** Listing link, photos, specs, anything you already have.
2. **I come back with a plan.** Slot-by-slot structure and a fixed price before anything is designed.
3. **First draft in days.** Complete set, not teasers.
4. **One round of changes included.** Further sets of adjustments are quoted separately.

### 7. Pricing
Label: `Pricing:`

Three outlined blue cards. Each shows the price large and in blue, with a smaller `from` above it where relevant.

- **Gallery images** — from €800
- **A+ Content** — from €800
- **Both together** — €1,500 — mark this one as the recommended option with a small blue filled tag reading `Most sellers choose this`. Place the hand-annotation scribble under this figure.

Below the cards, two lines in `#6B7280`:
Final price depends on the number of products and variations. You get a fixed quote before work starts, never an hourly estimate.
As a small business under §19 UStG, no VAT is charged.

### 8. About
Label: `Who you're working with:`

Left column, short paragraphs, no photo needed (leave a small square placeholder well in case I add one later).

I'm Boris — a UX/UI designer with five years in German product teams, working across both B2B and B2C. Most of that time has been spent on the same question your listing is asking: why does someone buy here and leave there.

That background is the difference between an image that looks good and an image that sells. Layout, hierarchy, what a person reads first on a phone at thumbnail size — that's the actual job, and it's the part most listing designers skip.

We work in English and German, whichever suits you.

### 9. FAQ
Label: `Questions:`

Accordion, hairline-separated, no cards, no chevron animations beyond a simple rotate. Six items:

- **How fast is this really?** Two to seven days for a complete set, depending on how many products and how quickly feedback comes back.
- **What do you need from me?** The listing link or ASIN, your product photos, and the specs. If your photography is weak, tell me early — it changes the approach.
- **Do you write the copy too?** Yes. The text on the images is part of the design, not an afterthought, and I write it in English or German.
- **What about variations?** Colour and size variants are quoted per variation. Recolouring is the smallest part of it — layout, scaling and translated text all have to be reworked.
- **Do you work with agencies?** Yes, on a white-label basis. Get in touch about rates.
- **Who owns the files?** You do, on final payment. Raw editable files are included.

### 10. Contact
Full-width block, still white, hairline above.

Headline: **Send me a listing you're unhappy with.**
Subhead: I'll tell you what I'd change before you commit to anything.

A short form: Name, Email, Listing link or ASIN, Message. Submit button `Send`. Below the form, an email address placeholder `[EMAIL]` for people who prefer to write directly.

Form validation should say what's wrong and how to fix it, in plain words. Success state replaces the form with a short confirmation, not a toast.

### 11. Footer
Minimal. Name, `[EMAIL]`, `Impressum` link pointing to `#` for now, and a copyright line. Do not invent an address, VAT number, or company details — leave `[IMPRESSUM PLACEHOLDER]` visible so I remember to complete it.

---

## Constraints

- Mobile-first. This page will mostly be opened on a phone after scanning a QR code. Design the mobile layout first and make sure the hero, one service card and the price are all reachable in the first two thumb-scrolls.
- No stock photography anywhere except inside the work placeholders.
- No icons except the four-point sparkle in the signature annotation, and the small chevron in the FAQ.
- No testimonials, no logo wall, no "trusted by" strip — I don't have them and fake ones are worse than none.
- No statistics I can't back up. No "+47% conversion." No invented numbers of any kind.
- No cookie banner, no chat bubble, no newsletter signup.
- Visible keyboard focus states in the accent blue. Semantic headings in order. Alt text on every placeholder.
- Single self-contained file.
