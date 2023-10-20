class: center, middle

## [Software Engineering](../../praesentationen.html)

#### Kapitel 3

# Inhaltsverzeichnis

- Version control systems / Source code management
- AI-driven development
- Code reading
- Bug report writing
- Debugging
- Agile testing workflows
- Pair programming
- Code reviews
- Refactoring
- Refactoring Patterns
- Tools
- Quellen

## Version Control, auch als Quellcodeverwaltung bezeichnet

- Praxis, Änderungen am Software-Code zu verfolgen und zu verwalten.
- Hilft Software-Teams in beschleunigten Entwicklungsumgebungen.
- Vorteilhaft für DevOps-Teams zur Verkürzung der Entwicklungszeit.
- Ermöglicht Fehlerbehebung durch Zurückgreifen auf frühere Code-Versionen.
- Effiziente Workflow-Verwaltung.
[1]
---

## Centralized vs Distributed Version Control

- Zentralisierte Kontrolle: Abhängig von einem zentralen Server, einfach einzurichten.
- Nachteile: Einzelner Serverausfall, Schwierigkeiten beim Merging und Branching.
- Verteilte Kontrolle: Bietet multiple Backups, Offline-Commits und schnelles Branching.
- Git ist ein bekanntes Beispiel für verteilte Versionskontrolle.
[2]
---

## Git

- Weitverbreitetes modernes Versionskontrollsystem.
- Entwickelt von Linus Torvalds, dem Schöpfer des Linux-Kernels.
- Verteilungsarchitektur ermöglicht vollständige Historie der Änderungen in Arbeitskopien.
- Schwerpunkt auf Leistung, Sicherheit und Flexibilität.
[3]
---

## Remote Repositories

- Versionen des Projekts, im Internet oder Netzwerk gehostet.
- Schreibgeschützt oder schreibgeschützt.
- Verwaltung von remote Repositories: Hinzufügen, Entfernen, Verwalten von Branches, Definition als tracked/untracked.
[4]
---

## Visualisierung von relevanten git-Kommandos und -Workflows

- `git commit`: Aktuelle Änderungen im Arbeitsverzeichnis in das lokale Repository aufnehmen.
- `git branch`: Listet vorhandene Branches auf und zeigt den aktuellen Branch an.
- `git checkout`: Wechseln zwischen Branches oder Wiederherstellen von Commits/Dateiversionen.
- `git checkout -b`: Erstellen und Wechseln zu einem neuen Branch.
- `git reset`: Rückgängig Machen von Commits, indem der HEAD/Branch auf einen früheren Commit zurückgesetzt wird.
- `git revert`: Erzeugt neuen Commit, um Änderungen eines früheren Commits rückgängig zu machen.
- `git merge`: Integriert Änderungen aus einem Branch in den aktuellen Branch.
- `git rebase`: Neuorganisation der Commit-Historie durch Anwenden von Commits aus einem Branch auf einen anderen.
- `git fetch`: Herunterladen neuer Änderungen aus einem entfernten Repository.
- `git pull`: Kombiniert `git fetch` und `git merge`, um Änderungen aus einem entfernten Repository in den lokalen Branch zu integrieren.
- `git push`: Hochladen lokaler Commits in ein entferntes Repository.
- `git tag`: Erstellen von Tags zur Markierung bestimmter Commit-Versionen in der Historie.
[5] [6]
---

## Sequenzdiagramm für git data transfer commands

- ![](media\git-transport.jpg) [7]

---
## Multirepos vs. Monorepos

Beide Ansätze, Monorepo und Multi-Repo, zielen darauf ab, Code effizient zu verwalten, aber ihr Hauptunterschied liegt im Zeitpunkt, zu dem Entscheidungen getroffen werden. Bei Multi-Repo werden Bibliotheken unabhängig voneinander verwaltet, was es Teams ermöglicht, schnell zu arbeiten, jedoch auf Kosten möglicher Divergenz. In einem Monorepo müssen Teams zusammenarbeiten und alle Bibliotheken gleichzeitig anpassen, um Konflikte zu vermeiden, was die Geschwindigkeit beeinträchtigen kann, aber die Code-Konsistenz gewährleistet. Monorepo fördert eine Kultur der Achtsamkeit, während Multi-Repo eine Kultur des schnellen Fortschritts begünstigt. [8]

---

### Submodules

Git-Submodule ermöglichen es, ein Git-Repository als Unterverzeichnis eines anderen Git-Repositorys zu behalten. Git-Submodule sind einfach eine Referenz auf ein anderes Repository zu einem bestimmten Zeitpunkt. Sie ermöglichen einem Git-Repository, die Versionshistorie von externem Code einzubeziehen und zu verfolgen. [9]

---

### Pull Requests

In ihrer einfachsten Form sind Pull Requests ein Mechanismus, mit dem ein Entwickler Teammitglieder darüber benachrichtigt, dass sie eine Funktion abgeschlossen haben. Sobald ihr Feature-Branch bereit ist, reicht der Entwickler über ihr Bitbucket-Konto einen Pull Request ein. Dies informiert alle Beteiligten darüber, dass sie den Code überprüfen und in den Haupt-Branch überführen müssen.

Aber der Pull Request ist mehr als nur eine Benachrichtigung - es handelt sich um ein dediziertes Forum zur Diskussion der vorgeschlagenen Funktion. Wenn es Probleme mit den Änderungen gibt, können Teammitglieder Feedback im Pull Request hinterlassen und die Funktion sogar durch das Einreichen. [10]

---
## Branching Strategies

Release Branching:
- Jede Veröffentlichung in einem eigenen Branch.
- Änderungen in Veröffentlichungs- und Haupt-Branch erforderlich.
- Kann zu erhöhtem Aufwand und Verwirrung führen.

Feature Branching:
- Features in eigenen Branches entwickelt und mit Feature Flags gesteuert.
- Ermöglicht schrittweise Bereitstellung und bessere Kontrolle.

Task Branching:
- Fokussiert auf Aufgabenverwaltung, erstellt Branch für jede Aufgabe.
- Transparente Zuordnung von Änderungen zu Aufgaben.
- Besonders für agile Entwicklung geeignet. [11]

---

### Git Flow

- "Master" (produktionsbereiter Code) und "develop" (neuester Code) Branches.
- Feature-, Release- und Hotfix-Branches.

### Github Flow

- Vereinfachte Version mit nur einem "main"-Branch.
- Feature-Branches werden nach Abschluss gemerged.

### Trunk-Based Development

- Ein einzelner "trunk"-Branch enthält aktuellen Code.
- Kurzlebige Feature-Branches, die zurückgemerged werden.

### Feature Branching

- Separater Branch für jede Funktion, Rückmerge nach Fertigstellung.

### Task Branching

- Ein Branch pro Aufgabe, Mergen nach Aufgabenabschluss.

### Clear Framework Branching

- Festgelegte Regeln und Workflows für Features, Releases und Bugfixes. Erfordert hohe Koordination. [12]

---

### Trunk-based Development

- Kleine, häufige Updates direkt im Haupt-Branch integriert.
- Beschleunigt Integration und ermöglicht CI/CD.
- Steigert Softwareauslieferung und Leistung.
- Unterschied zum strengeren Gitflow-Modell, das Änderungen im Hauptcode begrenzt.
[13]
---

### Long-lived Branches

- Separate Branches für neue Funktionen oder größere Änderungen.
- Unabhängig von Hauptentwicklungslinie, über längere Zeiträume gepflegt.
- Gemerged nach Überprüfung und Konfliktlösung.
- In Open-Source-Software verbreitet, bei fehlendem Zugriff auf die Hauptlinie.
- Dauer hängt von Aktivität im Code ab, nicht von Kalenderzeit. [14]

---
## Git Flow

- Beliebte Branching-Strategie.
- Enthält "master"-Branch (produktionsbereiter Code) und "develop"-Branch (neuester Code).
- Feature-Branches für spezifische Funktionen, die zurück in "develop" gemerged werden.
- Release-Branches und Hotfix-Branches für Veröffentlichungen und Fehlerkorrekturen. [12]

---

### Feature, develop, release, hotfix und master branch

- Feature Branch: Abzweigung vom develop-Branch für neue Funktionen. Wird zurück in den develop-Branch gemerged.
- Develop Branch: Hauptentwicklungs-Branch, von dem Feature-Branches abgezweigt und zurückgeführt werden.
- Release Branch: Vorbereitung auf Veröffentlichung, Abzweigung vom develop-Branch und Rückführung in develop und master.
- Hotfix Branch: Entwicklung von Hotfix, Abzweigung vom master-Branch und Rückführung in develop und master.
- Master Branch: Haupt-Branch, von dem Release-Branches abgezweigen und zurückgeführt werden. [0]

---

### Github Flow

- Vereinfachte Version von Git Flow.
- Ein einziger langfristiger "main"-Branch (produktionsbereiter Code).
- Feature-Branches für spezifische Funktionen, die zurück in "main" gemerged werden.
- Keine Release-Branches oder Hotfix-Branches. [12]

---
## Merging Strategies

- Ein Merge in Git tritt auf, wenn zwei Branches kombiniert werden.
- Git sucht nach einem gemeinsamen Basis-Commit zwischen diesen Branches und erstellt dann einen Merge-Commit.
- Die Auswahl der Merge-Strategie erfolgt in der Regel automatisch, basierend auf den gegebenen Branches. [15]

---

### Merge Commit

- Beim Mergen von Commits in einem Pull Request auf GitHub.com werden alle Commits aus dem Featurebranch in den Basisbranch in einem zusätzlichen Merge-Commit zusammengeführt.
- Standardmäßig mit der --no-ff-Option.
- Schreibberechtigungen im Repository erforderlich.
- Diagramm zeigt den Standardablauf für Merge- und Commitvorgänge. [16]

### Squash and Merge

- Beim Squashen und Mergen von Commits in einem GitHub-Pull Request werden alle einzelnen Commits zu einem einzigen zusammengefasst und in den Hauptbranch integriert.
- Schreibberechtigungen und Einstellung zur Unterstützung des Squash-Mergens erforderlich.
- Schafft einen sauberen Git-Verlauf.
- Diagramm zeigt den Prozess des Commit-Squashings. [16]

