# SEO-Update v2: Rapid Set ASPHALT REPAIR MIX Landing Page

**Agent:** 3 -- SEO-Spezialist
**Projekt:** KORODUR Rapid Set ARM -- Landing Page v2 (Projekt 002-v2)
**Datum:** 2026-02-27
**Status:** Abgeschlossen
**Basis:** `seo-analyse.md` (v1, 2026-02-23)
**Anlass:** Pivot von Lead-Generierung zu reiner Produktinformationsseite

---

## Vorbemerkung

Dieses Dokument ist ein gezieltes Update der v1-SEO-Analyse. Alles, was in v1 steht und hier nicht erwaehnt wird, gilt weiterhin -- insbesondere die komplette Keyword-Recherche (Kap. 1), technische SEO-Empfehlungen (Kap. 4), Content-SEO-Grundlagen (Kap. 5) und SERP-Feature-Strategie (Kap. 6). Nur die Punkte, die sich durch den Seitentypwechsel aendern, werden hier behandelt.

---

## 1. Title Tag + Meta Description (aktualisiert)

### 1.1 Title Tag

**v1:**
```
Asphaltreparatur dauerhaft in 30 Min. | Rapid Set ARM
```

**v2 -- Empfehlung (55 Zeichen):**
```
Rapid Set ASPHALT REPAIR MIX | Dauerhafte Asphaltreparatur
```

**Alternativ-Varianten:**
- `Asphaltreparatur dauerhaft in 30 Min. | Rapid Set ARM` (55 Zeichen) -- v1-Variante, funktioniert weiterhin
- `Rapid Set ARM -- Dauerhafte Asphaltreparatur ohne Fraese` (57 Zeichen) -- USP-fokussiert

**Was sich aendert und warum:**
- Produktname rueckt an den Anfang. Die Seite ist jetzt eine Produktinformationsseite, kein Aktions-Funnel. Besucher, die ueber Haendler-E-Mail kommen, erkennen den Produktnamen sofort im Browser-Tab.
- "Jetzt Beratung anfragen" oder implizite Aktions-Signale entfallen komplett.
- Das Hauptkeyword "Asphaltreparatur" bleibt enthalten. Die Marke KORODUR wird weiterhin durch die Domain (korodur.de) automatisch in den SERPs angezeigt.

**Hinweis:** Der v1-Title Tag war bereits aktionsfrei formuliert und kann ohne Aenderung uebernommen werden. Die v2-Empfehlung priorisiert lediglich den Produktnamen staerker, was zum neuen Seitentyp passt.

---

### 1.2 Meta Description

**v1:**
```
Rapid Set ASPHALT REPAIR MIX: Dauerhafte Asphaltreparatur in 30 Min. begehbar.
Kein Kaltasphalt, keine Fräse, keine Haftbrücke. Jetzt Beratung anfragen.
```

**v2 -- Empfehlung (155 Zeichen):**
```
Rapid Set ASPHALT REPAIR MIX: Dauerhafte Asphaltreparatur in 30 Min. begehbar. Kein Kaltasphalt, keine Fraese, keine Haftbruecke. Im Baustoffhandel erhaeltlich.
```

**Zeichenzahl:** 160

**Alternativ-Variante (147 Zeichen):**
```
Rapid Set ARM: Die dauerhafte Alternative zu Kaltmischgut. Begehbar nach 30 Min., belastbar nach 1 Std. Alle Fakten und Referenzprojekte.
```

**Was sich aendert:**
| Element | v1 | v2 |
|---------|----|----|
| Abschluss | "Jetzt Beratung anfragen." | "Im Baustoffhandel erhaeltlich." |
| Tonfall | Aktivierend (CTA) | Informierend (Bezugsquelle) |
| Rest | Unveraendert | Unveraendert |

