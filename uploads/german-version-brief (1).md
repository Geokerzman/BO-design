# Design brief — German version

Add a German version of the Start page. The Impressum and Datenschutz pages are already in German and stay exactly as they are — do not touch them, do not create English versions of them.

---

## Structure

- English Start page stays at `/`
- German Start page goes to `/de`
- Impressum stays at `/impressum`, Datenschutz at `/datenschutz` — shared by both language versions

**Language switcher:** in the nav, right of the menu links and left of the button. Two labels, `DE` and `EN`, separated by a thin `#E5E7EB` vertical divider. The active language is `#111111` Bold; the inactive one is `#6B7280` Regular and links to the other version of the same page. No flag icons, no dropdown, no globe icon — flags stand for countries, not languages, and this is a two-option choice that does not need a menu.

On mobile, where the nav links collapse, the switcher stays visible. It is more important than the menu.

**In the `<head>` of both Start pages**, add reciprocal hreflang tags:
```
<link rel="alternate" hreflang="en" href="[URL]/" />
<link rel="alternate" hreflang="de" href="[URL]/de" />
<link rel="alternate" hreflang="x-default" href="[URL]/" />
```
Set `lang="de"` on the German page and `lang="en"` on the English one.

**Everything else is identical:** same design system, same layout, same components, same image placeholders, same hand annotation in the same two places, same consent checkbox behaviour. Only the words change.

**One layout warning:** German words are longer than English. Check that headlines, button labels, the three-fact line under the hero and the card headings do not break awkwardly at mobile widths. Adjust line breaks and font sizes where needed rather than letting text overflow or shrink inconsistently.

---

## German copy

Use exactly as written. This is adapted copy, not a translation — do not "improve" it back toward the English phrasing. Formal address (`Sie`) throughout.

### Nav
`Arbeiten` · `Preise` · `Über mich` — button: `Angebot anfragen`

### Hero

Headline: **Der Verkauf entscheidet sich in der Galerie.**

Subhead: Galeriebilder und A+ Content für Amazon-Seller. Gestaltet von einem UX-Designer, der seit fünf Jahren daran arbeitet, warum Menschen klicken – und warum nicht.

Three facts: `5 Jahre in deutschen Produktteams` · `Deutsch & Englisch` · `2–7 Tage Lieferzeit`

Buttons: `Angebot anfragen` — `Arbeiten ansehen`

Large figure: `2–7 Tage` — label beneath: `vom Briefing bis zur Lieferung`

### Services
Label: `Leistungen:`

**Galeriebilder** — Die sieben Slots, die entscheiden, ob jemand weiterscrollt oder abspringt. Hero-Shot, Feature-Erklärung, Größe und Maßstab, Lifestyle-Kontext, Vergleich. Nach Amazon-Vorgaben gebaut und schon als Thumbnail lesbar.

**A+ Content** — Der Bereich unterhalb der Galerie, der bei erklärungsbedürftigen Produkten den Kauf abschließt. Modulare Layouts, Vergleichstabellen, Markengeschichte, technische Details – aufgebaut in der Reihenfolge, in der Käufer ihre Einwände haben.

Below: Die meisten Seller brauchen beides. Deshalb sind sie zusammen günstiger.

### Included
Label: `In jedem Projekt enthalten:`

- **Jede Sprache.** Layouts zuerst für Deutsch und Englisch, aber jeder Zielmarkt ist möglich. Um die Typografie kümmere ich mich, damit übersetzte Texte das Layout nicht sprengen.
- **Jede Kategorie.** Elektronik, Möbel, Beauty, Werkzeug, Haushalt. Die Recherche ändert sich, die Methode nicht.
- **Beliebig viele Produkte.** Keine Obergrenze. Varianten werden separat berechnet, weil sie echte Gestaltungsarbeit sind und kein Farbtausch.
- **Offene Dateien.** Sie bekommen die bearbeitbaren Quelldateien, nicht nur fertige JPGs. Die Arbeit bleibt Ihre.

### Work
Label: `Ausgewählte Arbeiten:`

- **Höhenverstellbarer Schreibtisch** — Komplettes Galerie-Set auf Deutsch. Aufgebaut nach Szenarien: Arbeit, Studium, Gaming.
- **Premium-Duft** — Galerie-Konzept für eine Kategorie, in der das Bild das gesamte Produkterlebnis tragen muss.
- **2-in-1-Notebook** — Zweisprachiges Set für ein technisches Produkt, dessen Feature-Liste scanbar bleiben musste.