### Rebase and Merge

- "Rebase und Merge" ermöglicht das Hinzufügen von Commits aus einem Feature-Branch einzeln und ohne einen separaten Merge-Commit in den Haupt-Branch.
- Führt zu einem linearen Projektverlauf.
- Unterschiedliches Verhalten von "Rebase und Merge" auf GitHub im Vergleich zu "git rebase" außerhalb von GitHub.
- Schreibberechtigungen und aktivierte Option "Rebase und Merge" im Repository erforderlich.
- Fälle, in denen automatisches "Rebase und Merge" auf GitHub.com nicht möglich ist, erfordern manuelles Rebase in der Befehlszeile. [16]

---
## Aufbau und Inhalt von Commit Messages

Commit-Nachrichten sollten bestimmten Richtlinien folgen:

- Eine kurze Zusammenfassung (maximal 72 Zeichen) und ein detaillierter erläuternder Text (maximal 72 Zeichen pro Zeile).

- Eine leere Zeile, die die Zusammenfassung vom Haupttext trennt, es sei denn, der Haupttext fehlt.

- Die erste Zeile ist die wichtigste und sollte den Satz "Wenn angewandt, wird dieser Commit <Ihre Betreffzeile hier>" vervollständigen. Die Betreffzeile sollte großgeschrieben und im Imperativ geschrieben sein.

- Beschreibung des Ziels oder des Grundes für die Änderung in klarem Englisch mit einem Präfix, das auf die Komponente oder die Aufgaben-ID hinweist.

- Wenn sich der Commit auf ein Problem bezieht, sollte dies in der Nachricht vermerkt werden.

- Kein Punkt am Ende der Nachricht, und jede Absatz sollte großgeschrieben sein.

- Keine patchset-spezifischen Kommentare und keine Beschreibung eventueller Einschränkungen des aktuellen Codes.

- Weitere Absätze sollten nach leeren Zeilen folgen; Aufzählungspunkte sind in Ordnung.

- Konsistente Wortwahl zur Beschreibung von Änderungen ist wichtig.

- Commit-Nachrichten-Linting kann konfiguriert werden, um Standards durchzusetzen und mit semantischer Versionierung übereinzustimmen.

Das Schreiben guter Commit-Nachrichten erleichtert die Kommunikation und Zusammenarbeit im Team. [17]

---
## AI-driven development

---

### Conversational AI vs. Generative AI

- Conversational AI-Systeme sind auf die Kommunikation mit Benutzern spezialisiert und werden auf kleineren Dialogdatensätzen trainiert.
- Ihr Hauptzweck ist die Interaktion zwischen Menschen und Maschinen, wobei die Generierung von Antworten nur ein Nebenprodukt ist.

- Generative KI-Tools sind darauf ausgerichtet, originale Inhalte zu erstellen und lernen aus Datenmustern.
- Ihr Hauptzweck ist die Generierung von einzigartigem Inhalt in verschiedenen Formaten, während die Kommunikation mit Benutzern nicht ihre Hauptfunktion ist.

Generative KI ist flexibler und vielseitiger in Bezug auf die Art des erstellten Inhalts. [18]

---

### Prompt engineering

Prompt Engineering ist der Prozess der Erstellung von Prompts, die die gewünschten Ergebnisse erzielen.
Es ist ein iterativer Prozess, der die Erstellung, das Testen und die Anpassung von Prompts umfasst, um die gewünschten Ergebnisse zu erzielen. [0]

---

### ChatGPT, Github Copilot

- ChatGPT ist ein leistungsstarkes KI-Modell von OpenAI, das menschenähnlichen Text auf natürliche Weise generieren kann.
- Es ist ein nützliches Werkzeug für die Texterstellung, Recherche und Unterstützung bei einer Vielzahl von Aufgaben.

- GitHub Copilot ist eine Erweiterung für Visual Studio Code, die von GitHub in Zusammenarbeit mit OpenAI entwickelt wurde.
- Sie bietet Unterstützung für Entwickler, indem sie intelligente Code-Vervollständigungen, -vorschläge und -dokumentationen bietet.
- GitHub Copilot ist ein wertvolles Werkzeug für die Softwareentwicklung und kann die Produktivität von Entwicklern erheblich steigern. [0]

---

### Best Practices für "Googling"

1. Verwenden Sie Anführungszeichen, um nach exakten Phrasen oder Namen zu suchen.

2. Schließen Sie bestimmte Wörter aus, indem Sie das Minuszeichen verwenden.

3. Mit "OR" können Sie nach einem von zwei Begriffen suchen.

4. Verwenden Sie die Tilde (~) für Synonyme in der Suche.

5. Nutzen Sie "site:" gefolgt von einer Domain, um innerhalb einer bestimmten Website zu suchen.

6. Das Sternchen (*) dient als Platzhalter für Wörter oder Teile von Wörtern.

7. Suchen Sie nach Ergebnissen in einem bestimmten Wertebereich mit "..".

8. Suchen Sie gezielt im Text, im Titel oder in der URL einer Seite mit Qualifikatoren wie "inurl:", "intext:" und "intitle:".

9. Finden Sie ähnliche Websites mit dem "related:"-Qualifikator.

10. Kombinieren Sie diese Techniken nach Bedarf, um Ihre Suche zu verfeinern.

Diese Tipps helfen, genauere und relevantere Suchergebnisse zu erzielen. [19]

---

# Code reading

---
# Wie liest man Code effektiv?

- Aktionskette folgen
- Wiederholung des Prozesses
- Qualität zählt
- Eigene Fähigkeiten verbessern
- Expertenwissen erlangen
- Zeitlicher Verlauf
- Empfehlungen
- Kontinuierliches Lernen [1]
---

# Bug report writing

---

# Best Practices für Bug reports

## Ziel
- Fehlerbericht soll Entwicklern und Management helfen, das Problem zu verstehen. [2]

---
## Richtlinien

1. **Alle relevanten Informationen bereitstellen:**
   - Verwenden einfacher Sätze.
   - Fehler melden als Fertigkeit.

2. **Reproduzierbare Fehler melden:**
   - Schritte zur Fehlerreproduktion angeben.
   - Alle Voraussetzungen und Testdaten hinzufügen.

3. **Prägnanz und Klarheit:**
   - Kurze, umfassende Problembeschreibung.
   - Vermeiden langer Beschreibungen. [2]
---

4. **Fehler frühzeitig melden:**
   - Schnelle Fehlermeldung für frühe Behebung.

5. **Vermeidung von Rechtschreib- und Sprachfehlern:**
   - Sorgfältiges Korrekturlesen.
   - Verwenden von Tools bei Bedarf.

6. **Dokumentation zeitweiliger Probleme:**
   - Videoaufzeichnungen bei nicht reproduzierbaren Fehlern.

7. **Vermeidung von Wiederholung von Fehlern:**
   - Sicherstellen, dass keine doppelten Fehler gemeldet werden. [2]

---

8. **Separate Fehler für nicht zusammenhängende Probleme:**
   - Bei verschiedenen Problemen separate Meldungen.

9. **Vermeidung autoritativen Tons:**
   - Höfliche und respektvolle Dokumentation.

Ein detaillierter und präziser Fehlerbericht ermöglicht schnellere und effektivere Fehlerbehebung. [2]

---

# Debugging

---

# Definiton

Debugging ist der Prozess der Identifizierung, Lokalisierung und Behebung von Fehlern, Fehlfunktionen oder Problemen in einer Softwareanwendung oder einem Programmcode. [3]

---

# Problem Solving

## Definition
- Allgemeiner Prozess zur Identifikation, Analyse und Lösung von Problemen und Herausforderungen.

## Ziel
- Nachhaltige Lösungen finden und Wiederholung der Probleme verhindern.

## Methoden
- Unterschiedliche Techniken: z. B. Ursachenanalyse (Root Cause Analysis), Lösungsentwicklung, Implementierung von Änderungen und Überwachung der Wirksamkeit. [3]
---

## Herausforderungen
- Genaue Problemidentifikation.
- Suche nach geeigneten Lösungen.
- Sicherstellung der Effektivität und Langfristigkeit der Lösung.

## Rolle in der Softwareentwicklung
- Entwickler und IT-Fachleute setzen Problem Solving ein.
- Unterscheidung von Debugging: Behebung von Softwarefehlern.
- Wesentlicher Bestandteil des Entwicklungsprozesses für hochwertige und zuverlässige Software.

Problem Solving ist der Schlüssel zur Bewältigung von Herausforderungen in verschiedenen Kontexten. [3]
---
# Root Cause Analysis (RCA)

## Definition
- Prozess zur Identifizierung der grundlegenden Ursache eines Problems, nicht nur seiner Symptome. [4]
---
## Schritte zur erfolgreichen RCA

1 . Definition des Problems
   - Klar definieren, welches Problem gelöst werden muss.

2 . Problemreproduktion
   - Problem in kontrollierter Umgebung reproduzieren, um Ursachen einzugrenzen.

3 . Code-Analyse
   - Programmcode überprüfen, um mögliche Fehler oder Probleme zu identifizieren.[4]
---
4 . Testen und Debuggen
   - Verwendung von Test- und Debugging-Tools, schrittweises Durchgehen des Codes, Ausführen von Testfällen.

5 . Überprüfen von Fehlermeldungen und Protokollen
   - Relevante Fehlermeldungen und Protokolle auf Hinweise zur Wurzelursache prüfen.

6 . Konsultation von Kollegen
   - Austausch mit erfahrenen Kollegen oder Programmierern zur Wurzelursache. [4]
---
7 . Lösungsentwicklung
   - Entwicklung einer Lösung, sei es durch Codeänderungen oder neue Prozesse.

8 . Lösungstest und Validierung
   - Testen der Lösung, um Effektivität und Vermeidung neuer Probleme sicherzustellen.

9 . Dokumentation der Ergebnisse
   - Dokumentieren der identifizierten Wurzelursache und der implementierten Lösung. [4]
