# AGIT Project Template

AGIT-Projekt-Template für strukturierte Zusammenarbeit, Projektkontext und Dokumentation.

[English documentation](README.md)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das generische AGIT Project Template.
>
> Das Template dokumentiert KI-gestützte Kollaborationspraktiken, Kontextübergabe, Entscheidungsdokumentation und Repository-Konventionen für strukturierte Projektarbeit.
>
> Das Collaboration Model wird in [ChatGPT.md](ChatGPT.md) gepflegt.

## Überblick

Das AGIT Project Template ist ein generischer Startpunkt für Projekte, die von strukturierter Zusammenarbeit, klarem Kontext, dokumentierten Entscheidungen und verlässlicher Übergabe zwischen Arbeitssitzungen profitieren.

Es ist bewusst nicht auf Softwareentwicklung beschränkt. Es kann für Recherche, Planung, Dokumentation, Prozessgestaltung, Konzeptarbeit, operative Projekte und andere strukturierte Projektarbeit verwendet werden.

Für entwicklungsorientierte Projekte mit Code, Skripten, Automatisierung, Tests, Releases und technischer Architektur kann das AGIT Dev Template verwendet werden.

## AGIT Templateverse

Die öffentlichen AGIT Templates bilden ein kleines Templateverse: eine Familie zusammenhängender Templates, die ein repository-first, maintainer-geführtes Modell für Human-AI Collaboration teilen und für unterschiedliche Projekttypen spezialisieren.

- [AGIT Project Template](https://github.com/ctreffe/agit-project-template) ist der generische Startpunkt für strukturierte Projektarbeit, Recherche, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) ist für technische Dokumentationsprojekte gedacht, etwa Benutzerhandbücher, Admin-Guides, Betriebsanweisungen, Tutorials, Migrationsguides und Dokumentationssites.

Das generische Project Template passt, wenn die Projektform noch offen ist. Ein spezialisiertes Template passt, wenn Entwicklungs- oder Dokumentationspraxis bereits im Zentrum der Arbeit steht.

## Was das Template bereitstellt

Dieses Template stellt bereit:

- ein Collaboration Model für Mensch-KI-Projektarbeit
- lokale Codex-Betriebsregeln
- ein Projektkontextdokument für Sitzungsübergaben
- Anleitung zur Projekteinrichtung und einen reproduzierbaren initialen Prompt
- Dokumentationsstandards
- Repository-Standards
- eine gemeinsame Projektphilosophie
- Project Decision Record Guidance für wichtige Entscheidungen
- Arbeitsordner für Inputs, Referenzen, Notizen und Ergebnisse
- Guidance zum Umgang mit sensiblen Rohquellen, geprüften Derivaten und generierten Outputs
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
- [INITIAL_PROMPT.md](INITIAL_PROMPT.md) - reproduzierbarer erster Prompt für die Projektinitialisierung
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


## Template-spezifische Initialisierungsdokumente

Die folgenden Dokumente unterstützen vor allem die Projekteinrichtung:

- `PROJECT_SETUP.md`
- `INITIAL_PROMPT.md`
- `DOCUMENTATION.md`
- `REPOSITORY.md`

Nach Abschluss der Ersteinrichtung können diese Dokumente aus dem abgeleiteten Projekt entfernt werden, sofern sie dort nicht weiterhin nützlich sind. Sie können auch für Onboarding, Nachvollziehbarkeit oder spätere Re-Initialisierung behalten werden. Beibehaltene Initialisierungsdateien behalten ihre ursprünglichen Namen; ihr Setup-Status kann optional in der Datei selbst oder in `PROJECT_CONTEXT.md` dokumentiert werden.
## Lizenz

Dieses Projekt steht unter der MIT-Lizenz.
