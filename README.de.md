# AGIT Project Template

AGIT-Projekt-Template für strukturierte Zusammenarbeit, Projektkontext und Dokumentation.

[English documentation](README.md)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das generische AGIT Project Template.
>
> Das Template dokumentiert Kollaborationspraktiken, Kontextübergabe, Entscheidungsdokumentation und Repository-Konventionen für strukturierte Projektarbeit.
>
> Das Collaboration Model wird in [ChatGPT.md](ChatGPT.md) gepflegt.

## Überblick

Das AGIT Project Template ist ein generischer Startpunkt für Projekte, die von strukturierter Zusammenarbeit, klarem Kontext, dokumentierten Entscheidungen und verlässlicher Übergabe zwischen Arbeitssitzungen profitieren.

Es ist bewusst nicht auf Softwareentwicklung beschränkt. Es kann für Recherche, Planung, Dokumentation, Prozessgestaltung, Konzeptarbeit, operative Projekte und andere strukturierte Projektarbeit verwendet werden.

Für entwicklungsorientierte Projekte mit Code, Skripten, Automatisierung, Tests, Releases und technischer Architektur kann das AGIT Dev Template verwendet werden.

## Was das Template bereitstellt

Dieses Template stellt bereit:

- ein Collaboration Model für Mensch-KI-Projektarbeit
- lokale Codex-Betriebsregeln
- ein Projektkontextdokument für Sitzungsübergaben
- Anleitung zur Projekteinrichtung
- Dokumentationsstandards
- Repository-Standards
- eine gemeinsame Projektphilosophie
- Project Decision Record Guidance für wichtige Entscheidungen
- Arbeitsordner für Inputs, Referenzen, Notizen und Ergebnisse
- Changelog und Versionsmetadaten

## Projektablauf

AGIT-Projekte sollten mit maintainer-eigenem Intent beginnen:

1. Projektzweck und Kontext definieren.
2. Gewünschten Endzustand beschreiben.
3. Grenzen und Nicht-Ziele festlegen.
4. Eine praktikable Roadmap ableiten.
5. In kleinen prüfbaren Schritten arbeiten.
6. Wichtige Entscheidungen dokumentieren.
7. `PROJECT_CONTEXT.md` aktuell halten.
8. Betroffene Dokumente vor wichtigen Meilensteinen harmonisieren.
9. Retrospektiven durchführen, wenn wiederverwendbare Erkenntnisse entstehen.

## Project Decision Records

Wichtige Entscheidungen werden als Project Decision Records (PDRs) dokumentiert.

PDRs eignen sich für dauerhafte Entscheidungen zu Projektausrichtung, Scope, Kollaborationsstruktur, Dokumentationsmodell, Toolwahl, Reviewprozess, Datenschutzgrenzen oder dem Übergang zu einem entwicklungsorientierten Projekt.

Wenn ein Projekt PDRs benötigt, wird folgender Ordner angelegt:

```text
decisions/
```

Das PDR-Konzept ist in [DECISIONS.md](DECISIONS.md) dokumentiert.

## Arbeitsordner

Das Template enthält optionale Arbeitsordner:

- `input/` für vom Maintainer bereitgestellte Materialien
- `references/` für Quellen und Referenzmaterial
- `notes/` für Arbeitsnotizen und offene Fragen
- `output/` für Projektergebnisse

Projekte können diese Ordner anpassen oder entfernen, wenn sie nicht nützlich sind.

## Übergang zu Dev-Projekten

Manche Projekte starten als allgemeine Projekte und werden später entwicklungsorientiert.

Wenn Code, Skripte, Automatisierung, Tests, Releases, technische Architektur oder Implementierungslebenszyklus zentral werden, kann das Projekt Guidance aus dem AGIT Dev Template übernehmen oder dorthin migrieren.

Der Übergang sollte bewusst dokumentiert werden, vorzugsweise mit einem Project Decision Record.

## Kerndokumente

- [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md) - aktueller Projektstand und Übergabepunkt
- [PROJECT_SETUP.md](PROJECT_SETUP.md) - Setup-Anleitung für abgeleitete Projekte
- [ChatGPT.md](ChatGPT.md) - AGIT Collaboration Model
- [CODEX.md](CODEX.md) - lokale Codex Operating Policy
- [PHILOSOPHY.md](PHILOSOPHY.md) - Projektphilosophie
- [DOCUMENTATION.md](DOCUMENTATION.md) - Dokumentationsstandards
- [REPOSITORY.md](REPOSITORY.md) - Repository-Standards
- [DECISIONS.md](DECISIONS.md) - Project Decision Record Guidance
- [CHANGELOG.md](CHANGELOG.md) - Versionshistorie
- [VERSION](VERSION) - aktuelle Template-Versionsmetadaten
- [README.md](README.md) - englische Dokumentation
- [LICENSE](LICENSE) - MIT-Lizenz

## Lizenz

Dieses Projekt steht unter der MIT-Lizenz.