**Begruendung:** Die Meta Description ist der erste Kontaktpunkt in den SERPs. "Jetzt Beratung anfragen" suggeriert ein Lead-Ziel, das die Seite nicht mehr hat. "Im Baustoffhandel erhaeltlich" ist sachlich, schliesst den Kreis zur Haendler-Kampagne und signalisiert dem Suchenden: Hier bekommst du Produktinformation, nicht ein Kontaktformular.

---

## 2. Schema Markup Anpassungen

### 2.1 Uebersicht: Was bleibt, was aendert sich

| Schema-Typ | Status v2 | Aenderung |
|------------|-----------|-----------|
| **Product** | Bleibt, angepasst | `offers`-Objekt anpassen: kein Discount/Aktionspreis |
| **FAQPage** | Bleibt, angepasst | Aktions-FAQ entfernen, 2 neue Fragen hinzufuegen |
| **Organization** | Bleibt unveraendert | Keine Aenderungen noetig |
| ~~BreadcrumbList~~ | Weiterhin NICHT verwenden | Learning aus Projekt 001 |

---

### 2.2 Product Schema -- Angepasst

Das `offers`-Objekt in v1 enthielt bereits keinen Aktionspreis oder Discount, sondern "Preis auf Anfrage". Fuer v2 empfehle ich dennoch eine Anpassung: Das `offers`-Objekt wird vereinfacht und auf den Baustoffhandel als Vertriebskanal hingewiesen.