---
## Kommunikation
- Wichtige Stakeholder informieren, z. B. Management, Kunden, Aufsichtsbehörden.

## Vorteile
- Verbesserte Problemlösung, Effizienzsteigerung, Qualitätsverbesserung des Codes, Risikoreduzierung.

## Nachteile
- Zeitintensiver Prozess, zusätzlicher Ressourcenbedarf, Komplexität der Probleme.

RCA ist entscheidend, um langfristige Lösungen zu finden und die Qualität von Software und Prozessen zu verbessern. [4]
---
# Debugging vs. Testen in der Softwareentwicklung

## Testen:
- Sicherstellen, dass Software den festgelegten Anforderungen entspricht.
- Fehler frühzeitig im Entwicklungsprozess aufdecken.
- Kann von Entwicklern, Testern und Endbenutzern durchgeführt werden.
- Nutzt Testautomatisierungs- und Testmanagement-Tools.
- Beginnt nach Abschluss der Softwareentwicklung. [5]
---
## Debugging:
- Reaktiver Prozess zum Finden und Beheben von Fehlern im existierenden Code.
- Startet, sobald Fehler während des Testvorgangs erkannt werden.
- Aufgabe der Entwickler.
- Verwendet Debugger, Profiler und andere Debugging-Tools.
- Konzentriert sich auf die Identifizierung und Behebung von Fehlern in existierendem Code.

## Zusammenfassung:
- Testen: Verhinderung von Qualitätsmängeln, frühzeitige Fehlererkennung.
- Debugging: Identifizierung und Behebung von Fehlern in existierendem Code.
- Beide Prozesse sind entscheidend für qualitativ hochwertige Softwareprodukte. [5]
---
# Rubber Duck Debugging

## Was ist Rubber Duck Debugging?
- Humorvoller und effektiver Ansatz zur Problemlösung in der Softwareentwicklung.

## Wie funktioniert es?
1. Beschaffen Sie sich eine Badeente (Badewannenversion).
2. Stellen Sie die Gummiente auf Ihren Schreibtisch.
3. Erklären Sie der Ente, dass Sie beabsichtigen, Ihren Code mit ihrer Hilfe zu durchgehen.
4. Beginnen Sie damit, der Ente zu erklären, was Ihr Code tun soll.
5. Gehen Sie detailliert vor und erläutern Sie Ihren Code Zeile für Zeile. [6]
---
## Warum ist es effektiv?
- Das Erklären des Codes laut hilft Entwicklern, festgefahrene Gedanken zu klären und Codierfehler zu finden.
- Oft stellt man während des Erklärungsprozesses fest, dass man sich vertan hat oder das, was man tut, nicht dem entspricht, was beabsichtigt war.

## Hinweis
- Wenn nötig, kann ein Kollege die Ente ersetzen, aber oft ist es effektiver, die Ente um Hilfe zu bitten, bevor Sie Kollegen involvieren.

## Fazit
- Die Methode des "Rubber Duck Debugging" mag amüsant erscheinen, hat sich jedoch als nützliche Möglichkeit erwiesen, um Codierfehler zu finden und Lösungen zu entwickeln, selbst wenn der Gesprächspartner nur aus Kunststoff ist.[6]
---
# Timetravel-Debugging (Reverse Debugging)

## Was ist Zeitreise-Debugging?
- Ermöglicht die Aufzeichnung und Navigation der gesamten Aktivitäten eines laufenden Programms rückwärts und vorwärts.

## Vorteile gegenüber herkömmlichen Debuggern
- Besonders geeignet für schwer reproduzierbare Fehler und große Anwendungen.
- Herkömmliche Debugger unterstützen nur Vorwärts-Debugging.

## Wie funktioniert es?
1. Aufzeichnung der Programmausführung, einschließlich Fehler und Ereignisse.
2. Möglichkeit, rückwärts durch die Aufzeichnung zu navigieren, um die Fehlerursache an verschiedenen Stellen des Programms zu finden. [7]
---
## Leistung und Verlangsamung
- Das Zeitreise-Debugging kann die Leistung beeinträchtigen, abhängig vom verwendeten Zeitreise-Debugger.

## Unterstützung in verschiedenen Programmiersprachen
- Prinzipiell in allen Programmiersprachen möglich.
- Unterstützung in GDB-kompatiblen Sprachen wie C/C++, Go und Fortran.
- Spezielle Zeitreise-Debugging-Tools für andere Sprachen wie Python und JavaScript.

## Anwendungsbereiche
- Hilfreich zur effektiven Behebung schwerwiegender Fehler, insbesondere bei komplexen und schwer zu reproduzierenden Problemen. [7]
---
# Logging / Tracing

## Logging
- Grundlegendste Form der Anwendungsüberwachung.
- Identifiziert Vorfälle oder Fehler.
- Zeichnet zeitgestempelte Daten von Anwendungen oder Diensten regelmäßig auf.
- Verwendet Loggingebenen wie FATAL, ERROR, WARN, DEBUG, INFO, TRACE und ALL zur Filterung wichtiger Informationen.
- Oft unstrukturiert und erfordert spezielle Tools zur Analyse.

## Tracing
- Wichtig in modernen verteilten Softwarearchitekturen, wo viele Anwendungen miteinander interagieren.
- Zeichnet den Weg einer Anfrage von Anfang bis Ende auf, inklusive Interaktionen mit verschiedenen Diensten und Messung der Latenz.
- Versteht den Kontext einer Anfrage und analysiert Abweichungen vom normalen Verhalten. [8]

---
## Wann man Logging und Tracing verwenden sollte
- Logging ist unerlässlich für die tägliche Überwachung von Anwendungen, immer aktiviert, um Probleme zu identifizieren.
- Tracing hilfreich bei schneller Fehlerbehebung, sollte aber nicht kontinuierlich verwendet werden, da die Leistung beeinträchtigt werden kann.

## Empfehlung
- Effektive Observability-Strategie in verteilten Systemen sollte Platz für beides bieten, da sie unterschiedliche Zwecke erfüllen.
- Logging zur Überwachung und Identifikation von Problemen im täglichen Betrieb.
- Tracing für schnelle Fehlerbehebung und Zuordnung von Problemen zu spezifischen Anwendungen oder Diensten.

Eine ausgewogene Kombination von Logging und Tracing ist in verteilten Architekturen empfehlenswert. [8]
---
# Ablauf des Debuggings

## 1. Reproduktion des Problems
- Überprüfung der Schritte oder Bedingungen, die zum Fehler führen.
- Ziel: Sicherstellen, dass das Problem tatsächlich besteht.

## 2. Fehlererkennung
- Lokalisierung des fehlerhaften Codebereichs.
- Identifikation von Aktionen, die unerwünschtes Verhalten auslösen.

## 3. Code-Inspektion
- Sorgfältige Analyse des Codes.
- Durchsuchen des Quellcodes, Überprüfen von Variablenwerten, Identifizieren von Inkonsistenzen. [3]
---
## 4. Hypothesenbildung
- Aufstellen von Hypothesen basierend auf der Code-Analyse.
- Verwendung von logischem Denken und Erfahrung.

## 5. Testen von Hypothesen
- Überprüfung, ob Hypothesen den Fehler erklären.
- Hinzufügen von Debugging-Anweisungen, Code-Änderungen und erneutes Ausführen unter verschiedenen Bedingungen.

## 6. Schritt-für-Schritt-Debugging
- Durchgehen des Codes Zeile für Zeile.
- Verwendung von Debugging-Tools und Breakpoints.[3]
---
## 7. Überprüfung der Annahmen
- Kontinuierliche Prüfung der angenommenen Fehlerursachen.
- Sicherstellen, dass die Annahmen korrekt sind.

## 8. Korrekturen und Tests
- Anpassen des Codes, um den Fehler zu beheben.
- Erneutes Testen, um sicherzustellen, dass der Fehler behoben ist und keine neuen Probleme auftreten.

## 9. Dokumentation
- Protokollieren des gefundenen Fehlers, durchgeführte Änderungen und die Lösung.
- Wichtiger, oft übersehener Schritt. [3]
---
## 10. Verifikation und Validierung
- Gründliche Überprüfung und Validierung des behobenen Codes.
- Sicherstellen, dass der Fehler nicht erneut auftritt und keine neuen Probleme entstehen.

## 11. Rückmeldung und Berichterstattung
- Dokumentation des Debugging-Ergebnisses.
- Weitergabe von Informationen an das Entwicklungsteam oder Stakeholder.

Der Debugging-Prozess erfordert Geduld, analytisches Denken und Systematik. Debugging-Tools und -Techniken wie Breakpoints und Protokollierung sind hilfreich, um den Prozess effizient zu gestalten.[3]
---
# Beispiel Debugging

## Nullzeiger-Ausnahmen (NullPointerException)
- Problem: Das Programm stürzt ab, weil auf eine Variable oder ein Objekt zugegriffen wird, die/das den Wert "null" hat.
- Debugging: Setzen Sie Breakpoints und überprüfen Sie die Werte von Variablen, um den Ort zu identifizieren, an dem die Variable null ist. Stellen Sie sicher, dass die Variable ordnungsgemäß initialisiert wurde.

## Endlosschleifen
- Problem: Das Programm bleibt in einer Schleife stecken und führt den Code immer wieder aus.
- Debugging: Fügen Sie Breakpoints in der Schleife hinzu und verfolgen Sie den Fluss des Programms, um den Grund für die Endlosschleife zu finden. Überprüfen Sie die Bedingungen, die zum Beenden der Schleife führen sollen.[3]
---
## Falsche Ergebnisse bei Berechnungen
- Problem: Das Programm gibt unerwartete oder fehlerhafte Ergebnisse aus.
- Debugging: Verwenden Sie Debugging-Anweisungen, um Zwischenergebnisse anzuzeigen. Überprüfen Sie mathematische Berechnungen und Vergleiche, um sicherzustellen, dass sie korrekt sind.

