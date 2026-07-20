# AGIT Project Template

[![Status](https://img.shields.io/badge/status-stable-green)](VERSION)
[![Version](https://img.shields.io/github/v/tag/ctreffe/agit-project-template?label=version)](CHANGELOG.md)
[![License](https://img.shields.io/github/license/ctreffe/agit-project-template)](LICENSE)

> [!NOTE]
> **KI-Zusammenarbeit**
>
> Dieses Repository pflegt das generische AGIT Project Template.
>
> Das Template dokumentiert Praktiken für KI-gestützte Zusammenarbeit, Kontextübergaben, Decision Records und Repository-Konventionen für strukturierte Projektarbeit.
>
> Das Kollaborationsmodell wird in [ChatGPT.md](ChatGPT.md) gepflegt.

<br>

**[Link to the English README](README.md)**

<br>

## Inhalt

- [Überblick](#überblick)
- [Kernprinzip](#kernprinzip)
- [AGIT Templateverse](#agit-templateverse)
- [Wann dieses Template geeignet ist](#wann-dieses-template-geeignet-ist)
- [Projektinitialisierung](#projektinitialisierung)
- [Empfohlener Workflow](#empfohlener-workflow)
- [Git-Index und geschützte Git-Aktionen](#git-index-und-geschützte-git-aktionen)
- [Decision Records](#decision-records)
- [Repository-Struktur](#repository-struktur)
- [Template- und abgeleitete Projektdateien](#template--und-abgeleitete-projektdateien)
- [Verwendung dieses Templates](#verwendung-dieses-templates)
- [Tool-Setup für Maintainer](#tool-setup-für-maintainer)
- [Kontinuierliche Verbesserung](#kontinuierliche-verbesserung)
- [Lizenz](#lizenz)

## Überblick

Das AGIT Project Template ist ein generischer Ausgangspunkt für Projekte, die von strukturierter Zusammenarbeit, explizitem Kontext, dokumentierten Entscheidungen und zuverlässiger Übergabe zwischen Arbeitssitzungen profitieren. Es ist bewusst nicht auf Softwareentwicklung beschränkt: Es unterstützt Forschung, Planung, Konzeptarbeit, Prozessgestaltung, operative Projekte und gemischte Projekttypen.

Das Template stellt ein Repository-zentriertes Kollaborationsmodell, lokale Codex-Regeln, reproduzierbare Setup- und Fortsetzungs-Prompts, einen aktuellen Projektkontext, Dokumentations- und Repository-Standards, Leitlinien für Decision Records und optionale Arbeitsordner bereit. Es ist eine Projektmethode und Repository-Grundlage, kein domänenspezifisches Framework.

## Kernprinzip

Der Maintainer verantwortet Projektintention und -richtung. Der Assistant kann Informationen strukturieren, Lücken erkennen, Artefakte vorbereiten, Konsistenz prüfen und Projektwissen bewahren, darf aber den gewünschten Endzustand nicht erfinden, folgenreiche Entscheidungen nicht stillschweigend treffen und Arbeit nicht als abgeschlossen ausgeben, wenn sie nicht existiert.

Das Repository ist das dauerhafte Projektgedächtnis. Künftige Maintainer, Mitwirkende oder Assistants sollen den aktuellen Zustand verstehen und die Arbeit fortsetzen können, ohne auf private Chatverläufe angewiesen zu sein.

## AGIT Templateverse

Die öffentlichen AGIT-Templates bilden ein kleines Templateverse: eine Familie verwandter Templates, die ein Repository-zentriertes, vom Maintainer geführtes Modell der Mensch-KI-Zusammenarbeit teilen und es für unterschiedliche Projekttypen spezialisieren.

- Das [AGIT Project Template](https://github.com/ctreffe/agit-project-template) ist der generische Ausgangspunkt für strukturierte Projektarbeit, Forschung, Planung, Konzeptarbeit, Prozessgestaltung und gemischte Projekte.
- Das [AGIT Dev Template](https://github.com/ctreffe/agit-dev-template) ist für entwicklungsorientierte Projekte gedacht, in denen Code, Skripte, Automatisierung, Validierung, Architektur oder Release-Workflows zentral sind.
- Das [AGIT Documentation Template](https://github.com/ctreffe/agit-docs-template) ist für technische Dokumentationsprojekte wie Benutzer- und Administrationshandbücher, Betriebsanweisungen, Tutorials, Migrationsleitfäden und Dokumentationswebsites gedacht.

## Wann dieses Template geeignet ist

Verwende das Project Template, wenn die Projektform noch offen ist oder mehrere Arbeitsarten ein gemeinsames Projektgedächtnis benötigen. Es eignet sich gut für Discovery, Planung, Forschung, Koordination, Prozessgestaltung und Projekte, die später stärker spezialisiert werden können.

Beginne mit einem spezialisierten Template, wenn die primäre Arbeit bereits feststeht:

- das Dev Template für Implementierung, Tests, Automatisierung und Releases;
- das Documentation Template für zielgruppenorientierte technische Dokumentation und Veröffentlichung;
Wenn ein generisches Projekt später entwicklungsorientiert wird, dokumentiere den Übergang und übernimm das Dev Template oder migriere bewusst dorthin.

## Projektinitialisierung

Nach dem Erzeugen des Repositorys muss der Maintainer nur
[INITIAL_PROMPT.md](INITIAL_PROMPT.md) aufrufen. Der Prompt weist den Agenten an,
das Repository zu lesen, alle Setup-Leitlinien anzuwenden und die vollständige
Initialisierung zu führen. Der Maintainer muss `PROJECT_SETUP.md` oder die
anderen Setup-Dateien nicht separat öffnen oder ausführen.

Die einfachste Anweisung an den Agenten lautet:

> Lies `INITIAL_PROMPT.md` vollständig und führe den darin enthaltenen Initialisierungs-Prompt aus.

Die Datei muss dafür nicht geöffnet und ihr Prompt nicht in die Unterhaltung kopiert werden.

Der Agent:

1. liest die Kollaborations-, Setup-, Dokumentations-, Repository- und Entscheidungsregeln;
2. prüft die Repository-Baseline, ohne die Git-Historie zu verändern;
3. stellt kompakte Fragen zu vom Maintainer definiertem Zweck, gewünschtem Endzustand, Zielgruppe, Grenzen, Risiken, Roadmap, Quellenbehandlung und Review-Modell;
4. fragt jede folgenreiche Entscheidung ab, statt Projektrichtung zu erfinden;
5. passt nach den Antworten README-Dateien, Projektkontext, Arbeitsordner und laufende Projektregeln an;
6. dokumentiert Template-Baseline und Initialisierungsprovenienz in [PROJECT_CONTEXT.md](PROJECT_CONTEXT.md);
7. prüft, dass erforderliche Platzhalter und ungelöste Setup-Entscheidungen sichtbar sind; und
8. übergibt den initialisierten Repository-Zustand mit Validierungsergebnissen, Einschränkungen und vorgeschlagenen Commit-Metadaten.

`PROJECT_SETUP.md` bleibt die detaillierte Initialisierungscheckliste des Agenten
und ein Provenienzartefakt. `INITIAL_PROMPT.md` ist der einzige
benutzerorientierte Einstiegspunkt, der diese Checkliste aktiviert.

## Empfohlener Workflow

AGIT-Projekte entwickeln sich von der Maintainer-Intention aus in kleinen, prüfbaren Projektschleifen:

```text
Intention -> Roadmap -> Erzeugen -> Prüfen -> Harmonisieren -> Festhalten -> Fortsetzen
```

1. Ermittle oder bestätige die Repository-Baseline.
2. Prüfe Maintainer-Intention, gewünschten Endzustand und aktuelle Roadmap.
3. Wähle den kleinsten sinnvollen Schritt, der Unsicherheit reduziert oder ein prüfbares Ergebnis erzeugt.
4. Erzeuge oder überarbeite das Projektartefakt.
5. Prüfe oder validiere das Ergebnis und mache Einschränkungen sichtbar.
6. Aktualisiere betroffenen Kontext, Dokumentation und Decision Records.
7. Bereite einen regulären Arbeits-Commit mit passendem Conventional-Commit-Präfix vor.
8. Fahre fort, bis das Milestone-Ziel erreicht ist.
9. Schließe den Milestone separat ab, indem aktueller Zustand, Versionierung und Historie abgeglichen werden.

Verwende [CONTINUATION_PROMPT.md](CONTINUATION_PROMPT.md), um das Projekt in einer neuen Sitzung zu rekonstruieren. Verwende [HARMONIZATION_PROMPT.md](HARMONIZATION_PROMPT.md) für bewusste inhaltliche Projektabstimmung und [RETROSPECTIVE_PROMPT.md](RETROSPECTIVE_PROMPT.md) für eine separate Auswertung der Maintainer-Agent-Zusammenarbeit.

## Git-Index und geschützte Git-Aktionen

Der Maintainer kontrolliert die Git-Historie. Assistants dürfen Status, Diffs und Logs prüfen sowie Working-Tree-Änderungen und Commit-Metadaten vorbereiten.

Staging und Unstaging sind Indexoperationen. Sie benötigen kein Kontrollwort, dürfen aber nur nach einer konkreten Maintainer-Anweisung oder Autorisierung des zugehörigen Commits erfolgen. Bestehende Staging-Auswahlen und nicht zusammenhängende Änderungen müssen erhalten bleiben.

Geschützte Aktionen umfassen Commits, Amendments, Tags, Pushes, Pulls, Merges, Rebases, Resets, Branch-Wechsel, Stash-Manipulationen und andere Operationen an der Git-Historie. Ein Assistant darf eine bestimmte geschützte Aktion nur ausführen, wenn die Anweisung für genau diese Aktion `explicit` oder `explicitly` auf Englisch oder die deutsche Wortfamilie `explizit` enthält. Die Freigabe von Dateiänderungen autorisiert keine Änderung der Git-Historie; die Freigabe einer geschützten Aktion autorisiert keine andere.

Reguläre Arbeits-Commits verwenden Conventional-Commit-Präfixe wie `feat:`, `fix:`, `docs:` oder `chore:`. Milestone-Commits verzichten auf das Präfix, verwenden eine lesbare Zusammenfassung mit abgeschlossener Version und schließen bereits geprüfte Arbeit ab.

## Decision Records

Decision Records bewahren, warum folgenreiche Entscheidungen getroffen wurden. Wähle das Präfix nach dem Entscheidungsgegenstand, nicht nur nach dem Repository-Typ:

- **PDR — Project Decision Record:** Projektrichtung, Umfang, Roadmap, Zusammenarbeit, Governance, Datenschutzgrenzen, Review-Modelle oder Repository-Beziehungen.
- **ADR — Architecture Decision Record:** technische Architektur, Tooling, Formate, Automatisierung oder eine andere dauerhafte technische Struktur in einem abgeleiteten Projekt.
- **DDR — Documentation Decision Record:** Dokumentationsstruktur, Terminologie, zielgruppenorientiertes Material, Veröffentlichungsregeln oder Dokumentations-QA.

Das generische Template verwendet standardmäßig PDRs und erklärt das Modell in [DECISIONS.md](DECISIONS.md). Verwende [decisions/](decisions/) nur für Entscheidungen, deren Begründung für zukünftige Mitwirkende relevant bleibt; kleine Routineentscheidungen benötigen keinen Record.

## Repository-Struktur

### Einstiegspunkte und Projektgedächtnis

- **`README.md` und `README.de.md`** führen auf Englisch und Deutsch in das Projekt ein, erklären den Einstieg und verlinken die vertiefenden Regeln.
- **`PROJECT_CONTEXT.md`** ist der primäre Wiedereinstiegspunkt. Die Datei hält aktuelle Intention, Status, Roadmap, Baseline, Validierungsstand, offene Entscheidungen und den nächsten sinnvollen Schritt fest, statt die vollständige Projekthistorie zu duplizieren.
- **`CHANGELOG.md` und `VERSION`** beschreiben abgeschlossene Zustände und die Versionshistorie. Sie werden aktualisiert, wenn ein versionierter Milestone abgeschlossen ist, nicht bereits bei Arbeitsbeginn.

### Zusammenarbeit und Betriebsregeln

- **`AGENTS.md`** ist der kompakte, automatisch geladene Einstiegspunkt für KI-Agenten. Die Datei verweist auf die vollständigen Kollaborations-, Betriebs-, Projekt- und Validierungsleitlinien, ohne sie zu duplizieren.
- **`ChatGPT.md`** definiert das allgemeine Kollaborationsmodell, Autoritätsgrenzen und den Arbeitsrhythmus zwischen Maintainer und Agent. Es ist transparente Projektdokumentation und kein versteckter Prompt.
- **`CODEX.md`** definiert lokale Ausführungs-, Netzwerk-, Offenlegungs- und Git-Regeln für Codex. Behalte die Datei bei lokaler Codex-Arbeit und passe sie nur für bewusste projektspezifische Anforderungen an.
- **`PHILOSOPHY.md`** hält die Werte hinter der Projektmethode fest, darunter Intention vor Struktur, Nachvollziehbarkeit, leichtgewichtiger Prozess und Integrität vor Außendarstellung.

### Setup, Fortsetzung und Review

- **`PROJECT_SETUP.md` und `INITIAL_PROMPT.md`** leiten die erste Initialisierung an und bewahren ihre methodische Provenienz. Abgeleitete Projekte behalten normalerweise beide Dateien und dokumentieren ihren Lebenszyklusstatus in `PROJECT_CONTEXT.md`.
- **`CONTINUATION_PROMPT.md`** definiert die geordnete Wiedereinstiegsprüfung für ein späteres Kontextfenster oder eine Assistant-Sitzung. Der Prompt gleicht vor substanzieller Arbeit den Projektkontext mit schreibgeschützten Git-Nachweisen ab.
- **`HARMONIZATION_PROMPT.md`** gleicht Projektinhalt, interne Dokumentation und Roadmap mit der aufgezeichneten Template-Baseline ab. Der Prompt bewertet nicht die Qualität der Zusammenarbeit und kopiert Template-Änderungen nicht blind.
- **`RETROSPECTIVE_PROMPT.md`** bewertet die Maintainer-Agent-Zusammenarbeit in einem gewählten Zeitraum. Inhaltliche Auswirkungen gehen an eine spätere Harmonisierung, während übertragbare Prozessbefunde kontrollierte Template-Kandidaten bleiben.

### Repository-Leitlinien und Entscheidungen

- **`DOCUMENTATION.md`** definiert Dokumentrollen, die Trennung von aktuellem Zustand und Historie sowie Qualitätsanforderungen. Die Datei bleibt nach der Initialisierung eine laufende Projektregel.
- **`REPOSITORY.md`** definiert Repository-Organisation, Git-Konventionen, Quellen- und Output-Behandlung, Versionierung und repository-fertige Übergaben. Abgeleitete Projekte passen die Datei an ihren tatsächlichen Workflow an, statt sie als vorübergehendes Setup-Material zu behandeln.
- **`DECISIONS.md` und `decisions/`** erklären Decision Records und speichern dauerhafte Entscheidungsbegründungen. Das Template bietet wiederverwendbare PDR-Leitlinien und gegenstandsbezogene Record-Vorlagen.

### Optionale Arbeitsordner

- **`input/`** enthält vom Maintainer bereitgestelltes Material, wenn das Projekt lokale Eingaben benötigt. Private, vertrauliche, lizenzierte oder personenbezogene Rohmaterialien benötigen vor Einsicht oder Git-Aufnahme eine Zugriffs- und Versionierungsentscheidung.
- **`references/`** enthält Quellen, Referenzen oder geprüfte Quellnotizen. Projekte sollten Provenienz, Lizenzierung und Sensitivität dokumentieren, wenn diese die Nutzung beeinflussen.
- **`notes/`** enthält Arbeitsnotizen und offene Fragen, die für das Projekt nützlich, aber noch keine dauerhaften Entscheidungen oder Deliverables sind.
- **`output/`** enthält Projekt-Deliverables oder erzeugte Ergebnisse. Projekte legen fest, ob Outputs versionierte Milestones, Review-Artefakte oder reproduzierbare lokale Produkte sind, und prüfen sie vor der Weitergabe.

## Template- und abgeleitete Projektdateien

In einem abgeleiteten Projekt:

- fülle `PROJECT_CONTEXT.md` aus und pflege sie als aktuellen Projektzustand;
- passe beide README-Dateien, `DOCUMENTATION.md` und `REPOSITORY.md` an das konkrete Projekt an;
- behalte und passe `AGENTS.md`, `ChatGPT.md`, `CODEX.md` und `PHILOSOPHY.md` an, sofern kein dokumentierter Projektbedarf eine Änderung erfordert;
- behalte `PROJECT_SETUP.md` und `INITIAL_PROMPT.md` als Initialisierungsprovenienz;
- behalte die Prompts für Fortsetzung, Harmonisierung und Retrospektive zur wiederholbaren späteren Nutzung;
- passe optionale Arbeitsordner nur an oder entferne sie nur, wenn ihre Rolle verstanden ist;
- ersetze Template-Decision-Records nur dann durch echte Records, wenn folgenreiche Entscheidungen vorliegen.

Halte Source-Template-Version und -Commit, Initialisierungsstatus, letzte Harmonisierungs-Baseline und beabsichtigte Abweichungen in `PROJECT_CONTEXT.md` fest. Ein abgeleitetes Projekt ist für seine eigene Intention und akzeptierten Entscheidungen maßgeblich; Template-Updates werden geprüft und angepasst statt blind kopiert.

## Verwendung dieses Templates

1. Erzeuge ein Repository aus dem Template und gib dem Agenten die Anweisung aus `INITIAL_PROMPT.md`.
2. Beantworte die nummerierten Fragen des Agenten; der Agent liest und verwendet die übrigen Setup-Dateien automatisch.
3. Prüfe den initialisierten Repository-Zustand, die Validierungsergebnisse und den vorgeschlagenen ersten Commit.
4. Lasse den Agenten `PROJECT_CONTEXT.md` während der späteren Arbeit als kompakte Projektübergabe aktuell halten.
5. Arbeite in kleinen Artefakten oder Änderungen, die aus der vom Maintainer definierten Intention, Grenzen und Erfolgskriterien abgeleitet sind.
6. Unterscheide Rohinputs, geprüfte Derivate und erzeugte Outputs, bevor Zugriff, Versionierung oder Veröffentlichung freigegeben werden.
7. Dokumentiere folgenreiche Entscheidungen in `decisions/` und validiere Ergebnisse, bevor sie als abgeschlossen dargestellt werden.
8. Beginne spätere Sitzungen mit `CONTINUATION_PROMPT.md`; der Agent rekonstruiert den aktuellen Zustand, ohne die Initialisierung zu wiederholen.
9. Nutze Harmonisierung, wenn Projektinhalt oder Template-Abgleich bewusst geprüft werden müssen, und eine Retrospektive separat zur Bewertung der Zusammenarbeit.
10. Schließe Milestones mit kohärentem Kontext, Dokumentation, Changelog und Versionsmetadaten ab.

## Tool-Setup für Maintainer

Das generische Template hat keine verpflichtende domänenspezifische Toolchain. Eine praktische lokale Baseline ist:

- [Git](https://git-scm.com/downloads) und ein vom Maintainer kontrollierter Client wie [GitHub Desktop](https://desktop.github.com/download/);
- ein Text- oder Markdown-Editor wie [Visual Studio Code](https://code.visualstudio.com/download);
- [PowerShell](https://learn.microsoft.com/powershell/scripting/install/installing-powershell-on-windows) unter Windows oder eine gleichwertige lokale Shell;
- [ripgrep (`rg`)](https://github.com/BurntSushi/ripgrep/releases) oder ein anderes schnelles Suchwerkzeug;
- projektspezifische Werkzeuge, die nur installiert werden, wenn die konkrete Arbeit sie benötigt.

Bevorzuge projektlokale Umgebungen wie `.venv/` oder `node_modules/` gegenüber globalen Änderungen. Paketinstallationen, externe Dienste und Netzwerknutzung sollten einen klaren Projektzweck haben; private Repository-Materialien bleiben standardmäßig lokal.

## Kontinuierliche Verbesserung

Nutze Harmonisierung, um ein konkretes Projekt intern konsistent und mit relevanten Template-Entwicklungen abgestimmt zu halten. Nutze Retrospektiven separat, um Kollaborationspraktiken, Übergaben, Entscheidungsfindung und Arbeitsrhythmus zu bewerten. Gemischte Projekte können sowohl generische Verbesserungen als auch Hinweise darauf liefern, dass ein stärker spezialisiertes Template langfristig besser geeignet ist.

Behandle Beobachtungen aus einem abgeleiteten Projekt als Kandidaten und nicht als automatische Template-Regeln. Prüfe, ob sie wiederholt auftreten, außerhalb ihres ursprünglichen Kontexts nützlich bleiben und in das generische Template oder eine Domänenspezialisierung gehören. Abgeleitete Projekte und ihre Decision Records bleiben für projektspezifische Entscheidungen maßgeblich.

Der Maintainer koordiniert die templateübergreifende Weiterentwicklung in einem privaten Governance-Repository namens `agit-templateverse`. Es dokumentiert gemeinsame Konventionen, bewusste Spezialisierungen und Evidenz aus abgeleiteten Projekten. Das Repository wird bewusst nicht verlinkt, da Template-Nutzer:innen keinen Zugriff darauf benötigen.

Die Governance-Koordination erzeugt keine verborgenen Anforderungen. Jede Änderung, die dieses Template betrifft, muss hier durch gepflegte Leitlinien, gegebenenfalls Decision Records, den Changelog und die Release-Historie abgebildet werden. Template-Änderungen sollen betroffene Dokumente kohärent aktualisieren, statt isolierte Notizen anzuhängen.

## Lizenz

Dieses Projekt steht unter der [MIT-Lizenz](LICENSE).