**v2-Product-Schema (geaenderte Stellen markiert):**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Rapid Set ASPHALT REPAIR MIX",
  "description": "Zementbasiertes, polymerverguetetes Reparaturmaterial fuer alle Asphaltflaechen. Dauerhafte Alternative zu Kaltmischgut und Heissasphalt -- begehbar nach 30 Minuten, belastbar nach ca. 1 Stunde. Einbaustaerke 30--600 mm. Erhaeltlich ueber den Baustoffhandel.",
  "brand": {
    "@type": "Brand",
    "name": "Rapid Set"
  },
  "manufacturer": {
    "@type": "Organization",
    "name": "KORODUR International GmbH",
    "url": "https://www.korodur.de"
  },
  "category": "Asphaltreparatur / Reparaturmoertel",
  "material": "Zementbasiert, polymerverguetet, mineralisch",
  "color": "schwarz",
  "additionalProperty": [
    {
      "@type": "PropertyValue",
      "name": "Druckfestigkeit",
      "value": "ca. 38 N/mm²"
    },
    {
      "@type": "PropertyValue",
      "name": "Biegezugfestigkeit",
      "value": "ca. 6,4 N/mm²"
    },
    {
      "@type": "PropertyValue",
      "name": "E-Modul",
      "value": "ca. 22.000 N/mm²"
    },
    {
      "@type": "PropertyValue",
      "name": "Koernung",
      "value": "0--8 mm"
    },
    {
      "@type": "PropertyValue",
      "name": "Einbaustaerke",
      "value": "30--600 mm"
    },
    {
      "@type": "PropertyValue",
      "name": "Begehbar nach",
      "value": "ca. 30 Minuten"
    },
    {
      "@type": "PropertyValue",
      "name": "Voll belastbar nach",
      "value": "ca. 1 Stunde"
    },
    {
      "@type": "PropertyValue",
      "name": "Lieferform",
      "value": "25 kg Sack"
    },
    {
      "@type": "PropertyValue",
      "name": "Wasserzugabe",
      "value": "ca. 3,80 l pro 25 kg"
    },
    {
      "@type": "PropertyValue",
      "name": "Materialverbrauch",
      "value": "ca. 20 kg/m²/cm"
    },
    {
      "@type": "PropertyValue",
      "name": "Verarbeitungstemperatur",
      "value": "5 °C bis 30 °C"
    },
    {
      "@type": "PropertyValue",
      "name": "CO₂-Reduktion",
      "value": "ca. 30 % weniger CO₂ als herkoemmlicher Portlandzement"
    }
  ],
  "offers": {
    "@type": "Offer",
    "availability": "https://schema.org/InStock",
    "description": "Erhaeltlich ueber den Baustoffhandel. Preis auf Anfrage beim Haendler.",
    "url": "https://www.korodur.de/asphaltreparatur-rapid-set/",
    "seller": {
      "@type": "Organization",
      "name": "KORODUR International GmbH"
    }
  },
  "image": "https://www.korodur.de/assets/images/rapid-set-asphalt-repair-mix.jpg",
  "url": "https://www.korodur.de/asphaltreparatur-rapid-set/"
}
</script>
```

**Aenderungen gegenueber v1:**

| Feld | v1 | v2 | Begruendung |
|------|----|----|-------------|
| `description` | Endet mit "Einbaustaerke 30--600 mm." | Ergaenzt um "Erhaeltlich ueber den Baustoffhandel." | Bezugshinweis fuer Suchende |
| `offers.priceCurrency` | "EUR" | **Entfernt** | Kein Preis wird genannt, Currency ohne Price ist irrefuehrend |
| `offers.priceSpecification` | Vorhanden (mit "Preis auf Anfrage") | **Entfernt** | Vereinfachung, vermeidet Google-Warnings |
| `offers.description` | "Preis auf Anfrage -- projektspezifische Kalkulation" | "Erhaeltlich ueber den Baustoffhandel. Preis auf Anfrage beim Haendler." | Haendler als Bezugskanal hervorheben |

**Option: `offers` komplett entfernen.** Wenn Google weiterhin Warnings zu fehlendem Preis erzeugt, kann das `offers`-Objekt auch komplett entfernt werden. Die Produktinformationen bleiben ueber `additionalProperty` vollstaendig erhalten. Das ist fuer v2 sogar die sauberere Variante, da die Seite keinen Kaufabschluss ermoeglicht.

---

### 2.3 FAQPage Schema -- Aktualisiert

**Aenderungen:**
- Keine Aktions-FAQ vorhanden (v1 hatte auch keine im Schema -- die Aktions-FAQ existierte nur im sichtbaren Content)
- 2 neue Fragen hinzufuegen: "Wo kann ich ARM kaufen?" und "Kann ich ARM selbst verarbeiten?"
- Die 7 bestehenden Fragen bleiben erhalten (alle produktbezogen, aktionsunabhaengig)

**v2-FAQPage-Schema (9 Fragen, neu hinzugefuegte markiert):**

```json
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Was ist Rapid Set ASPHALT REPAIR MIX?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Rapid Set ASPHALT REPAIR MIX (ARM) ist ein zementbasiertes, polymerverguetetes Reparaturmaterial fuer alle Asphaltflaechen. Es vereint die Geschwindigkeit von Kaltmischgut mit der Dauerhaftigkeit von Heissasphalt -- begehbar nach 30 Minuten, voll belastbar nach ca. 1 Stunde. Einbaustaerke von 30 bis 600 mm."
      }
    },
    {
      "@type": "Question",
      "name": "Warum ist Rapid Set ARM besser als Kaltasphalt?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Kaltasphalt (Kaltmischgut) ist eine temporaere Loesung, die oft nach wenigen Wochen wieder aufreisst. Rapid Set ARM ist mineralisch und erreicht eine Druckfestigkeit von ca. 38 N/mm². Es ist frostbestaendig, tausalzbestaendig und bietet eine dauerhafte Reparatur -- ohne die typischen Nacharbeiten, die bei Kaltmischgut noetig werden."
      }
    },
    {
      "@type": "Question",
      "name": "Wie schnell kann eine mit ARM reparierte Flaeche wieder genutzt werden?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Rapid Set ARM ist bereits nach ca. 30 Minuten begehbar und nach ca. 1 Stunde voll belastbar -- auch fuer Fahrzeugverkehr. Das ist deutlich schneller als Heissasphalt, der Abkuehlzeit und Maschinen benoetigt, und zuverlaessiger als Kaltmischgut."
      }
    },
    {
      "@type": "Question",
      "name": "Brauche ich eine Haftbruecke oder spezielle Grundierung?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Nein. Rapid Set ARM haftet exzellent ohne Haftbruecke oder Primer auf dem vorhandenen Untergrund. Die Schadstelle muss lediglich sauber, tragfaehig und vorgenaeesst sein. Das spart Zeit und Material auf der Baustelle."
      }
    },
    {
      "@type": "Question",
      "name": "Welche Schichtdicken kann ich mit ARM einbauen?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Rapid Set ARM kann in Schichtdicken von 30 bis 600 mm eingebaut werden. Das reicht von flachen Oberflaechenschaeden ueber tiefe Schlagloecher bis hin zur Reparatur von Schachtabdeckungen und Rinneneinlaeufen. Das Material ist auch pumpfaehig und kann horizontal sowie vertikal eingesetzt werden."
      }
    },
    {
      "@type": "Question",
      "name": "Kann ARM auch bei niedrigen Temperaturen verarbeitet werden?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ja. Rapid Set ARM kann bei Temperaturen von 5 °C bis 30 °C verarbeitet werden. Das macht es besonders geeignet fuer Reparaturen im Fruehjahr nach der Frostperiode, wenn die meisten Schlagloecher und Frostschaeden auftreten -- anders als Heissasphalt, der waermere Temperaturen benoetigt."
      }
    },
    {
      "@type": "Question",
      "name": "Wie nachhaltig ist Rapid Set ASPHALT REPAIR MIX?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Rapid Set ARM verursacht ca. 30 % weniger CO₂ als herkoemmlicher Portlandzement. Zudem wird recyceltes Zuschlagmaterial eingesetzt und der Einsatz von Primaeerrohstoffen reduziert. Da ARM-Reparaturen dauerhaft halten, entfallen wiederholte Reparatureinsaetze mit entsprechendem Material- und Energieaufwand."
      }
    },
    {
      "@type": "Question",
      "name": "Wo kann ich Rapid Set ARM kaufen?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Rapid Set ASPHALT REPAIR MIX ist ueber den Baustoffhandel erhaeltlich. Fragen Sie Ihren Haendler nach Verfuegbarkeit und Konditionen. Fuer groessere Projekte oder technische Beratung koennen Sie sich auch direkt an KORODUR wenden unter korodur.de/kontakt."
      }
    },
    {
      "@type": "Question",
      "name": "Kann ich Rapid Set ARM selbst verarbeiten?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Ja. Rapid Set ARM ist fuer die einfache Verarbeitung konzipiert -- auch ohne Fachpersonal. Material aus dem 25-kg-Sack mit ca. 3,8 Liter Wasser mischen, in die vorbereitete Schadstelle einfuellen, verdichten, fertig. Kein Heissasphalt-Equipment, keine Haftbruecke, keine Spezialwerkzeuge erforderlich."
      }
    }
  ]
}
</script>
```

**Aenderungen gegenueber v1:**

| Aenderung | Detail |
|-----------|--------|
| FAQ 8 (NEU) | "Wo kann ich Rapid Set ARM kaufen?" -- Schliesst den Kreis zur Haendler-Kampagne. SEO-relevant fuer "Asphaltreparaturmoertel kaufen", "ARM bestellen". |
| FAQ 9 (NEU) | "Kann ich Rapid Set ARM selbst verarbeiten?" -- Adressiert "Schlagloch selber reparieren" (100--200/Monat) und "Asphalt reparieren ohne Maschinen" (10--30/Monat). Staerkt den DIY-Aspekt. |
| FAQ 1--7 | Inhaltlich unveraendert. Alle 7 Fragen sind produktbezogen und aktionsunabhaengig. |

**Reihenfolge-Empfehlung fuer die sichtbare FAQ-Section:** Die letzte sichtbare FAQ-Frage sollte "Wo kann ich Rapid Set ARM kaufen?" sein (analog zur Empfehlung des Strategen). Das schliesst den Storytelling-Bogen: *Information aufgenommen -> ueberzeugt -> wo kaufen?*

---

### 2.4 Organization Schema -- Unveraendert

Das Organization-Schema aus v1 (Abschnitt 3.4 der SEO-Analyse) bleibt komplett unveraendert. Keine Anpassungen noetig.

---

## 3. Keyword-Strategie: Anpassungen

### 3.1 Was bleibt (alles Wesentliche)

Die gesamte Keyword-Recherche aus v1 (Cluster A--G, Top 15, LSI-Keywords) gilt unveraendert. Die Suchintention der Nutzer aendert sich nicht dadurch, dass die Seite jetzt eine Produktinformationsseite statt einer Aktionsseite ist. Wer "Asphaltreparatur" oder "Schlagloch reparieren" googelt, hat dasselbe Problem wie vorher.

### 3.2 Was sich verschiebt

| Aspekt | v1 | v2 | Auswirkung |
|--------|----|----|------------|
| **Primaerer Traffic-Kanal** | Organische Suche + Ads | Haendler-E-Mail-Link (primaer), organische Suche (sekundaer) | SEO bleibt wichtig, ist aber nicht mehr der Haupt-Treiber |
| **Suchintention-Match** | Transaktional ("Jetzt anfragen") | Informational/Commercial ("Alles erfahren") | Content darf informierender sein, weniger CTA-getrieben |
| **Conversion-Keywords** | "Beratung anfragen", "Angebot sichern" | "Datenblatt herunterladen", "im Baustoffhandel erhaeltlich" | Andere Conversion-Signalwoerter im Content |

### 3.3 Neue Keywords fuer v2

Durch die Kaufkanal-Aenderung (Baustoffhandel statt Direktkontakt) werden folgende Keywords relevant:

| Keyword | Suchvolumen (geschaetzt) | Einsatzort |
|---------|--------------------------|------------|
| Asphaltreparaturmoertel kaufen | 10--30/Monat | FAQ "Wo kann ich ARM kaufen?" |
| Asphaltreparatur Baustoffhandel | <10/Monat | FAQ, Footer |
| Asphalt reparieren selber machen | 50--100/Monat | FAQ "Kann ich ARM selbst verarbeiten?" |
| Schlagloch selber reparieren | 100--200/Monat | FAQ, "So funktioniert's" |
| Asphaltreparatur Material | 30--80/Monat | Produktbeschreibung |

Diese Keywords waren teilweise schon in v1 als "zusaetzliche FAQ-Kandidaten" aufgefuehrt (Abschnitt 5.4). Jetzt werden sie durch den neuen Seitentyp aktiviert.

### 3.4 Keywords, die an Bedeutung verlieren

| Keyword-Bereich | Begruendung |
|-----------------|-------------|
| "Beratung anfragen" / "Angebot anfordern" | Kein Lead-Ziel mehr, kein Formular auf der Seite |
| "Fruehjahrsaktion" / "Aktion Asphaltreparatur" | War nie im SEO-Schema, aber im sichtbaren Content -- jetzt komplett irrelevant |
| Dringlichkeits-Keywords ("sofort", "jetzt") | Passen nicht zum informierenden Tonfall |

**Wichtig:** Diese Keywords werden nicht aktiv "entfernt" -- sie tauchen einfach nicht mehr im Content auf. Die Keyword-Strategie wird nicht kleiner, sondern verschiebt ihren Schwerpunkt.

---

## 4. On-Page Empfehlungen: Heading-Struktur v2

### 4.1 H1 -- Angepasst

**v1:**
```
H1: Rapid Set ASPHALT REPAIR MIX -- Dauerhafte Asphaltreparatur in 30 Minuten
```

**v2 -- Empfehlung:**
```
H1: Rapid Set ASPHALT REPAIR MIX -- Dauerhafte Asphaltreparatur in 30 Minuten
```

**Keine Aenderung.** Die H1 aus v1 war bereits produktfokussiert und aktionsfrei. Sie enthaelt den Produktnamen, das Hauptkeyword und den zeitlichen USP. Das passt perfekt zur v2-Seite.

Alternative, falls ein kuerzerer H1 gewuenscht ist:
```
H1: Rapid Set ASPHALT REPAIR MIX -- Die dauerhafte Alternative zu Kaltmischgut
```

---

### 4.2 H2-H3-Struktur -- Angepasst an v2-Seitenstruktur

Die Sektionsreihenfolge aendert sich gegenueber v1 (siehe Strategie-Update Kap. 7). Hier die angepasste Heading-Struktur:

```
H1: Rapid Set ASPHALT REPAIR MIX -- Dauerhafte Asphaltreparatur in 30 Minuten

  H2: Warum Kaltmischgut keine dauerhafte Loesung ist
    H3: Jedes Jahr dieselbe Stelle -- das Problem mit Kaltasphalt
    H3: Die dritte Option: Schneller als Heissasphalt, haltbarer als Kaltmischgut

  H2: So funktioniert Rapid Set ARM -- in 4 Schritten
    H3: Schritt 1: Schadstelle vorbereiten
    H3: Schritt 2: Wasser zugeben und mischen
    H3: Schritt 3: Einbauen und verdichten
    H3: Schritt 4: Nach 30 Minuten begehbar

  H2: Rapid Set ARM vs. Kaltmischgut vs. Heissasphalt
    (Vergleichstabelle, keine H3 noetig)

  H2: Bewaehrt in der Praxis -- Referenzprojekte
    H3: Parkplatzsanierung bei laufendem Betrieb (Kaufland, Bukarest)
    H3: LKW-Ausfahrt unter Extremlast (KS-Werke, Sassenberg)
    H3: Gehwegsanierung Kommune (Oelie/Saur, Saint-Etienne)

  H2: Fuer jede Flaeche. Fuer jeden Einsatz.
    H3: Kommunen & Tiefbauaemter
    H3: GaLa-Bau & Strassenbau
    H3: Facility Management
    H3: Verarbeiter & Handwerker

  H2: Technische Daten im Ueberblick
    H3: Leistungsmerkmale und Kennwerte

  H2: Haeufige Fragen zu Rapid Set ASPHALT REPAIR MIX
    (FAQ-Items als sichtbare Accordion-Elemente, Schema-konform)

  H2: Groesseres Projekt? Wir beraten Sie gerne.
    (Einziger CTA, dezent, am Seitenende)