## Fehlerhafte Benutzereingaben
- Problem: Das Programm akzeptiert Benutzereingaben, die ungültig oder unerwartet sind.
- Debugging: Überwachen und validieren Sie Benutzereingaben. Verwenden Sie Protokollierung, um Eingaben und Verarbeitungsschritte nachzuverfolgen.[3]
---
## Fehler in Schleifen und Bedingungen
- Problem: Schleifen oder bedingte Anweisungen verhalten sich nicht wie erwartet.
- Debugging: Setzen Sie Breakpoints innerhalb der Schleifen oder vor bedingten Anweisungen, um den Code schrittweise auszuführen. Überprüfen Sie die Werte von Schleifenvariablen und Bedingungen.

## Fehler in Multithreading-Anwendungen
- Problem: In einer Anwendung mit mehreren Threads treten unvorhersehbare Wettlaufbedingungen oder Deadlocks auf.
- Debugging: Verwenden Sie spezielle Debugging-Tools für Multithreading, um den Zustand der Threads zu überwachen und Probleme in der Koordination zu identifizieren.[3]
---
## Fehler in der Benutzeroberfläche (UI)
- Problem: Die Benutzeroberfläche verhält sich fehlerhaft oder zeigt unerwartete Anzeigeelemente.
- Debugging: Überprüfen Sie das UI-Code-Teil und setzen Sie Breakpoints, um den Programmfluss zu verfolgen. Stellen Sie sicher, dass Ereignishandler korrekt konfiguriert sind.

## Probleme in der Datenbankkommunikation
- Problem: Das Programm kann keine Verbindung zur Datenbank herstellen oder erhält falsche Daten.
- Debugging: Überprüfen Sie die Datenbankverbindungsparameter und Protokolle. Verwenden Sie SQL-Abfrage-Protokollierung, um Datenbankinteraktionen nachzuverfolgen.

Diese Beispiele veranschaulichen typische Situationen, in denen Debugging notwendig ist. Die Wahl der Debugging-Tools und -Techniken hängt von der Programmiersprache, der Entwicklungsplattform und der Art des Problems ab. Ein systematischer Ansatz, bei dem Sie schrittweise den Code durchgehen und wichtige Variablen und Zustände überwachen, ist in den meisten Fällen hilfreich. [3]
---
# Debugging Werkzeuge

## Trace32 von Lauterbach
- Hardware- und Software-Tools
- Modulares Konzept mit universellen Basismodulen und architekturspezifischen Kabeln
- "PowerDebug PRO" für verschiedene Architekturen mit USB-3.0- und GbE-Anschlüssen
- Umfassende Analyse des Programmablaufs

## ULINKplus von Arm Keil
- Debugger, Leistungsmessgerät und I/O-Schnittstelle in einem
- Einblicke in Funktion, Timing und Leistungsaufnahme von Embedded-Anwendungen
- Anschluss an Arm-Cortex-basierte Geräte
- Funktionen wie SWV-Trace und Multi-Core-Debugging [9]
---
## J-Link von Segger
- Hardware-Debugger mit hoher RAM-Download-Geschwindigkeit (3 Mbyte/s)
- Unbegrenzte Anzahl von Breakpoints im Flash-Speicher von MCUs
- Kompatibilität mit verschiedenen CPUs und Architekturen
- Software-Tools wie Embedded Studio, System View und Ozone

## Universal Debug Engine (UDE) von PLS Programmierbare Logik & Systeme
- Software-Tool für Systemanalyse, Tests und Debugging von High-End-SoCs und Multicore-Systemen
- Darstellung von Systemzuständen, Setzen von Breakpoints und Laufzeitanalyse
- Unterstützung für verschiedene Architekturen
- Funktionen wie Trace, Profiling und Code-Coverage-Analyse

Diese Tools unterstützen, Softwarefehler zu finden, zu isolieren und zu beheben, um sicherzustellen, dass ihre Software einwandfrei funktioniert. Sie bieten vielfältige Funktionen, darunter Hardware-Debugging und Software-Simulation, abhängig von den Projektanforderungen.[9]
---
# Agile testing workflows
---
## Agile testing workflows Definition
Agiles Testen ist eine Testpraxis, die agilen Softwareentwicklungsprinzipien folgt. Im Gegensatz zur sequentiellen Wasserfallmethode startet das Agile Testing früh im Projekt und integriert kontinuierlich Entwicklung und Test. Es betont Zusammenarbeit, kontinuierliche Verbesserung und die Integration von Entwicklung und Test. Der agile Testlebenszyklus umfasst Anforderungsschätzung, Testplanung, Release-Vorbereitung und Übergang. Tests werden in verschiedenen Quadranten durchgeführt, um verschiedene Aspekte wie interne Codequalität, Geschäftsorientierung, Feedback und nicht-funktionale Anforderungen abzudecken. Dennoch gibt es Herausforderungen wie eine höhere Fehlerwahrscheinlichkeit und die Notwendigkeit effektiver Testautomatisierung im agilen Testen. Insgesamt zielt Agile Testing darauf ab, die Qualität und Anpassungsfähigkeit von Software in agilen Umgebungen sicherzustellen. [10]
---
# TDD, BDD, ATDD: Eine Übersicht

## Testgetriebene Entwicklung (TDD)
- Entwickler schreiben automatisierte Testfälle vor der Codierung.
- Der Code wird angepasst, um die Tests erfolgreich durchlaufen zu lassen.
- Fokus auf Entwickler, Programmiersprache, Unit-Tests.

## Behavior-Driven Development (BDD)
- Erweiterung von TDD, betont das Verhalten eines Systems.
- Testfälle in natürlicher Sprache mit "Given-When-Then" formuliert.
- Einbeziehung von Kunden und QA-Teams. [11]
---
## Acceptance Test-Driven Development (ATDD)
- Ähnlich wie BDD, konzentriert sich auf genaue Anforderungen.
- Verbessert die Zusammenarbeit zwischen Entwicklern, Kunden und QA.
- Verwendung von Abnahmetests.

## Unterschiede
- Beteiligte Personen: TDD (Entwickler), BDD (Kunden, QA), ATDD (Entwickler, Kunden, QA).
- Verwendete Sprache: TDD (Programmiersprache), BDD (natürliche Sprache), ATDD (genaue Anforderungen).
- Hauptaugenmerk: TDD (Unit-Tests), BDD (Verhalten des Systems), ATDD (genaue Anforderungen).
- Verwendete Tools je nach Projekt und Anforderungen.

## Die richtige Wahl
- Die effizienteste Methode oder Kombination hängt von Ihrem Projekt und Ihren Anforderungen ab. [11]
---
# Motivation, Ablauf, Inhalte, Frameworks

## Test-Driven Development (TDD)
- Motivation: Verbesserung der Softwarequalität durch vorheriges Schreiben von Tests.
- Ablauf: Schreiben von Tests, Implementierung, wiederholter Zyklus.
- Inhalte: Fokus auf Unit-Tests und erwartetem Verhalten.
- Frameworks: JUnit, pytest, NUnit.

## Behavior-Driven Development (BDD)
- Motivation: Betonung des Verhaltens aus Benutzersicht und verbesserte Kommunikation.
- Ablauf: Verwendung von "Given-When-Then" Szenarien.
- Inhalte: Benutzerorientierte Tests.
- Frameworks: Cucumber, SpecFlow, Behave. [3]
---
## Acceptance Test-Driven Development (ATDD)
- Motivation: Erfassung genauer Anforderungen und verbesserte Zusammenarbeit.
- Ablauf: Erstellung von Akzeptanztests aus Benutzersicht.
- Inhalte: Spezifikation des Benutzerverhaltens.
- Frameworks: Verwendet BDD-Frameworks wie Cucumber und SpecFlow.

## Die richtige Wahl
- Je nach Projekt und Anforderungen kann eine der Methoden oder eine Kombination effizient sein. [3]
---
# Testdoubles in TDD

## Bedeutung von Testdoubles
- Schlüsselkomponente in agilen Test-Workflows wie TDD.
- Simulieren das Verhalten echter Abhängigkeiten.
- Isolieren zu testender Codeeinheiten von anderen Systemteilen.
- Beschleunigen Tests und fördern besseres Design, Feedback und Kommunikation.

## Verwendung von Testdoubles
- Beginnt mit dem Schreiben eines fehlgeschlagenen Tests, der gewünschtes Verhalten beschreibt.
- Ersatz nicht relevanter oder nicht verfügbarer Abhängigkeiten durch Testdoubles.
- Schreiben minimalen Codes, um den Test zu bestehen.
- Testdoubles leiten Interaktionen zwischen Code und Abhängigkeiten. [12]
---
## Wann Testdoubles nutzen
- Isolieren von Codeeinheiten von Abhängigkeiten.
- Testen von schwer zu reproduzierenden Szenarien oder Grenzfällen.
- Beschleunigen und vereinfachen des Testprozesses, Ressourceneinsparung.

## Auswahl des richtigen Testdoubles
- Abhängig von Komplexität, Kontrolle, Abstraktion und Realismus.
- Verfügbare Tools und Frameworks: Mockito, JUnit, Sinon, Jest, RSpec.

## Fazit
- Testdoubles fördern agile Test-Workflows, erleichtern Isolation von Codeeinheiten und verbessern Tests, Design und Kommunikation. [12]
---
# Mocks vs Fakes vs Stubs vs Spy in Tests