Disclaimer line in `#6B7280` at 13px, exactly as written:
*Eigenständig erstellte Konzeptarbeiten. Keine Verbindung zu den gezeigten Marken und nicht von diesen beauftragt.*

### Process
Label: `Ablauf:`

1. **Sie schicken mir das Produkt.** Listing-Link, Fotos, Datenblatt – alles, was Sie schon haben.
2. **Ich komme mit einem Plan zurück.** Slot für Slot durchdacht, mit Festpreis, bevor gestaltet wird.
3. **Erster Entwurf in wenigen Tagen.** Das komplette Set, keine Häppchen.
4. **Eine Korrekturrunde ist enthalten.** Weitere Anpassungsrunden werden separat angeboten.

### Pricing
Label: `Preise:`

- **Galeriebilder** — ab 800 €
- **A+ Content** — ab 800 €
- **Beides zusammen** — 1.500 € — tag: `Die meisten entscheiden sich dafür`

Use German number and currency formatting: a full stop as the thousands separator and the € symbol after the figure with a non-breaking space (`1.500 €`, not `€1,500`).

Below the cards:
Der Endpreis richtet sich nach Anzahl der Produkte und Varianten. Sie bekommen einen Festpreis, bevor die Arbeit beginnt – keine Stundenschätzung.
Als Kleinunternehmer gemäß § 19 UStG wird keine Umsatzsteuer berechnet.

### About
Label: `Mit wem Sie arbeiten:`

Ich bin Boris – UX/UI-Designer mit fünf Jahren in deutschen Produktteams, im B2B wie im B2C. Die meiste Zeit davon ging es um genau die Frage, die auch Ihr Listing stellt: Warum kauft jemand hier und springt dort ab.

Dieser Hintergrund ist der Unterschied zwischen einem Bild, das gut aussieht, und einem Bild, das verkauft. Aufbau, Hierarchie, was jemand am Handy in Thumbnail-Größe zuerst liest – das ist die eigentliche Arbeit, und genau die überspringen die meisten Listing-Designer.

Wir arbeiten auf Deutsch oder Englisch, ganz wie es Ihnen lieber ist.

### FAQ
Label: `Fragen:`

- **Wie schnell geht das wirklich?** Zwei bis sieben Tage für ein komplettes Set, je nach Anzahl der Produkte und wie schnell Ihr Feedback kommt.
- **Was brauchen Sie von mir?** Den Listing-Link oder die ASIN, Ihre Produktfotos und die technischen Daten. Wenn Ihre Fotos schwach sind, sagen Sie es früh – das ändert die Herangehensweise.
- **Schreiben Sie auch die Texte?** Ja. Der Text auf den Bildern ist Teil der Gestaltung, kein Nachgedanke. Auf Deutsch oder Englisch.
- **Und Varianten?** Farb- und Größenvarianten werden pro Variante berechnet. Das Umfärben ist der kleinste Teil – Layout, Skalierung und übersetzter Text müssen jedes Mal mit.
- **Arbeiten Sie mit Agenturen?** Ja, auf White-Label-Basis. Melden Sie sich wegen der Konditionen.
- **Wem gehören die Dateien?** Ihnen, mit der Schlusszahlung. Die offenen Quelldateien sind enthalten.

### Contact

Headline: **Schicken Sie mir ein Listing, mit dem Sie unzufrieden sind.**
Subhead: Ich sage Ihnen, was ich ändern würde – bevor Sie sich zu irgendetwas verpflichten.

Form fields: `Name`, `E-Mail`, `Listing-Link oder ASIN`, `Nachricht`
Button: `Senden`

Consent checkbox label, exactly as written — the word `Datenschutzerklärung` is the link:
Ich habe die Datenschutzerklärung gelesen und bin damit einverstanden, dass meine Daten zur Bearbeitung meiner Anfrage verarbeitet werden.

Message shown on attempted submit without consent: Bitte bestätigen Sie dies, um fortzufahren.

Success confirmation: Danke, Ihre Anfrage ist angekommen. Ich melde mich innerhalb eines Werktags.

### Footer
`BO Design` · `Impressum` · `Datenschutz` · copyright line.
Back link on legal pages: `← Zurück zum Start`

---

## Typography note

German uses `„quotation marks like this"` and the en dash `–` with spaces where English uses an em dash. The copy above already follows this. Do not normalise the punctuation to English conventions.
