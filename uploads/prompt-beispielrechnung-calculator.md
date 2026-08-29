# Claude Design prompt — interactive version of the worked example

Paste into Claude Design, in the same BO Design landing page project. This **replaces the existing "Worked example" / "Beispielrechnung" section** with an interactive version. Keep its position (after the process section, before the FAQ), its card layout, its row structure and its type scale. Only the parts described below change.

---

## WHAT CHANGES

The four assumption values become inputs the visitor controls. The calculation rows recompute live. Everything else — the table-like layout, the explanatory paragraph, the disclaimer, the link to the contact form — stays.

The fields are **pre-filled with the current example values**, so a visitor who touches nothing still reads exactly the worked example that is there today. Interactivity is an offer, not a requirement.

## TWO FIXES TO THE EXISTING SECTION

Apply these while rebuilding:

1. **The "Difference" row must not be the visual peak of the card.** Currently it is bold accent-blue and pulls the eye before the inputs do. Render the result in normal body colour at normal weight; the row keeps only its top border and its bold *label* to close the table. No accent colour on the figure.
2. **The disclaimer must be the same font size as the explanatory paragraph above it** — currently it reads smaller. Same size, same contrast, no lighter tint.

## LEGAL CONSTRAINTS — hard requirements

Same basis as before (§5 UWG, German advertising law). The interactive version adds one constraint that outranks all design considerations:

1. **The visitor sets the target conversion rate themselves.** There must be no pre-selected uplift presented as what this service delivers, no "recommended" or "realistic" marker on the slider, no auto-suggested improvement, no button that raises the scenario value for them. The starting default of 11% exists only because it is the example's value — it must be as freely movable as every other field, and it must never be labelled as expected, typical, or achievable.
2. **No claim of achieved results anywhere in the section.** No "results", "clients see", "typically", "proven", "up to X%", "guaranteed", "ROI". Conditional phrasing only.
3. **Do not add any figure, benchmark, study, source, client name, category or industry** beyond the copy below. If Claude Design wants to helpfully add "average Amazon conversion is X%" — it must not. No sourced numbers at all.
4. **Every field keeps the word "assumption" in its framing** — the group label and the helper text below the scenario field carry this, both are mandatory copy.
5. **Disclaimer stays adjacent to the numbers, inside the card,** minimum 14px, normal body contrast, never collapsed behind a toggle.
6. **Forbidden styling:** before/after layouts, dashboards, gauges, arrows, trend lines, sparklines, animated counters, confetti, green/red semantic colouring, badges like "+22%", progress rings, "Calculate my ROI" style primary buttons. This is a spec sheet with movable values, not a SaaS ROI widget.

If any other instruction in this prompt seems to conflict with this list, the list wins.

## PRIVACY / TECHNICAL CONSTRAINTS

1. **Everything computes client-side.** No API call, no form submission, no server round-trip, no third-party script.
2. **No persistence and no tracking.** No localStorage, no sessionStorage, no cookies, no analytics or pixel events bound to the inputs — not even a generic "calculator_used" event. The entered values must not become part of any data processing, so nothing here requires consent or a new entry in the Datenschutzerklärung.
3. **Do not pre-fill, append or link these values into the contact form.** No hidden fields, no "send my calculation" button. The contact form stays exactly as it is.
4. Recalculation happens on input, with no submit button.

## FIELDS

| Field | Control | Default | Range |
|---|---|---|---|
| Sessions per month | number input, `inputmode="numeric"` | 1,000 | 1 – 1,000,000 |
| Average order value | number input with € affix, `inputmode="decimal"` | 45 | 1 – 10,000 |
| Conversion rate, currently | slider + numeric readout | 9% | 0.5 – 30%, step 0.5 |
| Conversion rate, scenario | slider + numeric readout | 11% | 0.5 – 30%, step 0.5 |

Sliders for the two rates, plain inputs for the two absolute numbers: the rates are a bounded guess worth dragging, the others are figures a seller reads off a report and types.

The scenario value may be set below the current one. Do not block it and do not warn about it — show the resulting negative difference in the same neutral styling.

**Empty or invalid input:** show `—` in the affected calculation rows and, under the field, the helper text given in the copy block. Never block typing, never show a red alarm state, never blame the visitor. A field being briefly empty while someone retypes it is normal.

**Formatting:** results round to whole euros. EN locale `1,000` / `€45`; DE locale `1.000` / `45 €`. Keep `font-variant-numeric: tabular-nums` so figures don't jitter while dragging a slider.

## COPY — verbatim, EN on `/`, DE on `/de`

### EN — route `/`

