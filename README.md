# Marketing Team Skills

Ein Team aus 7 KI-Agents, die gemeinsam hochwertige Landing Pages und Vermarktungskonzepte erstellen.

## Konzept

**Team** = Sammlung von Agents
**Agents** = Einzelne Rollen mit spezialisierten Fähigkeiten
**Skills** = Die konkreten Fähigkeiten jedes Agents

## Das Team

| # | Agent | Kernaufgabe |
|---|-------|-------------|
| 0 | **Projektleiter** | Orchestrierung, Qualitätssicherung, Nutzer-Kommunikation |
| 1 | **Stratege** | Konzept, Positionierung, Wettbewerbsanalyse |
| 2 | **Content Creator** | Texte, Copywriting, Social Content |
| 3 | **SEO-Spezialist** | Suchmaschinenoptimierung, Schema Markup |
| 4 | **CRO-Optimierer** | Conversion-Optimierung, A/B-Tests |
| 5 | **Growth Manager** | Traffic, E-Mail-Marketing, Paid Ads |
| 6 | **Landing Page Builder** | Technische Umsetzung der Landing Page |

## Workflow

```
Nutzer-Briefing
     |
[Projektleiter] --> Briefing erstellen
     |
Phase 1: Analyse (parallel)
  - Stratege --> Konzept
  - SEO-Spezialist --> SEO-Audit
     |
Phase 2: Content (sequentiell)
  - Content Creator --> Texte
  - CRO-Optimierer --> Feedback
     |
Phase 3: Umsetzung
  - Landing Page Builder --> Bau
  - SEO --> Schema & Meta
  - CRO --> finale Optimierung
     |
Phase 4: Launch (parallel)
  - Growth Manager --> Promotion
  - CRO --> Tracking & A/B-Tests
```

## Live Landing Pages

**Übersichtsseite:** https://sfleischmann-3steps2.github.io/Marketing-Team-Skills/

### ARM-Kampagne

| Seite | Link | Status |
|-------|------|--------|
| **Rapid Set ARM v2 (Produktseite)** | [Live](https://sfleischmann-3steps2.github.io/Marketing-Team-Skills/projekte/korodur-asphalt-repair-mix/landing-page/index.html) | Aktuell — wartet auf Kollegen-Feedback |

Zielgruppe: Endkunden (via Händler-E-Mail). Reine Produktinformation ohne Aktionsangebot. Einziger CTA: "Größeres Projekt? Beratung anfragen."

### Weitere Landing Pages

| Produkt | Vollversion | Kurzversion |
|---------|------------|-------------|
| **NEODUR Level** | [Vollversion](https://sfleischmann-3steps2.github.io/Marketing-Team-Skills/projekte/korodur-neodur-autostore/landing-page/index.html) | [Kurzversion](https://sfleischmann-3steps2.github.io/Marketing-Team-Skills/projekte/korodur-neodur-autostore/landing-page/index-short.html) |

### Archiv

| Seite | Link | Archiviert |
|-------|------|------------|
| ARM v1 Frühjahrsaktion (Voll) | [Ansehen](https://sfleischmann-3steps2.github.io/Marketing-Team-Skills/projekte/korodur-asphalt-repair-mix/landing-page/archiv/index-v1-fruehjahrsaktion.html) | 27.02.2026 |
| ARM v1 Frühjahrsaktion (Kurz) | [Ansehen](https://sfleischmann-3steps2.github.io/Marketing-Team-Skills/projekte/korodur-asphalt-repair-mix/landing-page/archiv/index-short-v1-fruehjahrsaktion.html) | 27.02.2026 |

## Projektstruktur

```
index.html        # Übersichtsseite (GitHub Pages Root)
agents/           # Agent-Definitionen (SKILL.md pro Agent)
workflows/        # Workflow-Definitionen
templates/        # Vorlagen (Briefings, etc.)
projekte/         # Landing Pages und Projektdateien
  korodur-asphalt-repair-mix/
    briefing.md                        # Original-Briefing (v1)
    05-briefing-v2-produktseite.md     # Briefing v2 (aktuell)
    06-strategie-update-v2.md          # Strategie v2
    07-seo-update-v2.md                # SEO v2
    08-landing-page-content-v2.md      # Content v2
    09-cro-review-v2.md                # CRO Review v2
    landing-page/
      index.html                       # Aktuelle LP (v2)
      archiv/                          # v1 Versionen
assets/           # Gemeinsame Assets (Logo, Bilder, Produktfoto)
```

## Quellen & Inspiration

- [VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills)
- [ComposioHQ/awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills)
- [coreyhaines31/marketingskills](https://github.com/coreyhaines31/marketingskills)