```

### 4.3 Aenderungen gegenueber v1-Heading-Struktur

| Aenderung | v1 | v2 | SEO-Begruendung |
|-----------|----|----|-----------------|
| Vergleich und Referenzen getauscht | Referenzen (H2 #5), Vergleich (H2 #4) | Vergleich (H2 #3), Referenzen (H2 #4) | Fakten vor Beweis -- passt zum informierenden Charakter. Vergleichstabelle ist staerkster Featured-Snippet-Kandidat und profitiert von frueherer Positionierung. |
| "Warum KORODUR?" entfernt | Eigene H2-Sektion | In Hero/Footer integriert | Schlanker, weniger Eigenwerbung auf einer Informationsseite |
| "Beratung anfragen" H2 geaendert | "Beratung anfragen -- Ihr Projekt, unsere Loesung" + H3 "In 2 Schritten..." | "Groesseres Projekt? Wir beraten Sie gerne." (ohne H3) | Kein Formular, kein Multi-Step -- nur ein dezenter Text-Link |
| Aktions-Sektion entfaellt | War als eigene H2 denkbar | **Komplett entfernt** | Keine Aktion, kein Markup, kein Content |

---

## 5. Open Graph / Social Tags -- Angepasst

### 5.1 Anpassungen

**v1-OG-Description:**
```
Dauerhafte Asphaltreparatur ohne Heißasphalt und Spezialgeräte.
Begehbar nach 30 Min., belastbar nach 1 Std. Jetzt Beratung anfragen.
```

**v2-OG-Description:**
```
Dauerhafte Asphaltreparatur ohne Heissasphalt und Spezialgeraete.
Begehbar nach 30 Min., belastbar nach 1 Std. Alle Fakten und Referenzen.
```

**Aenderung:** "Jetzt Beratung anfragen" ersetzt durch "Alle Fakten und Referenzen." -- informierender Abschluss statt CTA.

OG-Title und Twitter-Card analog zum neuen Title Tag anpassen:

```html
<meta property="og:title" content="Rapid Set ASPHALT REPAIR MIX | Dauerhafte Asphaltreparatur" />
<meta property="og:description" content="Dauerhafte Asphaltreparatur ohne Heissasphalt und Spezialgeraete. Begehbar nach 30 Min., belastbar nach 1 Std. Alle Fakten und Referenzen." />

