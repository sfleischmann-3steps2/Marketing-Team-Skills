# KORODUR Landing Page Blueprint

Wiederverwendbares Design-System und Style Guide für alle KORODUR-Themenseiten.
Extrahiert aus den Projekten NEODUR AutoStore und Asphalt Repair Mix (Februar 2026).

---

## 1. Design-System

### 1.1 Farbpalette

| Farbe | Hex | CSS Variable | Verwendung |
|-------|-----|-------------|------------|
| Dunkelblau (Primär) | `#002d59` | `--primary` | Headlines, Text, Header/Footer, dunkle Sektionen |
| Cyan (Sekundär) | `#009ee3` | `--secondary` / `--cta` | CTAs, Buttons, Highlights, Zahlen, aktive Tabs |
| Hellgrau | `#ececed` | `--light-gray` | Hintergründe alternierender Sektionen |
| Mittelgrau | `#d9dada` | `--mid-gray` | Rahmen, Tabellenlinien, inactive States |
| Weiß | `#ffffff` | `--white` | Standard-Hintergrund |
| CTA Hover | `#007bb5` | – | Button-Hover-State (abgedunkeltes Cyan) |
| Fehler-Rot | `#d32f2f` | – | Formular-Validierung |
| Muted Text | `#5a6a7a` | – | Micro-Copy, Labels, Zeitangaben |

**Regeln:**
- Buttons immer Cyan (`#009ee3`), sparsam einsetzen
- Text auf dunklen Flächen: Weiß
- Hervorhebungen: Cyan
- Keine zusätzlichen Farben ohne Abstimmung

### 1.2 Typografie

**Font:** Gabarito (Google Fonts)
- Schnitte: 400 (Regular), 700 (Bold), 800 (ExtraBold), 900 (Black)
- Fallback: Arial, sans-serif

| Element | Gewicht | Größe | Transform |
|---------|---------|-------|-----------|
| H1 | 900 (Black) | `clamp(2rem, 5vw, 3.2rem)` | UPPERCASE |
| H2 | 900 (Black) | `clamp(1.6rem, 3.5vw, 2.4rem)` | UPPERCASE |
| H3 | 700 (Bold) | `clamp(1.1rem, 2vw, 1.4rem)` | normal |
| Subline | 800 (ExtraBold) | inherit | UPPERCASE |
| Fließtext | 400 (Regular) | 1rem | normal |
| Micro-Copy | 400 (Regular) | 0.85rem | normal |
| Buttons | 700 (Bold) | 1rem | normal |

**Regeln:**
- Headlines und Sublines immer VERSAL (uppercase)
- Fließtext-Farbe: Dunkelblau (`#002d59`)
- Line-height: 1.6 (Fließtext), 1.15-1.2 (Headlines)

### 1.3 Abstände & Layout

```
--max-w: 1200px          (Container-Breite)
--section-pad-d: 80px    (Sektion Padding Desktop)
--section-pad-m: 48px    (Sektion Padding Mobile)
--radius: 8px            (Standard Border-Radius)
--card-radius: 12px      (Karten Border-Radius)
--shadow: 0 2px 12px rgba(0,45,89,.08)  (Standard Schatten)
Container padding: 0 24px
```

### 1.4 Buttons

| Typ | Klasse | Style |
|-----|--------|-------|
| Primär | `.btn-primary` | Cyan Background, weiße Schrift, Cyan Border |
| Ghost | `.btn-ghost` | Transparent, Cyan Schrift, Cyan Border |
| Hover (Primär) | – | `#007bb5`, translateY(-1px) |
| Hover (Ghost) | – | Cyan Background, weiße Schrift |

```css
.btn {
  padding: 16px 32px;
  border-radius: 8px;
  border: 2px solid transparent;
  font-weight: 700;
  font-size: 1rem;
}
```

### 1.5 Karten

```css
.card {
  background: var(--white);
  border-radius: var(--card-radius);    /* 12px */
  box-shadow: var(--shadow);
  padding: 32px 24px;
}
```

