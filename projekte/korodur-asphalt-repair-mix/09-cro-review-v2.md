# CRO-Review: ARM Landing Page v2 (Produktinformationsseite)

**Agent:** 4 -- CRO-Optimierer
**Projekt:** KORODUR Rapid Set ARM -- Landing Page v2 (Projekt 002-v2)
**Datum:** 2026-02-27
**Status:** Abgeschlossen
**Basis:** 05-briefing-v2-produktseite.md, 08-landing-page-content-v2.md

**Vorbemerkung:** Diese Seite ist KEINE klassische Conversion-Seite. Der Endkunde kommt ueber eine Haendler-E-Mail, hat bereits erstes Interesse und soll durch sachliche Information zum Kauf beim Haendler ueberzeugt werden. Das CRO-Review bewertet daher Informationsqualitaet, Vertrauensaufbau und Nutzerfluss -- nicht Conversion Rate im engeren Sinn.

---

## 1. Informationsarchitektur-Check

**Bewertung: Gut -- eine Anpassung empfohlen.**

Die Sektionsreihenfolge folgt einem sauberen narrativen Bogen:

```
Hero (Versprechen) → Trust-Leiste (Beleg) → Problem (Relevanz) → Loesung (Wie?) →
Vergleich (Warum besser?) → Referenzen (Beweis) → Zielgruppen (Fuer mich?) →
Technik (Details) → FAQ (Restfragen) → Kontakt
```

Das ist fuer einen "warmen" Besucher (weiss schon, worum es geht) die richtige Abfolge. Er bekommt zuerst die Kernaussage, dann den Beweis, dann die Details.

**Eine Anpassung:** Die Mini-Trust-Leiste (Sektion 2) steht direkt unter dem Hero -- das ist korrekt. Aber die Referenzen (Sektion 6) kommen erst nach dem Vergleich. Fuer einen warmen Besucher, der vom Haendler kommt, ist Social Proof ("andere nutzen das auch") oft ueberzeugender als technische Vergleiche. Pruefen, ob Referenzen und Vergleichstabelle getauscht werden sollten:

- **Aktuell:** Problem → Loesung → Vergleich → Referenzen
- **Alternative:** Problem → Loesung → Referenzen → Vergleich

Empfehlung: Aktuelle Reihenfolge beibehalten. Begruendung: Der Besucher braucht zuerst das intellektuelle Argument (Vergleich), bevor die Referenzen den emotionalen Beweis liefern. Das ist die staerkere Abfolge fuer ein erklaerungsbeduerftiges B2B-Produkt.

---

## 2. Trust-Signal-Verteilung

**Bewertung: Sehr gut -- ueber die gesamte Seite verteilt.**

| Sektion | Trust-Signal | Typ |
|---|---|---|
| Hero | Key Figures (30 Min., 38 N/mm2, 50+ Referenzen) | Zahlen/Fakten |
| Sektion 2 | Mini-Trust-Leiste (seit 2021, seit 1936, Schwerlast) | Autoritaet |
| Sektion 3 | Problemkarte ARM mit "50+ Referenzprojekte" | Social Proof |
| Sektion 5 | Vergleichstabelle mit konkreten Werten | Fakten |
| Sektion 6 | Testimonial + 4 Referenzkarten mit echten Firmennamen | Social Proof |
| Sektion 7 | Referenzhinweis in jedem Zielgruppen-Tab | Social Proof |
| Sektion 8 | Vollstaendige technische Datentabelle | Fakten |

**Positiv:** Kein Trust-Signal-Vakuum auf der Seite. Jede Sektion liefert mindestens einen Beleg. Die Referenzkarten mit echten Firmennamen, Orten und Jahreszahlen sind der staerkste Trust-Faktor.

**Ein Hinweis:** Das Testimonial-Zitat (F & G Bau GmbH) steht momentan nur ueber den Referenzkarten. Es ist das einzige Zitat auf der gesamten Seite. Falls ein zweites Zitat verfuegbar ist (z. B. von Knappheide oder Dieckmann), koennte es in der Technik-Sektion oder im Hero-Bereich platziert werden, um Trust auch in den Fakten-Sektionen spuerbar zu machen. Kein Muss, aber ein optionales Plus.

---

## 3. Datenblatt-Download als Mikro-Conversion

**Bewertung: Gut positioniert, aber Tracking sicherstellen.**

Der PDF-Download erscheint an 7 Stellen:
1. Hero (Hauptbutton)
2. Zielgruppen-Tab 1 (Kommunen)
3. Zielgruppen-Tab 2 (GaLa-Bau)
4. Zielgruppen-Tab 3 (Facility Management)
5. Zielgruppen-Tab 4 (Verarbeiter)
6. Technik-Sektion
7. Footer

**Das ist sinnvoll.** Der Datenblatt-Download ist die einzige messbare Nutzeraktion neben dem finalen CTA. Er dient gleichzeitig als "Takeaway" -- der Besucher hat etwas Handfestes zum Weiterleiten an Kollegen oder zum Vorlegen beim Haendler.

**Empfehlung fuer den Builder:**
- Alle Datenblatt-Links mit einem einheitlichen `data-event="datenblatt-download"` oder UTM-Parameter versehen, damit spaeter nachvollzogen werden kann, aus welcher Sektion die meisten Downloads kommen.
- Der Hero-Button sollte als Outline-Button gestaltet sein (wie im Content vorgesehen) -- nicht als dominanter Cyan-Button. Er soll Informationsangebot sein, kein Conversion-Druck.