## Mock
- Ein Mock ist ein Objekt, das indirekte Ein- und Ausgaben steuern kann und automatisch Erwartungen und Ergebnisse überprüft.
- Nützlich, wenn komplexe Klassen mit externen Abhängigkeiten getestet werden müssen.
- Ideal, wenn eine Klasse nicht geändert werden kann oder der Umbau zu zeitaufwändig wäre. [13]
---
```javascript
final class ShoppingService
{
    public function calculateAmount(Lines lines): Float
    {
        Float amount = 0;

        /** Complex code to test, we need a mock for this class */
        Array<Line> linesTransformed = ShoppingCart::transform(lines);
        foreach (Line line : linesTransformed) {
            amount += line.price();
        }

        return amount;
    }
}
```
In solchen Situationen ist Mocking die beste Option, wenn wir diese Klasse nicht einfach ändern können (vielleicht wird die Klasse in verschiedenen Teilen verwendet) und die Umgestaltung zu lange dauern könnte. [13]
---
```javascript
class ShoppingService // Not final anymore because of the mock!!
{
    public function calculateAmount(Lines lines): Float
    {
        Float amount = 0;

        /** Complex code to test, we need a mock for this class */
        Array<Line> linesTransformed = this.getShoppingCart(lines);
        foreach (Line line : linesTransformed) {
            amount += line.price();
        }

        return amount;
    }

    /**
     * Protected to have access in the mock object.
     *
     * @codeCoverageIgnore
     */
    protected function getShoppingCart(Lines lines): Array
    {
        return ShoppingCart::transform(lines);
    }
}
```
[13]
---
Und das ist der Spott:
```javascript
final class LoggerTest extends TestCase
{
    public function testMovieBudgetFactory(): void
    {
        MockShoppingService service = this.createMock(ShoppingService::class);
        service
            .method('getShoppingCart') // Overriding the method.
            .willReturn([100, 200, 300]);

        Lines stubLines = new Lines(null);
        Float totalAmount = service.calculateAmount(stubLines);

        self.assertEquals(600, totalAmount);
    }
}
```
[13]
---
## Fake
- Ein Fake ist eine einfachere Implementierung eines realen Objekts.
- Geeignet für den Test von Infrastrukturklassen, die außerhalb des Anwendungsbereichs liegen, wie Repositorys oder Warteschlangen.
- Ein Fake kann sich wie ein Dummy, Stub, Spy oder Mock verhalten.

```javascript
interface UserRepositoryInterface
{
    public function getUserById(String uuid): User;
}

final class FakeUserRepository implements UserRepositoryInterface
{
    public function getUserById(String uuid): UserModel
    {
        return new User(uuid, 'Jesus', "['ADMIN_ROLE']");
    }
}
```
Wenn wir also dieses gefälschte Repository verwenden, erhalten wir einen Fake-Benutzer. [13]
---
## Stub
- Ein Stub ist ein Objekt, das gefälschte Daten zurückgibt.
- Nützlich, wenn ein Dienst von einem bestimmten Objekt abhängt und sein Verhalten im Test gesteuert werden soll.[13]
---
```javascript
final class Service
{
    public function doSomething(UserModelInterface user): Int
    {
        /* Do things */
        return user.uuid;
    }
}
```
Um diesen Dienst zu testen, können wir einen Stub des Benutzers erstellen und prüfen, ob die Antwort unseren Erwartungen entspricht.
```javascript
final class ServiceTest extends TestCase
{
    public function testDoSomething(): void
    {
        // The service needs a implementation from `UserModelInterface`.
        String uuid = (new Service()).doSomething(new UserStub());
        self.assertStringContainsString('0000-000-000-00001', uuid);
    }
}

interface UserModelInterface
{
    public function getUuid(): String;
}

final class UserStub implements UserModelInterface
{
    public function getUuid(): String
    {
        return '0000-000-000-00001';
    }
}
```
[13]
---
## Spy
- Ein Testspy kann indirekte Ausgaben erfassen und indirekte Eingaben bereitstellen.
- Geeignet, um beispielsweise zu überwachen, wie oft eine Methode aufgerufen wird und welche Nachrichten sie generiert.
- Spy-Objekte können dazu führen, dass Tests fragiler werden. [13]
---

```javascript
interface LoggerInterface
{
    public function log(String message): void;
}

final class LoggerSpy implements LoggerInterface
{
    public Array<String> messages = [];

    public function log(String message): void
    {
        this.messages.add(message);
    }
}
```
[13]
---
```javascript
final class UserNotifier
{
    public function __construct(
        private LoggerInterface logger,
    ) {}

    public function registerUser(UserModelInterface user): void
    {
        this.logger.log("Notifying the user: {user.name()}");
        // ...
    }
}
```
[13]
---
Das Folgende wäre die Implementierung des Spions in einem Test:
```javascript
final class UserNotifierTest extends TestCase
{
    public function testLogMessage(): void
    {
        LoggerSpy logger = new LoggerSpy();
        UserNotifier notifier = new UserNotifier(logger);
    
        User user = new User(name: 'Jesus');
        notifier.registerUser(user);
    
        self.assertStringContainsString(
            "Notifying the user: Jesus",
            logger.messages.firt()
        );
    }
}
```
[13]
---

## Test Double Frameworks in der Softwareentwicklung

- **Definition:** Test Double Frameworks sind Tools und Bibliotheken, die in der Softwareentwicklung und im Testing eingesetzt werden, um Testdoubles zu erstellen und zu verwalten.

- **Zweck:** Sie dienen dazu, Abhängigkeiten in einer Codeeinheit zu ersetzen und ihr Verhalten zu steuern.

- **Arten von Testdoubles:** 
  - Dummy-Objekte
  - Stubs
  - Mocks
  - Spies

- **Erstellung von Testdoubles:** Frameworks bieten Funktionen zur einfachen Erstellung von Testdoubles.

- **Verhaltensdefinition:** Sie ermöglichen die Festlegung des erwarteten Verhaltens der Testdoubles, einschließlich der Reaktion auf Methodenaufrufe und Rückgabewerte.

- **Integration mit Test-Frameworks:** Test Double Frameworks sind nahtlos in gängige Test-Frameworks wie JUnit und pytest integriert. [3]
---
- **Einfache Handhabung:** Diese Frameworks bieten benutzerfreundliche APIs zur Erstellung und Konfiguration von Testdoubles.

- **Überwachung und Verifikation:** Entwickler können das Verhalten der Testdoubles überwachen und überprüfen, ob erwartete Methodenaufrufe erfolgt sind.

- **Testisolation:** Die Verwendung von Test Double Frameworks ermöglicht die Durchführung von Tests in isolierter Umgebung.

- **Beliebte Frameworks:**
  - Mockito (Java)
  - Sinon (JavaScript)
  - PHPUnit (PHP)
  - Pytest-mock (Python)

- **Zusammenfassung:** Test Double Frameworks sind unverzichtbare Werkzeuge in der agilen Softwareentwicklung, um zuverlässige und effektive Tests sicherzustellen. [3]
---
# Pair Programming
---
## Pair Programming
- **Was ist es?**
  - Zentrale Technik aus Extreme Programming (XP)
  - Zwei Entwickler arbeiten gleichberechtigt an einem Rechner

- **Rollen der Entwickler:innen**
  - "Pilot": Schreibt den Code
  - "Navigator": Überwacht die Korrektheit des Codes, den Lösungsansatz und das Design
  - Keine feste Aufgabenteilung

- **Dynamik**
  - Wechsel zwischen "Pilot" und "Navigator" alle paar Minuten
  - Partner:innen werden kontinuierlich gewechselt

- **Ziel**
  - Sicherstellen, dass jedes Teammitglied alle Teile des Projekts kennenlernt

Pair Programming fördert die Zusammenarbeit/Wissensaustausch zwischen Entwickler und verbessert die Codequalität in der Softwareentwicklung.[14]
---
## Ablauf des Pair Programming

- **Rollen der Entwickler:innen**
  - Driver (Pilot): Schreibt aktiv den Code und erklärt seine Handlungen.
  - Navigator (Beobachter): Überwacht die Codierung, gibt Feedback und denkt über Optimierungen nach.

- **Perspektiven auf den Code**
  - Driver: Konzentriert sich auf Details und Codezeilen.
  - Navigator: Nimmt eine strategische Sichtweise ein und behält das Gesamtbild im Auge.

- **Wechsel der Rollen**
  - Die Entwickler:innen tauschen regelmäßig die Rollen von Driver und Navigator. [15]
---
- **Kommunikation und Klärung**
  - Enge Zusammenarbeit und ständige Kommunikation.
  - Klärung von Unklarheiten und Fragen zum Vorgehen, zur Programmierung und zu Tests.

- **Pair Rotation (Paar-Rotation)**
  - Periodisches Wechseln der Pair-Partner:innen (z. B. alle paar Tage oder eine Woche).
  - Ziel: Frische Perspektiven und Vermeidung von Wissenssilos.

- **Praktische Zusammenarbeit**
  - Variabler Arbeitsstil: Gemeinsamer Computer oder getrennte Computer.
  - Verwendung von Versionsverwaltungstools für effiziente Zusammenarbeit.

Pair Programming fördert eine effektive Zusammenarbeit, Wissensaustausch und Qualitätsverbesserung in der Softwareentwicklung. [15]

---
## Best Practices für Pair Programming

1 . Gemeinsam planen
   - Klären von Zielen und Aufgaben
   - Festlegen der Sitzungsdauer und Rollenwechsel
   - Austausch über persönliche Vorlieben

2 . Regelmäßiger Rollenwechsel
   - Idealerweise alle 30 Minuten
   - Fördert verschiedene Perspektiven und Zusammenarbeit

3 . Gutes Audio- und Video-Setup
   - Klarstellung der Audio- und Videokommunikation
   - Verwendung von Headsets und Videokamera [16]
---
4 . Vermeiden von Mikromanagement
   - Schaffung einer sicheren Umgebung
   - Förderung des Wissensaustauschs

5 . Freundlichkeit und Geduld
   - Respekt bei unterschiedlichen Qualifikationsniveaus
   - Vermeidung von Überwachung und Unterbrechungen

6 . Vermeiden von äußeren Ablenkungen
   - Ignorieren von E-Mails und Ablenkungen
   - Planung von Pausen und außerprogrammatischen Aktivitäten

7 . Ständige Kommunikation
   - Sicherstellung der aktiven Teilnahme beider Partner
   - Zusammenarbeit fördern [16]

---
# Code reviews
---
## Code reviews
Eine Codeüberprüfung ist eine Peer-Review von Code, die Entwicklern dabei hilft, die Codequalität sicherzustellen oder zu verbessern, bevor sie ihn zusammenführen und versenden.
[17] 
---
## Conventional Comments

- Definition:
  - Standardisiertes System für Feedback in Code-Reviews und technischen Diskussionen.
  - Verwendet vordefinierte Labels zur Kategorisierung von Kommentaren.
  - Verbessert Kommunikation und Effizienz in Code-Reviews. [18]