- Problem-Cards: 4px farbiger Top-Border
- Hover-Effekt: `translateY(-4px)` bei interaktiven Karten

---

## 2. Seitenstruktur-Template

### Standard-Reihenfolge der Sektionen

```
1. HEADER (sticky, weiß, Logo links, Nav rechts)
2. HERO (Gradient-Hintergrund, H1, Subline, Key Figures, CTAs)
3. MINI TRUST BAR (Dunkelblau, 4 Trust-Items, inside Hero)
4. PROBLEM (Grauer Hintergrund, 3 Problem-Cards, Section Bridge)
5. LÖSUNG / SO FUNKTIONIERT'S (Weiß, Schritte/Features)
6. ZIELGRUPPEN (Tabs Desktop / Accordion Mobile)
7. VERGLEICH (Grau, Tabelle Desktop / Cards Mobile)
8. [Optional: SYSTEM-AUFBAU / REFERENZEN]
9. TECHNISCHE DATEN (Tabelle + Merkmale-Liste)
10. TRUST / WARUM KORODUR (Weiß, Trust-Grid)
11. FAQ (Accordion)
12. CTA / KONTAKTFORMULAR (Multi-Step Form)
13. FOOTER (Dunkelblau)
14. STICKY CTA (Fixed Bottom, ab Scroll-Trigger)
15. COOKIE BANNER (Fixed Bottom)
```

### Farbwechsel-Schema (alternierend)

```
Hero:      bg-white (mit Gradient)
Trust Bar: bg-dark
Problem:   bg-gray
Lösung:    bg-white
Zielgruppen: bg-gray oder bg-white
Vergleich: bg-gray
Technik:   bg-white oder bg-gray
Trust:     bg-white
FAQ:       bg-gray oder bg-white
CTA/Form:  bg-gray oder bg-white
Footer:    bg-dark
```

---

## 3. Komponenten-Bibliothek

### 3.1 Header

- Sticky, weiß, Border-Bottom 1px Mittelgrau
- Logo links: "KORODUR" in Gabarito Black, Dunkelblau
- Nav rechts: Anker-Links zu Sektionen, Bold, 0.9rem
- Mobile: Hamburger-Button, Nav als Dropdown

### 3.2 Hero Section

- Gradient: `linear-gradient(135deg, #ececed 0%, #ffffff 100%)`
- H1: Produktversprechen in einem Satz
- Subline: 1-2 Sätze Kontext
- Key Figures: 4er Grid mit Zahl + Label (Cards)
- CTA-Reihe: Primary + Ghost Button
- Micro-Copy unter CTAs

### 3.3 Mini Trust Bar

- Dunkelblau-Hintergrund
- 4 Items: Icon + Bold Text
- Flexbox, zentriert, Wrap

### 3.4 Problem Section

- 3 Problem-Cards nebeneinander
- Icon (Unicode/Emoji), H3, Beschreibung
- Section Bridge: Dunkelblau-Box mit Überleitung zur Lösung
- Optional: Letzte Card hervorgehoben (bei ARM: Lösungs-Preview)

### 3.5 Zielgruppen (Tabs/Accordion)

- Desktop: Tabs mit horizontalen Buttons
- Mobile: Accordion
- Jeder Tab: H3, Fließtext, Bullet-Liste, CTA-Button
- Optional: Referenz-Hinweis pro Zielgruppe

### 3.6 Vergleichstabelle

- Desktop: `<table>` mit farbcodierten Headern
- Mobile: Cards pro Kriterium
- KORODUR-Spalte hervorgehoben (Cyan, Bold)
- Summary-Box darunter: Cyan-Linksborder

### 3.7 Kontaktformular (Multi-Step)

- 2-3 Schritte, Progress-Bar oben
- Step 1: Rolle + Projekttyp/Anwendungsfall
- Step 2: Name, Firma, E-Mail (+ optionale Details Toggle)
- Datenschutz-Checkbox (required)
- Success-State mit Bestätigung
- Trust-Liste unter dem Formular