<meta name="twitter:title" content="Rapid Set ASPHALT REPAIR MIX | Dauerhafte Asphaltreparatur" />
<meta name="twitter:description" content="Dauerhafte Asphaltreparatur ohne Heissasphalt und Spezialgeraete. Begehbar nach 30 Min., belastbar nach 1 Std. Alle Fakten und Referenzen." />
```

Alle anderen OG-Tags (type, url, image, locale, site_name) bleiben unveraendert.

---

## 6. Zusammenfassung: Checkliste fuer Agent 6 (Landing Page Builder)

Kompakte Uebersicht aller SEO-Aenderungen v1 -> v2:

### Muss geaendert werden:

- [ ] **Meta Description:** "Jetzt Beratung anfragen" ersetzen durch "Im Baustoffhandel erhaeltlich."
- [ ] **OG/Twitter Description:** "Jetzt Beratung anfragen" ersetzen durch "Alle Fakten und Referenzen."
- [ ] **FAQPage Schema:** 2 neue Fragen hinzufuegen ("Wo kann ich ARM kaufen?", "Kann ich ARM selbst verarbeiten?")
- [ ] **Product Schema `offers`:** `priceCurrency` und `priceSpecification` entfernen, `description` auf Baustoffhandel anpassen -- ODER `offers` komplett entfernen
- [ ] **CTA-H2:** "Beratung anfragen -- Ihr Projekt, unsere Loesung" ersetzen durch "Groesseres Projekt? Wir beraten Sie gerne."
- [ ] **Heading-Reihenfolge:** Vergleichstabelle vor Referenzen (falls nicht bereits so)
- [ ] **Aktions-Sektion:** Komplett entfernen (alle H2/H3 die sich auf Fruehjahrs-Aktion beziehen)

### Kann optional angepasst werden:

- [ ] **Title Tag:** Produktname an den Anfang ruecken (optional, v1-Version funktioniert auch)
- [ ] **OG Title:** Analog zum Title Tag
- [ ] **H1:** Bleibt idealerweise unveraendert

### Bleibt unveraendert (explizit bestaetigt):

- Organization Schema
- Canonical URL
- Robots Meta Tag
- URL-Struktur
- Alt-Text-Strategie
- Interne Verlinkung (Datenblatt-PDF, Referenzseiten, korodur.de/kontakt/)
- Alle technischen SEO-Massnahmen (Ladezeit, Mobile, Core Web Vitals)
- Keyword-Cluster A--G und Top-15-Priorisierung
- LSI-Keywords und semantische Begriffe
- Featured-Snippet-Strategie (Tabelle, Liste, Paragraph)

---

*Erstellt von Agent 3 (SEO-Spezialist) am 2026-02-27*
*Basis: seo-analyse.md (v1) + 05-briefing-v2-produktseite.md + 06-strategie-update-v2.md*
*Naechster Schritt: Weitergabe an Agent 6 (Landing Page Builder) fuer Implementierung*