---
| Label       | Beschreibung                                                |
|-------------|------------------------------------------------------------|
| praise      | Hebt etwas Positives hervor.                                |
| nitpick     | Schlägt geringfügige, präferenzbasierte Änderungen vor.     |
| suggestion  | Schlägt explizite Verbesserungen im Code vor.               |
| issue       | Weist auf spezifische Probleme hin, die behoben werden müssen.|
| todo        | Kennzeichnet kleine, notwendige Änderungen.                 |
| question    | Bittet um Klärung oder Untersuchung einer möglichen Bedenken.|
| thought     | Teilt Ideen mit, die während des Reviews auftauchen.        |
| chore       | Vermerkt einfache Aufgaben, die vor der Akzeptanz erledigt werden müssen.|
| note        | Hebt Informationen zur Kenntnis des Lesers hervor.          |
| typo        | Identifiziert und schlägt die Behebung von Tippfehlern vor.  |
| polish      | Empfiehlt Möglichkeiten zur Verbesserung der Code-Qualität.  |
| quibble     | Macht Vorschläge, die geringfügig sind, ähnlich wie "nitpick". |

- Dekorationen:
  - non-blocking: Kommentar, der die Code-Akzeptanz nicht blockiert.
  - blocking: Kommentar, der vor Akzeptanz behoben werden muss.
  - if-minor: Autor kann Kommentar bei geringfügigen Änderungen beheben. [18]
---

- Vorteile:
  - Verbesserte Klarheit durch standardisierte Labels und Formate.
  - Strukturiertes Feedback, das Entwicklern hilft, schneller zu verstehen.
  - Fördert einen offenen Dialog und konstruktive Gespräche.

- Verbesserung von Code-Reviews:
  - Bietet strukturierten und klaren Rahmen für Feedback. [18]
---
## Code-Review-Ablauf

1 . Einreichung des Codes:
   - Entwickler reicht Code zur Überprüfung ein, z.B., durch Pull Requests in Git.

2 . Auswahl der Überprüfer:
   - Autor wählt Teammitglieder für die Überprüfung, erfahrene Entwickler oder Experten.

3 . Review des Codes:
   - Überprüfer prüfen Code Zeile für Zeile.
   - Suchen nach Fehlern, Sicherheitslücken, Codequalität.
   - Achten auf Best Practices und Projektrichtlinien.

4 . Kommentare und Diskussion:
   - Überprüfer hinterlassen Kommentare für Probleme oder Verbesserungen.
   - Autor antwortet, Klarstellungen und Diskussionen. [3]
---

5 . Überarbeitung:
   - Autor überarbeitet Code basierend auf Kommentaren.
   - Behebt Fehler, implementiert Verbesserungen.

6 . Weitere Reviews:
   - Autor kann Code erneut einreichen für weitere Überprüfungen.
   - Prozess wiederholt sich, bis Code akzeptabel ist.

7 . Akzeptanz und Zusammenführung:
   - Code wird in Hauptprojekt/Hauptzweig zusammengeführt nach Zustimmung.

8 . Dokumentation:
   - Autor dokumentiert Änderungen im Changelog oder Projektdokumentation.

Effektive Code-Reviews:
- Fördern Wissensaustausch.
- Verbessern Code-Qualität.
- Erhöhen Zuverlässigkeit der Software.

Wichtiger Schritt für erfolgreiche Projekte und Wartbarkeit.[3]
---
## Best Practices für Code-Reviews

1. **Klarer Prozess etablieren:**
   - Definition von Regeln und Schritten für Code-Reviews.
   - Festlegung, wann Pull Requests erstellt werden und wer sie überprüft.

2. **Fokus auf das Wesentliche:**
   - Bewertung von Aspekten wie Funktionalität, Softwaredesign, Komplexität, Tests, Benennung, Kommentaren und Dokumentation.

3. **Frühzeitige Diskussion:**
   - Vor der Implementierung komplexe Aufgaben besprechen, um spätere Änderungen zu minimieren.

4. **Teamoptimierung:**
   - Teamleistung optimieren, nicht nur individuelle Produktivität.
   - Beteiligung aller Teammitglieder sicherstellen und Reaktionszeit auf PRs festlegen.[19]
---
5 . **Entscheidungen umsetzen:**
   - Technische Entscheidungen in angemessener Zeit umsetzen und lange Entscheidungsprozesse vermeiden.

6 . **Kleine Pull Requests:**
   - Kleinere PRs vereinfachen die Verwaltung und beschleunigen den Prozess (ca. 100 Zeilen pro PR).

7 . **Positive Feedback-Kultur:**
   - Feedback zum Code, nicht zum Autor.
   - Akzeptanz verschiedener Lösungsansätze und Respekt gegenüber Teammitgliedern.

8 . **Effektive Nutzung der kontinuierlichen Integration:**
   - Automatisierung von Qualitätsprüfungen, um manuelle Überprüfungen auf wichtigere Aspekte zu konzentrieren.[19]

9 . **Automatisierung von Kleinigkeiten:**
   - Automatisierung von stilistischen Prüfungen und Vermeidung langer Diskussionen über Stilfragen.
---
10 . **Explizite Kommunikation:**
    - Klare Anweisungen an den Autor, was geändert werden sollte.
    - Nutzung von Tools zur expliziten Kommunikation.

11 . **Explizite Überprüfungsanfragen:**
    - Automatisierung von Überprüfungsanfragen, um das Übersehen von PRs zu verhindern.

12 . **Selbstprüfung des Codes:**
    - Vor Einreichung der PR den eigenen Code auf einfache Fehler überprüfen.

13 . **Dokumentation im Code:**
    - Dokumentation von Codeänderungen und Diskussionen direkt im Code zur Verbesserung der Lesbarkeit und des Verständnisses.[19]
---
14 . **Klare PR-Beschreibungen:**
    - Erstellung detaillierter PR-Beschreibungen für ein klares Bild der Änderungen.

15 . **Shared-Repository-Modell nutzen:**
    - Empfohlen in privaten Repositorys zur Vereinfachung von Abläufen und effizienteren Code-Branches.

16 . **Öffentliche Diskussionen:**
    - Führung von Diskussionen innerhalb der PR-Diskussionen, um sie für alle zugänglich und durchsuchbar zu machen.

Mit diesen bewährten Methoden können Code-Reviews effektiver gestaltet werden, was zu höherer Codequalität und besserer Teamarbeit führt.
[19]
---
# Refactoring
---
## Refactoring
Refactoring ist eine disziplinierte Technik zur Umstrukturierung eines vorhandenen Codekörpers, bei der seine interne Struktur geändert wird, ohne sein äußeres Verhalten zu ändern.

Sein Herzstück ist eine Reihe kleiner verhaltenserhaltender Transformationen. Jede Transformation (als „Refactoring“ bezeichnet) bewirkt wenig, aber eine Abfolge dieser Transformationen kann zu einer erheblichen Umstrukturierung führen. Da jedes Refactoring klein ist, ist es weniger wahrscheinlich, dass es schiefgeht. Das System bleibt nach jedem Refactoring voll funktionsfähig, wodurch die Wahrscheinlichkeit verringert wird, dass ein System während der Umstrukturierung ernsthaft beschädigt wird.

[20]
---
## Ziele des Refactorings

- Verbesserung der Lesbarkeit des Codes.
- Vereinfachung des Verständnisses und der Wartung des Codes.
- Steigerung der Codequalität durch Reduzierung der Komplexität.
- Erhöhung der Wartbarkeit und Leistung des Codes.
- Vereinfachung der Codebasis.
- Reduzierung der technischen Schulden.

Refactoring ist ein wesentlicher Bestandteil der agilen Softwareentwicklung und wird oft in Kombination mit Test-Driven Development (TDD) eingesetzt.
[3]
---
## Refactoring-Patterns
---
##Extract Method
Dieses Muster ist nützlich, um lange und komplexe Methoden in kleinere, leichter verständliche Teile aufzuteilen.

Problem:
Sie haben ein Codefragment, das gruppiert werden kann.

```javascript
void printOwing() {
  printBanner();

  // Print details.
  System.out.println("name: " + name);
  System.out.println("amount: " + getOutstanding());
}
```
Lösung:
Verschieben Sie diesen Code in eine separate neue Methode (oder Funktion) und ersetzen Sie den alten Code durch einen Aufruf der Methode. [21]

```javascript
void printOwing() {
  printBanner();
  printDetails(getOutstanding());
}

void printDetails(double outstanding) {
  System.out.println("name: " + name);
  System.out.println("amount: " + outstanding);
}
``` 
---
## Extract Variable
Dieses Muster wird verwendet, um komplexe Ausdrücke in benannte Variablen zu extrahieren, um den Code verständlicher zu machen.

Problem:
Sie haben einen Ausdruck, der schwer zu verstehen ist.

```javascript
void renderBanner() {
  if ((platform.toUpperCase().indexOf("MAC") > -1) &&
       (browser.toUpperCase().indexOf("IE") > -1) &&
        wasInitialized() && resize > 0 )
  {
    // do something
  }
}
```
Lösung:
Platzieren Sie das Ergebnis des Ausdrucks oder seiner Teile in separaten Variablen, die selbsterklärend sind. [22]
```javascript
void renderBanner() {
  final boolean isMacOs = platform.toUpperCase().indexOf("MAC") > -1;
  final boolean isIE = browser.toUpperCase().indexOf("IE") > -1;
  final boolean wasResized = resize > 0;

  if (isMacOs && isIE && wasInitialized() && wasResized) {
    // do something
  }
}
```
---
## Inline Method
Umgekehrt zu "Extract Method", das Entfernen kleiner Hilfsmethoden kann den Code vereinfachen.

Problem:
Wenn ein Methodenkörper offensichtlicher ist als die Methode selbst, verwenden Sie diese Technik.
```javascript
class PizzaDelivery {
  // ...
  int getRating() {
    return moreThanFiveLateDeliveries() ? 2 : 1;
  }
  boolean moreThanFiveLateDeliveries() {
    return numberOfLateDeliveries > 5;
  }
}
```
Lösung:
Ersetzen Sie Aufrufe der Methode durch den Inhalt der Methode und löschen Sie die Methode selbst. [23]