### 3.8 FAQ Accordion

- Ein-/Ausklappen einzeln (nur eins offen)
- Active State: Dunkelblau Hintergrund, weiße Schrift
- `aria-expanded` Attribut
- Schema.org FAQPage Markup im `<head>`

### 3.9 Footer

- Dunkelblau, 2-Spalten Grid
- Links: Firma-Daten (Adresse, Tel, E-Mail)
- Rechts: Footer-Links (Impressum, Datenschutz, Produkte etc.)
- Bottom-Bar: Claim "KORODUR – ... seit 1936. Made in Germany."

### 3.10 Sticky CTA

- Fixed Bottom, Weiß, Schatten
- Erscheint wenn Hero-CTAs nicht sichtbar, verschwindet bei Kontakt-Sektion
- IntersectionObserver-basiert

---

## 4. Content-Guidelines

### 4.1 Tonalität

- **Zielgruppe:** B2B-Baubranche (Bauherren, Planer, Verarbeiter, Facility Manager)
- **Ton:** Professionell, klar, vertrauenswürdig
- **Sprachstil:** Technisch-präzise, aber verständlich
- **Perspektive:** Du/Sie-Ansprache (Sie im B2B-Kontext)
- **Gedankenstrich:** Immer kurzer Strich (–), kein langer (—)

### 4.2 Headline-Regeln

- **H1 (Hero):** Produktversprechen in einem Satz. Benefit vor Feature.
  - Gut: "Der Boden, den Ihre Roboter brauchen."
  - Gut: "Einmal reparieren. Dauerhaft halten."
  - Schlecht: "NEODUR Level Industrieboden-System"

- **H2 (Sektionen):** Problem oder Nutzen adressieren, nicht Feature beschreiben.
  - Gut: "Automatisierung verzeiht keine Unebenheiten."
  - Gut: "Jedes Jahr dieselbe Stelle flicken? Das muss nicht sein."
  - Schlecht: "Unsere Produkte im Überblick"

- **H3 (Cards/Tabs):** Kurz, spezifisch, aktiv formuliert.

### 4.3 CTA-Hierarchie

| Stufe | Text-Muster | Button-Typ | Wo |
|-------|-------------|------------|-----|
| Primär | "Jetzt beraten lassen" / "Projekt bewerten lassen" | btn-primary | Hero, nach Sektionen, Form |
| Sekundär | "Datenblatt herunterladen (PDF)" | btn-ghost | Hero, Technik-Sektion |
| Tertiär | "Ausschreibungstexte anfordern" | btn-ghost | Zielgruppen-Tabs |

**Regeln:**
- Max. 2 CTAs pro Sichtfeld
- Primary CTA immer links/oben
- Micro-Copy unter CTAs: Kostenloses Angebot betonen, Zeitrahmen nennen
  - "Kostenlos und unverbindlich – Antwort innerhalb von 48 Stunden."

### 4.4 Trust-Signale

Standardmäßig einsetzen:
1. **Mini Trust Bar** (Hero): 4 Items mit Unternehmens-Credentials
   - Jahre Erfahrung, Projekte weltweit, Zertifizierung, Made in Germany
2. **Referenzprojekte** (eigene Sektion oder in Zielgruppen-Tabs)
   - Mit Ort, Jahr, Verarbeiter, konkretem Ergebnis
3. **Testimonials** (Blockquote mit Zitat und Firma)
4. **Trust-Liste** (unter Formular)
   - Kostenlos, Antwortzeit, kein Vertriebsdruck, Datenschutz

---

## 5. SEO-Standard

### Meta Tags

```html
<title>[Produkt] | [Nutzenversprechen] | KORODUR</title>
<meta name="description" content="[Produkt]: [Hauptvorteil]. [2-3 Key Facts]. Jetzt Beratung anfragen.">
<meta name="robots" content="index, follow">
<link rel="canonical" href="https://www.korodur.de/[slug]/">
<meta property="og:title" content="...">
<meta property="og:description" content="...">
<meta property="og:type" content="product">
<meta property="og:url" content="...">
<meta property="og:locale" content="de_DE">
<meta property="og:site_name" content="KORODUR">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="...">
<meta name="twitter:description" content="...">
```