---

## 4. Der eine CTA am Ende

**Bewertung: Text und Platzierung stimmen. Gestaltungsdetail beachten.**

**Text:** "Groesseres Projekt? Wir beraten Sie gerne." + Button "Beratung anfragen"
**Platzierung:** Sektion 10, nach FAQ, vor Footer -- korrekt am Ende der Informationsreise.
**Zielgruppe:** Nur fuer den kleinen Teil der Besucher, der ein Grossprojekt plant und direkten KORODUR-Kontakt braucht.

Das ist genau richtig. Der CTA filtert sich selbst: Wer kein grosses Projekt hat, scrollt vorbei. Wer eines hat, wird hier abgeholt.

**Gestaltungsempfehlung fuer den Builder:**
- Hellgrauer Hintergrund (#ececed) -- korrekt geplant. Kein dunkler Block, der "Vertrieb!" schreit.
- Button in Cyan (#009ee3), aber **nicht breiter als 280px**. Er soll auffindbar sein, nicht die Sektion dominieren.
- Telefonnummer und E-Mail **unter** dem Button, nicht daneben. Das gibt dem Besucher eine Alternative, ohne den Button zu verdraengen.
- Kein Formular, kein Multi-Step -- der Link zur korodur.de/kontakt/-Seite reicht. Weniger Reibung.

---

## 5. Mobile UX: Toggle/Accordion-Struktur

**Bewertung: Grundstruktur passt. Drei Punkte beachten.**

Die Seite nutzt Accordion/Toggle fuer:
- Zielgruppen (4 Tabs Desktop → 4 Accordions Mobile)
- FAQ (Accordion auf allen Geraeten)

**Empfehlungen:**

1. **Vergleichstabelle auf Mobile:** Die 3-Spalten-Tabelle (ARM vs. Kaltmischgut vs. Heissasphalt) wird auf Mobile als "gestapelte Karten" geplant. Das ist die richtige Entscheidung. Wichtig: Jede Karte sollte die ARM-Spalte visuell hervorheben (Cyan-Rand), damit der Besucher auch in der gestapelten Ansicht sofort sieht, welches Produkt gewinnt.

2. **Zielgruppen-Accordion -- Default-Zustand:** Auf Mobile sollte der erste Accordion-Eintrag (Kommunen) standardmaessig geoeffnet sein. Ein komplett geschlossenes Accordion wirkt auf Mobile wie leerer Raum und erhoert die Absprungwahrscheinlichkeit. Die uebrigen drei bleiben geschlossen.

3. **Scroll-Tiefe auf Mobile:** Die Seite hat 11 Sektionen. Auf Mobile sind das ca. 8-10 Bildschirmhoehen. Das ist akzeptabel fuer eine Informationsseite (kein harter Conversion-Druck), aber der Builder sollte darauf achten, dass die Sektionen auf Mobile nicht zu "luftig" sind. Kompakte Abstaende zwischen den Sektionen halten den Scrollfluss.

---

## 6. Drei Quick-Wins fuer den Builder

### Quick-Win 1: Scroll-Indikator im Hero

Der Hero hat keinen CTA-Button, der zum Scrollen motiviert. Ein dezenter Scroll-Indikator (animierter Pfeil nach unten oder "Mehr erfahren" als Ankerlink zur Problem-Sektion) verhindert, dass Mobile-Nutzer den Hero fuer die gesamte Seite halten. Kein Button -- nur ein visueller Hinweis, dass es weitergeht.

### Quick-Win 2: Sticky "Zurueck nach oben"-Button auf Mobile

Da die Seite lang ist und keinen Sticky CTA hat, fehlt eine Navigationshilfe auf Mobile. Ein dezenter "Nach oben"-Button (erscheint ab Sektion 4) verbessert die Navigation erheblich. Klein, rund, unten rechts, halbtransparent -- kein Aufmerksamkeits-Konkurrent.

### Quick-Win 3: Referenzkarten mit "Nachkontrolle"-Badge priorisieren

Die Wueseke-Karte hat einen speziellen Badge: "Nachkontrolle nach 1,5 Jahren: Flaeche intakt." Das ist das staerkste einzelne Argument auf der gesamten Seite -- es belegt Dauerhaftigkeit mit Zeitbeweis. Diese Karte sollte auf Mobile als **erste** Referenzkarte erscheinen (Position 1 statt Position 3), damit sie auch bei fruehzeitigem Abbruch des Scrollens gesehen wird.

---

## Gesamtbewertung

Die v2-Seite ist ein sauberer Umbau von einer Aktions- zu einer Informationsseite. Die CTA-Reduktion ist konsequent umgesetzt, die Trust-Signale sind gut verteilt, und die Sektionsreihenfolge folgt einem ueberzeugenden narrativen Bogen. Die drei Quick-Wins sind kleine Optimierungen, die ohne inhaltliche Aenderungen umsetzbar sind.

**Keine Blocker fuer den Builder. Seite kann gebaut werden.**

---

*Erstellt von Agent 4 (CRO-Optimierer) am 2026-02-27*
*Basis: 05-briefing-v2-produktseite.md, 08-landing-page-content-v2.md*
*Naechster Schritt: Weitergabe an Agent 6 (Landing Page Builder) zusammen mit dem Content-Dokument*