```javascript
class PizzaDelivery {
  // ...
  int getRating() {
    return numberOfLateDeliveries > 5 ? 2 : 1;
  }
}
```
---
## Weitere Refactoring Patterns

- **Rename Variable:** Umbenennung von Variablen in verständliche Namen zur Verbesserung der Lesbarkeit.

- **Move Method:** Verschieben von Methoden in die richtige Klasse zur Verbesserung der Code-Struktur und Verwaltung von Abhängigkeiten.

- **Replace Conditional with Polymorphism:** Umstellung von bedingten Anweisungen auf polymorphe Strukturen zur Steigerung der Wartbarkeit und Lesbarkeit.

- **Encapsulate Field:** Einhüllen von Feldern in Methoden, um den Feldzugriff zu steuern und die Flexibilität zu erhöhen.

- **Introduce Parameter Object:** Gruppieren von vielen Parametern einer Methode in einem Objekt zur Vereinfachung der Methodensignatur.

- **Encapsulate Collection:** Einhüllen von Sammlungen in eigene Klassen zur besseren Steuerung und Datenabstraktion.

- **Remove Duplicate Code:** Entfernung von Duplikaten im Code zur Steigerung der Wartbarkeit und Fehlerreduzierung.

Diese sind einige der am häufigsten verwendeten Refactoring Patterns, aber es gibt noch viele weitere. [3]

---
# Tools
---
## Test-Tools

- Testautomatisierungs-Frameworks sind Regelwerke und Tools zur effizienten Erstellung von Testfällen.

- Vorteile: Wiederverwendbarkeit von Code, kostengünstige Testfallentwicklung, minimale manuelle Interaktion, Standardisierung von Testabläufen, Maximierung der Testabdeckung. [24]
---
- Arten von automatisierten Test-Frameworks:

  - Datengesteuertes Test-Framework: Speicherung von Testdaten auf externen Laufwerken zur Erweiterung von Testskripten.

  - Schlüsselwortgesteuertes Test-Framework: Extraktion von Testdaten aus externen Quellen, Verwendung von Schlüsselwörtern zur Anpassung von Testskripten und Erzielung unterschiedlicher Ergebnisse.

  - Hybrid-Test-Framework: Kombination von datengesteuerten und schlüsselwortgesteuerten Frameworks für höhere Produktivität.

  - Lineares Scripting-Framework: Manuelle Aufzeichnung von Prozessschritten, weniger Automatisierung, auch als "Record and Playback Framework" bekannt.

  - Modulbasiertes Test-Framework: Separate Skripte für verschiedene Module, hohe Modularisierung, individuelle Anpassungen der Testdaten.

- Auswahl des Frameworks je nach Anforderungen und Komplexität der Testfälle zur Maximierung der Effizienz, Wiederverwendbarkeit und Kostenreduzierung. [24]
---
## Build Tools

Build Tools sind Softwarewerkzeuge, die in der Softwareentwicklung eingesetzt werden, um den Prozess der Kompilierung, des Testens und des Bereitstellens von Software zu automatisieren. Sie spielen eine entscheidende Rolle bei der Umwandlung von Quellcode in ausführbare Anwendungen oder Bibliotheken.

1. Jenkins
   - Open-Source-Automatisierungstool für CI/CD.
   - Einfache Einrichtung auf verschiedenen Plattformen.
   - Unterstützt Plugin-basierte Integration mit Drittanbieter-Tools.
   - Ermöglicht verteilte Builds.
   - Bietet nativ Integration mit Versionskontrollsystemen wie Git.

2. Gradle
   - Open-Source-Build-Automatisierungstool mit Schwerpunkt auf Anpassbarkeit und Geschwindigkeit.
   - Verwendet eine Groovy-basierte DSL für Build-Skripts.
   - Unterstützt inkrementelle Builds und ist flexibel für verschiedene Projekte und Sprachen.
   - Besonders geeignet für die Android-Entwicklung. [25]
---
3 . Maven
   - Populäres Build-Automatisierungstool, spezialisiert auf die Java-Entwicklung.
   - Verwendet XML-basierte POM-Dateien zur Steuerung des Builds.
   - Betont Konvention über Konfiguration und zentralisierte Abhängigkeitsverwaltung.
   - Unterstützt verschiedene Phasen des Projektzyklus.

4 . Travis CI
   - Cloud-Lösung zur Automatisierung des Builds und Tests von GitHub-Repositories.
   - Einfache Einrichtung und Integration mit GitHub.
   - Bietet parallele Builds für schnellere Tests und kürzere Build-Zeiten.

5 . CircleCI
   - Continuous Integration- und Continuous Delivery-Tool in der Cloud.
   - Fokussiert auf Tests von Code-Änderungen mit Unit-Tests, Integrationstests und Funktionstests.
   - Arbeitet gut mit Docker-Containern und bietet Caching für schnellere Builds.

Die Wahl des richtigen Tools hängt von Projektanforderungen, Plattformunterstützung und Integration in CI/CD-Pipelines ab. Es gibt keine Einheitslösung, da jedes Tool Unterschiedlich ist. [25]
---
## GitHub Actions

GitHub Actions ist ein mächtiges Tool zur Automatisierung von Build- und Testprozessen in GitHub-Repositorys. Es ermöglicht Entwicklern, Workflow-Automatisierungen zu erstellen und auszuführen, die auf Ereignissen in ihren Repositorys basieren.

- **Automatisierte Tests:** Mit GitHub Actions können Entwickler automatisierte Tests als Teil ihres Workflows erstellen. Dies gewährleistet, dass bei jedem Commit oder Pull Request automatisch Tests durchgeführt werden, um Code-Fehler zu identifizieren. Besonders nützlich in Continuous Integration (CI) und Continuous Deployment (CD) Pipelines.

- **Build-Prozesse:** Entwickler können auch Build-Prozesse automatisieren. Der Code wird automatisch kompiliert, Bibliotheken werden heruntergeladen, und Artefakte für den Bereitstellungsprozess werden erstellt. Dies beschleunigt den Build-Prozess und minimiert menschliche Fehler.

- **Vielseitigkeit:** GitHub Actions unterstützt verschiedene Programmiersprachen, Build-Tools und Test-Frameworks. Der Workflow kann an die spezifischen Anforderungen des Projekts angepasst werden.[3]
---

- **Benutzerdefinierte Workflows:** Entwickler können benutzerdefinierte Workflow-Dateien erstellen, um präzise festzulegen, welche Schritte ausgeführt werden sollen, und spezifische Build- und Testaufgaben entsprechend den Projektanforderungen konfigurieren.

- **Integrationen:** GitHub Actions kann in Kombination mit anderen Tools und Diensten genutzt werden, um erweiterte CI/CD-Pipelines zu erstellen. Zum Beispiel können Docker-Container für Testumgebungen erstellt und Cloud-Dienste für die Bereitstellung genutzt werden.

- **Status-Checks:** Nach Abschluss eines GitHub-Actions-Workflows sind Status-Checks und Berichte in Pull Requests verfügbar, um Tests zu überwachen und die Code-Qualität vor der Zusammenführung sicherzustellen.

- **Skalierbarkeit:** GitHub Actions ist flexibel und kann sowohl in kleinen als auch in großen Projekten eingesetzt werden, um sich an die spezifischen Projektanforderungen anzupassen.

Insgesamt bietet GitHub Actions eine nahtlose Möglichkeit, CI/CD in GitHub-Workflows zu integrieren, um sicherzustellen, dass der Code getestet und effizient bereitgestellt wird. Es ist eine wertvolle Ressource für Entwickler, um die Qualität ihres Codes sicherzustellen und Entwicklungsprozesse zu automatisieren. [3]
---
## Bug and Work Tracking Tools

Diese Tools sind nützlich für Softwareentwickler, Projektmanager und Teams, um Fehler und Aufgaben effizient zu verfolgen und zu verwalten. Hier sind einige beliebte Optionen:

- **Jira:** Ein bekanntes Tool von Atlassian zur Verfolgung von Aufgaben, Bugs und Projekten. Es bietet umfangreiche Anpassungsmöglichkeiten und wird weltweit in der Softwareentwicklung eingesetzt.

- **Trello:** Ein visuelles Projektmanagement-Tool, ideal für kleinere Teams und weniger komplexe Projekte. Verwendet Boards, Listen und Karten zur Aufgaben- und Fehlerorganisation.

- **Asana:** Ein umfassendes Projektmanagement-Tool, das die Zusammenarbeit in Teams ermöglicht. Bietet Funktionen wie Zeitleisten und Abhängigkeiten für die Aufgabenverfolgung.

- **GitHub Issues:** Perfekt für Open-Source-Projekte und Entwicklungsprojekte auf GitHub. Ermöglicht die Verfolgung von Problemen direkt im GitHub-Repository. [3]
---
- **Bugzilla:** Eine Open-Source-Plattform für das Bug-Tracking, die von vielen großen Organisationen eingesetzt wird. Bietet zahlreiche Funktionen für die Fehler- und Aufgabenverfolgung.

- **Redmine:** Eine Open-Source-Projektmanagement- und Bug-Tracking-Plattform mit flexiblen Anpassungsmöglichkeiten und großer Entwicklergemeinschaft.

- **Zendesk:** Eine Kunden-Support- und Ticketverwaltungsplattform, die auch für das Bug-Tracking genutzt werden kann. Ideal für die Kombination von Kundenbetreuung und Fehlerverfolgung.

- **Mantis Bug Tracker:** Ein benutzerfreundliches Open-Source-Tool für das Bug-Tracking, geeignet für kleinere Entwicklungsteams.

Die Auswahl eines Bug- und Arbeitsverfolgungstools sollte auf den spezifischen Anforderungen eines Teams und Projekts basieren. Berücksichtige Faktoren wie Teamgröße, Projektumfang, Budget und Integrationsmöglichkeiten bei der Auswahl des richtigen Tools für deine Bedürfnisse. [3]
---