### Schema.org Markup

Immer einbinden:
1. **Product** – Produktdaten, Hersteller, Eigenschaften
2. **FAQPage** – Alle FAQ-Einträge
3. **Organization** – KORODUR-Firmendaten

### URL-Konvention

`https://www.korodur.de/[produktname-oder-thema]/`

---

## 6. Formular-Standard

### Struktur

- **Step 1:** Qualifizierung (Rolle, Projekttyp/Anwendungsfall)
  - Optional: Checkbox für Musterverlegung/Demo
- **Step 2:** Kontaktdaten (Name*, Firma*, E-Mail*, Telefon optional)
  - Toggle: Zusätzliche Projektdetails (Fläche, Zeitraum, Nachricht)
  - Datenschutz-Checkbox (required, Link zur Datenschutzerklärung)

### Validierung

- Client-seitig: Required-Felder prüfen, E-Mail-Format
- Error-State: Rote Border, Fehlermeldung unter dem Feld
- Datenschutz nicht gecheckt: Rote Schrift

### Success-State

- Formular + Progress ausblenden
- Bestätigungstext: "Vielen Dank für Ihre Anfrage!" + Zeitangabe (48h)
- Optional: Download-Link zum Datenblatt

---

## 7. Technische Standards

### Performance

- Google Fonts mit `preconnect` + `preload`
- Images mit `loading="lazy"`, `width` und `height` Attributen
- Inline CSS (kein externes Stylesheet für Landing Pages)
- Inline JS am Ende des `<body>`

### Accessibility

- `aria-label` auf Navigation und Buttons
- `aria-expanded` auf alle Accordion/FAQ-Buttons
- Semantisches HTML: `<header>`, `<nav>`, `<section>`, `<footer>`
- Tabellen: `<thead>`/`<tbody>`, `aria-label`
- Fokus-Styles für Keyboard-Navigation (`:focus`)
- Cookie-Banner mit `role` und Keyboard-Support

### Responsive Breakpoints

```
Desktop: > 1024px       (volles Layout)
Tablet:  769px–1024px   (Grid-Anpassungen)
Mobile:  ≤ 768px        (1-Spalte, Accordion statt Tabs, Cards statt Tabelle)
Small:   ≤ 480px        (Stack-Layout für Key Figures etc.)
```

### Cookie Consent

- Banner am unteren Rand, Dunkelblau
- Akzeptieren + Ablehnen Buttons
- `localStorage` für Consent-Status
- Link zur Datenschutzerklärung

---

## 8. Checkliste für neue KORODUR-Seiten

- [ ] Farben und Typografie aus diesem Blueprint übernommen
- [ ] Gabarito Font geladen (400, 700, 800, 900)
- [ ] Seitenstruktur folgt dem Template (Sektion 2)
- [ ] Hero: H1 benefit-orientiert, Key Figures, 2 CTAs, Micro-Copy
- [ ] Mini Trust Bar mit 4 Credentials
- [ ] Problem-Sektion mit 3 Cards + Section Bridge
- [ ] Zielgruppen: Tabs (Desktop) + Accordion (Mobile)
- [ ] Vergleichstabelle: Table (Desktop) + Cards (Mobile)
- [ ] FAQ mit Schema.org + aria-expanded
- [ ] Multi-Step Formular mit Datenschutz-Checkbox
- [ ] Alle Meta-Tags (OG, Twitter, Schema.org)
- [ ] Footer mit echten KORODUR-Links
- [ ] Cookie Banner mit Datenschutz-Link
- [ ] Sticky CTA (IntersectionObserver)
- [ ] Keine alert() oder Placeholder-Links
- [ ] Mobile Responsive getestet (768px, 480px)
