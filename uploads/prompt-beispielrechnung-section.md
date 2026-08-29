# Claude Design prompt — "Worked example" / "Beispielrechnung" section

Paste everything below into Claude Design, inside the existing BO Design landing page project.

---

## TASK

Add one new section to the existing landing page. It goes **after the process section** ("You send the product." → "First result in days.") and **before the FAQ**. Same section width, same vertical rhythm, same type scale as the rest of the page. Do not restyle anything else.

The section shows a **worked calculation with openly assumed values**. It is not a case study, not a result, not a testimonial. This distinction drives every decision below, so read the constraints before designing.

## LEGAL CONSTRAINTS — these are hard requirements, not preferences

This page advertises a service in Germany (§5 UWG). Concrete performance figures presented as achieved results must be substantiable. This section deliberately avoids that by presenting arithmetic on declared assumptions instead.

Therefore:

1. **Never present the numbers as an achieved outcome.** No "results", "we achieved", "clients see", "typically", "proven", "up to X%", "guaranteed". Use conditional phrasing only ("if the conversion rate rises to…").
2. **Do not invent or add any figure, percentage, study, source, client name, industry or category** beyond the copy given below. If a value is missing, leave the field out — do not fill it.
3. **Every input value must be visibly labelled as an assumption.** The word "assumed" / "angenommen" must appear in the input group, not only in the footnote.
4. **The disclaimer must be legible and adjacent to the numbers** — same content block, not the page footer. Minimum 14px, normal body contrast. Do not render it in a lighter tint, smaller size, or collapsed/expandable element. (German case law on Blickfangwerbung: a footnote that is visually subordinate does not cure a headline figure.)
5. **Do not style this like a performance report.** Specifically forbidden: before/after comparison layout, dashboard or screenshot mockups, arrows, trend lines, sparklines, green/red semantic colouring, big animated counters, badge shapes like "+22%", progress rings, star ratings.
6. **The visual emphasis belongs on the method, not on the delta.** The €900 figure may be highlighted as the row conclusion, but must not be the largest element in the section and must not sit above the assumptions. The reader has to see the inputs before the outcome.

If any instruction elsewhere in this prompt appears to conflict with this list, the list wins.

## LAYOUT

A single card or bordered block, calm and table-like — closer to an invoice or a spec sheet than to a marketing stat band.

Vertical order, top to bottom:

1. Eyebrow label
2. Headline
3. Intro paragraph (max two lines on desktop)
4. **Assumptions** — a labelled group of four rows: `label ......... value`, right-aligned values, hairline separators
5. **Calculation** — three rows in the same visual language: starting point, scenario, difference. The difference row is the only one allowed a slightly heavier weight or a top border to close the table.
6. Explanatory paragraph (the honest caveats — do not shorten or cut it, it carries the legal framing)
7. Disclaimer line
8. One text link to the existing contact form anchor

Use tabular figures / `font-variant-numeric: tabular-nums` so the numbers align. Reuse the existing hand-drawn underline accent already used in the page's headings if it fits the eyebrow or headline — do not introduce new decorative elements, colours, gradients or shadows beyond what the page already uses.

Mobile: the label/value rows stack or compress to two columns without horizontal scrolling. The formula strings (`1,000 × 9% × €45`) must not wrap mid-formula — reduce their size or let them sit on their own line under the label.

## COPY — use verbatim, do not rewrite, do not machine-translate

English copy goes on `/`, German copy on `/de`. Both strings are final. Keep number formatting exactly as written (EN: `1,000` / `€45` — DE: `1.000` / `45 €`).

### EN — route `/`

- **Eyebrow:** Worked example
- **Headline:** What two percentage points of conversion are worth
- **Intro:** What a better listing is worth depends on your category, your price and your competition. The lever itself can still be calculated. The values below are freely chosen assumptions, not data from a client account.

**Assumptions (group label: Assumed values)**
- Sessions per month → 1,000
- Average order value → €45
- Conversion rate, starting point → 9%
- Conversion rate, scenario → 11%

**Calculation (group label: Calculation)**
- Starting point → 1,000 × 9% × €45 = €4,050 per month
- Scenario → 1,000 × 11% × €45 = €4,950 per month
- Difference → +€900 per month · €10,800 per year

**Explanatory paragraph:**
Two percentage points is a deliberately modest step. Whether more or less is possible depends on category, price, reviews and traffic quality — not on design alone. On the main image the options are limited by Amazon's image guidelines; gallery images from the second slot onwards and A+ Content are the part design actually moves. And if the ad budget stays the same, a higher conversion rate also lowers the cost per order.

**Disclaimer:**
Worked example based on assumed values. No client data, no guarantee of any particular outcome.

**Link:** Send me your own numbers and I'll run the same example with them.

### DE — route `/de`

- **Eyebrow:** Beispielrechnung
- **Headline:** Was zwei Prozentpunkte Conversion ausmachen
- **Intro:** Was ein besseres Listing wert ist, hängt von Kategorie, Preis und Wettbewerb ab. Rechnen lässt sich der Hebel trotzdem. Die Werte unten sind frei gewählte Annahmen, keine Daten aus einem Kundenkonto.

**Annahmen (group label: Angenommene Werte)**
- Sessions pro Monat → 1.000
- Ø Warenkorb → 45 €
- Conversion Rate, Ausgangslage → 9 %
- Conversion Rate, Szenario → 11 %

**Rechnung (group label: Rechnung)**
- Ausgangslage → 1.000 × 9 % × 45 € = 4.050 € pro Monat
- Szenario → 1.000 × 11 % × 45 € = 4.950 € pro Monat
- Differenz → +900 € pro Monat · 10.800 € pro Jahr

**Erläuterung:**
Zwei Prozentpunkte sind bewusst konservativ gewählt. Ob mehr oder weniger möglich ist, entscheiden Kategorie, Preis, Bewertungen und Traffic-Qualität — nicht das Design allein. Beim Hauptbild sind die Möglichkeiten durch Amazons Bildrichtlinien begrenzt; Galeriebilder ab Position zwei und A+ Content sind der Teil, den Gestaltung wirklich bewegt. Und bleibt das Werbebudget gleich, sinken mit steigender Conversion Rate auch die Kosten pro Bestellung.

**Disclaimer:**
Rechenbeispiel mit angenommenen Werten. Keine Kundendaten, keine Zusicherung eines bestimmten Ergebnisses.

**Link:** Schick mir deine eigenen Zahlen und ich rechne das Beispiel damit durch.

## ACCESSIBILITY

Mark up the assumptions and the calculation as a real `<table>` with a `<caption>` (visually hidden if needed), or as a description list — not as a grid of loose `<div>`s. The `×` and `=` characters must not be the only carriers of meaning for screen readers; give the calculation rows readable text alternatives via the row labels. Section gets a proper heading level continuing the page's existing hierarchy.
