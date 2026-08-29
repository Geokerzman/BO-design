# Design brief — Impressum page

Build a single page: the German legal notice (`Impressum`) for a freelance design business. This is a legally required page, not a marketing page. Its entire job is to be readable and easy to find.

---

## Design system

**Palette — use these exact values:**
- `#FFFFFF` — page background. Pure white. Not cream, not off-white, no warm tint.
- `#111111` — primary text and headings
- `#6B7280` — secondary text
- `#3B82F6` — accent. Used only for links and the visible keyboard focus state. Nowhere else on this page.
- `#E5E7EB` — hairline dividers. 1px.

No gradients, no colored panels, no cards, no dark mode. This page is deliberately quiet.

**Typography:**
- One geometric grotesque family. Figtree, or General Sans if available. Fallback Inter.
- Page title: Bold (700), tracking about −0.02em.
- Block headings: Bold, at body size — not display size.
- Body: Regular (400), 16px minimum, leading 1.7.

---

## Layout

- Sticky nav, thin, white, hairline bottom border once scrolled. Left: `BO Design` in Bold. Right: a small solid blue button `Get a quote`. Nothing else.
- Single centred column, max width 640px, generous top and bottom padding.
- Page title `Impressum` in Bold, then `Angaben gemäß § 5 DDG` in `#6B7280` directly beneath.
- Content grouped into blocks: Bold heading, then plain text. Blocks separated by a hairline rule and generous whitespace — roughly 48px above and below each rule.
- Address lines break naturally as an address, not as a bulleted list.
- Bottom of the page: a plain text link `← Back to start`.
- Footer: `BO Design`, a link to `Impressum` marked as the current page, a link to `Datenschutz` pointing to `#`, and a copyright line.

## Constraints

- Fully responsive. On mobile the column takes 24px side padding and nothing else changes.
- Email rendered as a `mailto:` link, phone as a `tel:` link.
- Text must stay selectable and copyable.
- No images, no icons, no motion, no scroll animations of any kind.
- Semantic heading order. Visible focus states in `#3B82F6`.

---

## Content

Use the German text below exactly as written. Do not translate it, rewrite it, shorten it, or add sentences to it. Keep the square-bracket placeholder visible so it can be filled in later.

```
Impressum

Angaben gemäß § 5 DDG

BO Design
Inhaber: Boris Onofrei
St.-Ulrich-Straße 33
79189 Bad Krozingen
Deutschland

Kontakt

Telefon: +49 160 95314627
E-Mail: boris.onofrei.design@gmail.com

Umsatzsteuer

Kleinunternehmer gemäß § 19 UStG.
Es wird keine Umsatzsteuer ausgewiesen.

USt-IdNr.: [DE…]

Haftung für Inhalte

Als Diensteanbieter bin ich gemäß § 7 Abs. 1 DDG für eigene Inhalte auf diesen
Seiten nach den allgemeinen Gesetzen verantwortlich. Nach §§ 8 bis 10 DDG bin ich
als Diensteanbieter jedoch nicht verpflichtet, übermittelte oder gespeicherte
fremde Informationen zu überwachen oder nach Umständen zu forschen, die auf eine
rechtswidrige Tätigkeit hinweisen.

Urheberrecht

Die auf diesen Seiten gezeigten Gestaltungsentwürfe sind eigenständig erstellte
Konzeptarbeiten. Sie stehen in keiner Verbindung zu den dargestellten Marken und
wurden nicht von diesen beauftragt. Alle genannten Marken und Produktnamen sind
Eigentum ihrer jeweiligen Inhaber.
```