- **Eyebrow:** Worked example
- **Headline:** What a higher conversion rate is worth
- **Intro:** What a better listing is worth depends on your category, your price and your competition. The lever itself can still be calculated. Set the values yourself — the fields start on freely chosen example values, not on data from a client account.

**Group label:** Your assumptions
- Sessions per month
- Average order value
- Conversion rate, currently
- Conversion rate, scenario
- *Helper text under the scenario field (mandatory):* You set this figure yourself. It's an assumption to calculate with, not a forecast from me.
- *Helper text for an empty or invalid field:* Enter a number above zero to see the calculation.

**Group label:** Calculation
- Currently
- Scenario
- Difference
- *Result row format:* `1,000 × 9% × €45 = €4,050 per month` — the "per month" in muted text, as now
- *Difference row format:* `+€900 per month · €10,800 per year`

**Below the table:** Everything is calculated in your browser. No values are sent, saved or tracked.

**Reset link:** Reset to the example values

**Explanatory paragraph:**
How big a step is realistic depends on category, price, reviews and traffic quality — not on design alone. On the main image the options are limited by Amazon's image guidelines; gallery images from the second slot onwards and A+ Content are the part design actually moves. And if the ad budget stays the same, a higher conversion rate also lowers the cost per order.

**Disclaimer:**
Calculation example based on values you choose yourself. No client data, no guarantee of any particular outcome.

**Link to contact form:** Want to go through your actual listing? Get in touch.

### DE — route `/de`

- **Eyebrow:** Beispielrechnung
- **Headline:** Was eine höhere Conversion Rate wert ist
- **Intro:** Was ein besseres Listing wert ist, hängt von Kategorie, Preis und Wettbewerb ab. Rechnen lässt sich der Hebel trotzdem. Die Werte setzt du selbst — die Felder starten mit frei gewählten Beispielwerten, nicht mit Daten aus einem Kundenkonto.

**Group label:** Deine Annahmen
- Sessions pro Monat
- Ø Warenkorb
- Conversion Rate, aktuell
- Conversion Rate, Szenario
- *Helper text unter dem Szenario-Feld (Pflicht):* Diesen Wert setzt du selbst. Er ist eine Annahme zum Rechnen, keine Prognose von mir.
- *Helper text bei leerem oder ungültigem Feld:* Trag eine Zahl über null ein, um die Rechnung zu sehen.

**Group label:** Rechnung
- Aktuell
- Szenario
- Differenz
- *Zeilenformat:* `1.000 × 9 % × 45 € = 4.050 € pro Monat`
- *Differenz:* `+900 € pro Monat · 10.800 € pro Jahr`

**Unter der Tabelle:** Alles wird in deinem Browser berechnet. Es werden keine Werte gesendet, gespeichert oder getrackt.

**Reset-Link:** Auf die Beispielwerte zurücksetzen

**Erläuterung:**
Wie groß ein realistischer Schritt ist, entscheiden Kategorie, Preis, Bewertungen und Traffic-Qualität — nicht das Design allein. Beim Hauptbild sind die Möglichkeiten durch Amazons Bildrichtlinien begrenzt; Galeriebilder ab Position zwei und A+ Content sind der Teil, den Gestaltung wirklich bewegt. Und bleibt das Werbebudget gleich, sinken mit steigender Conversion Rate auch die Kosten pro Bestellung.

**Disclaimer:**
Rechenbeispiel mit selbst gewählten Werten. Keine Kundendaten, keine Zusicherung eines bestimmten Ergebnisses.

**Link zum Kontaktformular:** Du willst dein Listing konkret durchgehen? Schreib mir.

## INTERACTION DETAIL

- Inputs sit in the value column, right-aligned like the static values were, so the table rhythm survives. On mobile the label may sit above its input.
- Sliders: full row width under their label, current value shown numerically at the right of the label line. Track and thumb in the page's existing neutral tones — no accent-coloured fill that implies "higher is better".
- Touch targets minimum 44px. No native number spinners on mobile.
- Values update as the slider moves, not only on release.
- No entry animation, no count-up on the result. The figure changes instantly.

## ACCESSIBILITY

- Every input has a real `<label>`, not a placeholder acting as one.
- Sliders are `<input type="range">` with `aria-valuetext` including the unit ("9 percent").
- The calculation block is `aria-live="polite"` so updates are announced, but debounce announcements to ~400ms so dragging a slider doesn't flood a screen reader.
- Keep the assumptions and calculation as a real `<table>` or description list with a caption, as in the current version.
- Helper texts are linked to their field with `aria-describedby`.
- Section heading continues the page's existing heading hierarchy.