# Quellen
  [0]: OpenAI GPT-3 Model. ChatGPT. URL: <https://platform.openai.com/docs/guides/chat> (abgerufen am 17. Oktober 2023)

  [1]: Atlassian. "What is Version Control?" Atlassian Git Tutorial, URL: <https://www.atlassian.com/git/tutorials/what-is-version-control> (abgerufen am 17. Oktober 2023)

  [2]: GitLab Inc. "Why it’s time to move to a Distributed Version Control System." GitLab Blog, URL: <https://about.gitlab.com/blog/2020/11/19/move-to-distributed-vcs/> (abgerufen am 17. Oktober 2023)

  [3]: Atlassian. "What is Git? | Atlassian Git Tutorial." Atlassian, URL: <https://www.atlassian.com/git/tutorials/what-is-git> (abgerufen am 17. Oktober 2023)

  [4]: Git - Working with Remotes. "Git Basics - Working with Remotes." git-scm.com, URL: <https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes#:~:text=Remote%20repositories%20are%20versions%20of,or%20read%2Fwrite%20for%20you> (abgerufen am 17. Oktober 2023
  
  [5]: Visual Git Guide. "Visual Git Guide." marklodato.github.io, URL: <https://marklodato.github.io/visual-git-guide/index-en.html> (abgerufen am 17. Oktober 2023)

  [6]: "Explain Git with D3." onlywei.github.io, URL: <https://onlywei.github.io/explain-git-with-d3/#> (abgerufen am 17. Oktober 2023)

  [7]: blog.osteele.com. "My Git Workflow" URL: https://blog.osteele.com/2008/05/my-git-workflow/ (abgerufen am 17. Oktober 2023)

  [8]: kinsta.com. "Monorepo vs. Multi-Repo: Pros and Cons" URL: https://kinsta.com/blog/monorepo-vs-multi-repo/ (abgerufen am 17. 
  Oktober 2023)

  [9]: atlassian.com. "Git Submodules" URL: https://www.atlassian.com/git/tutorials/git-submodule (abgerufen am 17. Oktober 2023)
  
  [10]: atlassian.com. "Making a Pull Request" URL: https://www.atlassian.com/git/tutorials/making-a-pull-request (abgerufen am 17. Oktober 2023)

  [11]: atlassian.com. "Branching" URL: https://www.atlassian.com/agile/software-development/branching (abgerufen am 17. Oktober 2023)

  [12]: mermaid.js. "Mermaid GitGraph Syntax" URL: https://mermaid.js.org/syntax/gitgraph.html (abgerufen am 17. Oktober 2023)

  [13]: atlassian.com. "Trunk Based Development" URL: https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development (abgerufen am 17. Oktober 2023)

  [14]: ardalis.com. "Trunk-Based Development vs. Long-Lived Feature Branches" URL: https://ardalis.com/trunk-based-development-vs-long-lived-feature-branches/#:~:text=What%20is%20Long%2DLived%20Feature,developers%20to%20work%20in%20isolation. (abgerufen am 17. Oktober 2023)

  [15]: atlassian.com. "Using branches" URL: https://www.atlassian.com/git/tutorials/using-branches/merge-strategy (abgerufen am 17. Oktober 2023)

  [16]: docs.github.com. "Incorporating changes from a pull request" URL: https://docs.github.com/de/pull-requests/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/about-pull-request-merges (abgerufen am 17. Oktober 2023)

  [17]: gist.github.com. "Git Cheatsheet" URL: https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53 (abgerufen am 17. Oktober 2023)

  [18]: aimultiple.com. "Conversational AI vs Generative AI: What’s the Difference?" URL: https://research.aimultiple.com/conversational-ai-vs-generative-ai/ (abgerufen am 17. Oktober 2023)

  [19]: linkedin.com. "Tips and Tricks for Better Googling" URL: https://www.linkedin.com/pulse/tips-tricks-better-googling-javid-ahmadi (abgerufen am 17. Oktober 2023)

  20. [Turing - Start Reading Code the Right Way](https://www.turing.com/kb/start-reading-code-the-right-way)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

  21. [Testsigma - How to Write a Good Bug Report](https://testsigma.com/blog/how-to-write-a-good-bug-report-some-tips/#How_to_Write_a_Bug_Report)
    - **Autor:** Atif Beg
    - **Veröffentlichungsdatum:** May 23, 2023
    - **Abrufdatum:** 19. Oktober 2023

  22. [Chat GPT](https://chat.openai.com/)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht anwendbar
    - **Abrufdatum:** 19. Oktober 2023

  23. [LinkedIn - Root Cause Analysis You Must Know](https://www.linkedin.com/pulse/all-rcaroot-cause-analysis-you-must-know-dhirendra-patel)
    - **Autor:** Dhirendra Patel
    - **Veröffentlichungsdatum:** 30. Dez. 2022
    - **Abrufdatum:** 19. Oktober 2023

  24. [Testsigma - Difference Between Testing and Debugging](https://testsigma.com/blog/difference-between-testing-and-debugging/#Difference_Between_Testing_and_Debugging)
    - **Autor:** Kiruthika Devaraj
    - **Veröffentlichungsdatum:** July 15, 2023
    - **Abrufdatum:** 19. Oktober 2023

  25. [Rubber Duck Debugging](https://rubberduckdebugging.com/)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

  26. [Undo - 6 Things About Time-Travel Debugging](https://undo.io/resources/6-things-time-travel-debugging#:~:text=Time%20travel%20debugging%20(aka%20reverse,to%20inspect%20the%20program%20state.)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

  27. [Coralogix - Tracing vs. Logging: What to Know](https://coralogix.com/blog/tracing-vs-logging-what-to-know/)
    - **Autor:** Tobias Schlichtmeier
    - **Veröffentlichungsdatum:** 14. Mai 2021
    - **Abrufdatum:** 19. Oktober 2023

  28. [Elektroniknet - Vier Tools im Check](https://www.elektroniknet.de/embedded/entwicklungstools/vier-tools-im-check.186375.html)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

  29. [Guru99 - Agile Testing: A Beginner's Guide](https://www.guru99.com/agile-testing-a-beginner-s-guide.html)
      - **Autor:** Thomas Hamilton
      - **Veröffentlichungsdatum:** October 7, 2023
      - **Abrufdatum:** 19. Oktober 2023

  30. [BrowserStack - TDD vs. BDD vs. ATDD](https://www.browserstack.com/guide/tdd-vs-bdd-vs-atdd)
      - **Autor:** Jash Unadkat
      - **Veröffentlichungsdatum:** June 15, 2023
      - **Abrufdatum:** 19. Oktober 2023

  31. [LinkedIn - How Do You Use Test Doubles, Mocks, Stubs?](https://www.linkedin.com/advice/3/how-do-you-use-test-doubles-mocks-stubs)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  32. [Jesus Valera Reales - Testing With Test Doubles](https://jesusvalerareales.com/testing-with-test-doubles/#:~:text=The%20five%20types%20of%20Test,how%20it%20will%20be%20used.)
      - **Autor:** Jesus Valera Reales
      - **Veröffentlichungsdatum:** June 11, 2020
      - **Abrufdatum:** 19. Oktober 2023

  33. [it-agile - Was ist Pair Programming?](https://www.it-agile.de/agiles-wissen/agile-entwicklung/was-ist-pair-programming/)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  34. [T2Informatik - Pair Programming](https://t2informatik.de/wissen-kompakt/pair-programming/)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  35. [Duckly - 7 Tips for Successful Pair Programming](https://duckly.com/blog/7-tips-for-successful-pair-programming/)
      - **Autor:** Jfromtheblock
      - **Veröffentlichungsdatum:** 17 SEPTEMBER 2021
      - **Abrufdatum:** 19. Oktober 2023

  36. [GitLab - What Is Code Review?](https://about.gitlab.com/topics/version-control/what-is-code-review/)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  37. [dev.to - Enhancing Code Reviews With Conventional Comments](https://dev.to/tsotsi1/enhancing-code-reviews-with-conventional-comments-2j9i)
      - **Autor:** TSOTSI1
      - **Veröffentlichungsdatum:** 12. Juni .2023
      - **Abrufdatum:** 19. Oktober 2023

  38. [Swarmia - A Complete Guide to Code Reviews](https://www.swarmia.com/blog/a-complete-guide-to-code-reviews/?utm_term=code%20review%20best%20practices&utm_campaign=SRH-REVIEW-EU-EN&utm_source=adwords&utm_medium=ppc&hsa_acc=6644081770&hsa_cam=16463390785&hsa_grp=134848023275&hsa_ad=585675515692&hsa_src=g&hsa_tgt=kwd-298072696942&hsa_kw=code%20review%20best%20practices&hsa_mt=p&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjwp8OpBhAFEiwAG7NaEhy7Gvy4r35tivXyYYrIs0-WQrkUQggqz3NcB2demdyWZ-7DKr0g3RoCY8sQAvD_BwE#best-practices-for-code-reviews
      - **Autor:** Kimmo Brunfeldt
      - **Veröffentlichungsdatum:** Oct 12, 2021
      - **Abrufdatum:** 19. Oktober 2023

  39. [Refactoring - refactoring.com](https://refactoring.com/)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  40. [Refactoring Guru - Extract Method](https://refactoring.guru/extract-method)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  41. [Refactoring Guru - Extract Variable](https://refactoring.guru/extract-variable)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  42. [Refactoring Guru - Inline Method](https://refactoring.guru/inline-method)
      - **Autor:** Nicht angegeben
      - **Veröffentlichungsdatum:** Nicht angegeben
      - **Abrufdatum:** 19. Oktober 2023

  43. [BrowserStack - Best Test Automation Frameworks](https://www.browserstack.com/guide/best-test-automation-frameworks)
      - **Autor:** GH and Akshay Badkar
      - **Veröffentlichungsdatum:** August 27, 2023
      - **Abrufdatum:** 19. Oktober 2023

  44. [BrowserStack - Build Tools](https://www.browserstack.com/guide/build-tools)
      - **Autor:** Somosree Roy
      - **Veröffentlichungsdatum:** July 27, 2023
      - **Abrufdatum:** 19. Oktober 2023

