* __Version control systems / Source code management__
  Version Control, auch als Quellcodeverwaltung bezeichnet, ist die Praxis, Änderungen am Software-Code zu verfolgen und zu verwalten. Version-Control-Systeme sind Software-Tools, die Software-Teams dabei helfen, diese Änderungen effizient zu managen, insbesondere in beschleunigten Entwicklungsumgebungen. Sie sind besonders vorteilhaft für DevOps-Teams, da sie die Entwicklungszeit verkürzen und erfolgreiche Bereitstellungen fördern. Diese Software hält jede Code-Änderung in einer speziellen Datenbank fest und ermöglicht es Entwicklern, Fehler zu beheben, indem sie auf frühere Code-Versionen zurückgreifen, ohne die Teammitglieder zu stark zu beeinträchtigen. [1]

  * __Centralized vs Distributed Version Control__
    Zentralisierte Versionskontrolle verlässt sich auf einen zentralen Server, was einfache Einrichtung und Workflow-Kontrolle bietet. Sie hat jedoch Nachteile wie das Risiko eines einzigen Serverausfalls und Schwierigkeiten bei Merging und Branching. Verteilte Versionskontrolle hingegen bietet multiple Backups, ermöglicht Offline-Commits und schnelles Branching, da sie keinen einzelnen Fehlerpunkt hat. Git ist ein bekanntes Beispiel für ein verteiltes Versionskontrollsystem, das in der Softwareentwicklung weit verbreitet ist. [2]

  * __Git__
    Git ist das am weitesten verbreitete moderne Versionskontrollsystem der Welt. Es ist ein ausgereiftes, quelloffenes Projekt, das von Linus Torvalds, dem Schöpfer des Linux-Betriebssystemkernels, entwickelt wurde. Git wird von einer breiten Palette von Softwareprojekten für die Versionskontrolle verwendet und ist bekannt für seine Verteilungsarchitektur, die es Entwicklern ermöglicht, die vollständige Historie ihrer Änderungen in ihren Arbeitskopien zu haben. Git wurde auch mit Schwerpunkt auf Leistung, Sicherheit und Flexibilität entworfen. [3]

    * __Remote repositories__
        Remote Repositories sind Versionen des Projekts, die im Internet oder irgendwo im Netzwerk gehostet werden. Sie können mehrere davon haben, von denen jede in der Regel entweder schreibgeschützt oder schreibgeschützt ist. Die Zusammenarbeit mit anderen beinhaltet die Verwaltung dieser remote Repositories und das Übertragen von Daten zu und von ihnen, wenn Sie Arbeit teilen müssen. Die Verwaltung von remote Repositories umfasst das Hinzufügen von remote Repositories, das Entfernen von nicht mehr gültigen Remotes, die Verwaltung verschiedener entfernter Branches und deren Definition als tracked oder untracked, und vieles mehr. [4]

    * __Visualisierung von relevanten git-Kommandos und -Workflows__
      * <https://marklodato.github.io/visual-git-guide/index-en.html>
      * <https://onlywei.github.io/explain-git-with-d3/#>
        1. `git commit`: Dieser Befehl erstellt einen Commit, der die aktuellen Änderungen im Arbeitsverzeichnis in das lokale Repository aufnimmt.

        2. `git branch`: Mit diesem Befehl können Sie die vorhandenen Branches im Repository auflisten. Es zeigt auch den aktuellen Branch an.

        3. `git checkout`: Dieser Befehl wird verwendet, um zwischen verschiedenen Branches zu wechseln oder um bestimmte Commits oder Dateiversionen wiederherzustellen.

        4. `git checkout -b`: Mit dieser Option können Sie einen neuen Branch erstellen und gleichzeitig zu diesem neuen Branch wechseln.

        5. `git reset`: Dieser Befehl wird verwendet, um Commits rückgängig zu machen, indem der HEAD oder der Branch auf einen früheren Commit zurückgesetzt wird.

        6. `git revert`: Mit diesem Befehl wird ein neuer Commit erstellt, der die Änderungen eines früheren Commits rückgängig macht, anstatt den Commit selbst zu löschen.

        7. `git merge`: Dieser Befehl wird verwendet, um Änderungen aus einem anderen Branch in den aktuellen Branch zu integrieren.

        8. `git rebase`: Dieser Befehl wird verwendet, um die Commit-Historie neu zu organisieren, indem Commits aus einem Branch auf den anderen angewendet werden.

        9. `git fetch`: Mit diesem Befehl werden die neuesten Änderungen aus einem entfernten Repository heruntergeladen, ohne sie jedoch in Ihr lokales Repository zu überführen.

        10. `git pull`: Dieser Befehl kombiniert `git fetch` und `git merge` in einem Schritt. Es lädt die neuesten Änderungen aus dem entfernten Repository herunter und führt sie in Ihren lokalen Branch ein.

        11. `git push`: Mit diesem Befehl können Sie Ihre lokalen Commits in ein entferntes Repository hochladen, um sie für andere Teammitglieder verfügbar zu machen.

        12. `git tag`: Dieser Befehl wird verwendet, um Tags zu erstellen, um bestimmte Commit-Versionen in der Historie zu markieren, was besonders nützlich für Versionen und Releases ist.

      * __Sequenzdiagramm für git data transfer commands__
        * <https://blog.osteele.com/2008/05/my-git-workflow/>
        ![](media\git-transport.jpg) [7]
        
    * __Multirepos vs. Monorepos__
      Beide Ansätze, Monorepo und Multi-Repo, zielen darauf ab, Code effizient zu verwalten, aber ihr Hauptunterschied liegt im Zeitpunkt, zu dem Entscheidungen getroffen werden. Bei Multi-Repo werden Bibliotheken unabhängig voneinander verwaltet, was es Teams ermöglicht, schnell zu arbeiten, jedoch auf Kosten möglicher Divergenz. In einem Monorepo müssen Teams zusammenarbeiten und alle Bibliotheken gleichzeitig anpassen, um Konflikte zu vermeiden, was die Geschwindigkeit beeinträchtigen kann, aber die Code-Konsistenz gewährleistet. Monorepo fördert eine Kultur der Achtsamkeit, während Multi-Repo eine Kultur des schnellen Fortschritts begünstigt. [8]

    * __Submodules__
    Git-Submodule ermöglichen es, ein Git-Repository als Unterverzeichnis eines anderen Git-Repositorys zu behalten. Git-Submodule sind einfach eine Referenz auf ein anderes Repository zu einem bestimmten Zeitpunkt. Sie ermöglichen einem Git-Repository, die Versionshistorie von externem Code einzubeziehen und zu verfolgen. [9]

    * __Pull requests__
      In ihrer einfachsten Form sind Pull Requests ein Mechanismus, mit dem ein Entwickler Teammitglieder darüber benachrichtigt, dass sie eine Funktion abgeschlossen haben. Sobald ihr Feature-Branch bereit ist, reicht der Entwickler über ihr Bitbucket-Konto einen Pull Request ein. Dies informiert alle Beteiligten darüber, dass sie den Code überprüfen und in den Haupt-Branch überführen müssen.

      Aber der Pull Request ist mehr als nur eine Benachrichtigung - es handelt sich um ein dediziertes Forum zur Diskussion der vorgeschlagenen Funktion. Wenn es Probleme mit den Änderungen gibt, können Teammitglieder Feedback im Pull Request hinterlassen und die Funktion sogar durch das Einreichen [10]

    * __Branching strategies__
      Release Branching: Hier wird jede Veröffentlichung in einem eigenen Branch verwaltet. Das bedeutet, dass Änderungen sowohl im Veröffentlichungs-Branch als auch im Haupt-Branch durchgeführt werden müssen. Dies kann zu erhöhtem Aufwand und Verwirrung führen.
      Feature Branching: Bei diesem Ansatz werden Features in eigenen Branches entwickelt und mit Feature Flags gesteuert. Dies ermöglicht eine schrittweise Bereitstellung und bessere Kontrolle.
      Task Branching: Diese Methode konzentriert sich auf die Aufgabenverwaltung und erstellt für jede Aufgabe einen eigenen Branch. Dies ermöglicht eine transparente Zuordnung von Änderungen zu Aufgaben und ist besonders für agile Entwicklung geeignet. [11]

      * <https://mermaid.js.org/syntax/gitgraph.html>
        Git Flow: Beliebte Strategie mit "master" (produktionsbereiter Code) und "develop" (neuester Code) Branches. Entwickler erstellen Feature-, Release- und Hotfix-Branches.

        Github Flow: Vereinfachte Version von Git Flow mit nur einem "main"-Branch. Entwickler erstellen Feature-Branches und mergen sie nach Abschluss zurück.

        Trunk-Based Development: Ein einzelner "trunk"-Branch enthält den aktuellen Code. Entwickler erstellen kurzlebige Feature-Branches und mergen sie zurück.

        Feature Branching: Für jede Funktion wird ein separater Branch erstellt. Entwickler mergen die Feature-Branches zurück, wenn die Arbeit abgeschlossen ist.

        Task Branching: Ein Branch pro Aufgabe. Entwickler mergen Task-Branches zurück, wenn Aufgaben erledigt sind, ideal für agile Teams.

        Clear Framework Branching: Festgelegte Regeln und Workflows für die Erstellung von Branches für Features, Releases und Bugfixes, erfordert hohe Koordination
        [12]

      * __Trunk-based Development__
        Trunk-based development ist eine Praxis im Versionskontrollmanagement, bei der Entwickler kleine und häufige Updates direkt in den Haupt-Branch (Trunk) integrieren. Dies beschleunigt die Integration, ermöglicht Continuous Integration/Continuous Delivery (CI/CD) und steigert die Softwareauslieferung und organisatorische Leistung. Im Gegensatz dazu gibt es auch das strengere Gitflow-Modell, bei dem nur bestimmte Personen Änderungen im Hauptcode genehmigen können, um die Codequalität zu wahren und Fehler zu minimieren. Trunk-based development hingegen erlaubt allen Entwicklern Zugriff auf den Hauptcode, was schnellere Iterationen und CI/CD ermöglicht.
        [13]

      * __Long-lived branches__
        Long-Lived Feature Branching beinhaltet das Erstellen von separaten Branches für neue Funktionen oder größere Änderungen. Diese Branches existieren unabhängig von der Hauptentwicklungslinie und werden über längere Zeiträume gepflegt. Sobald die Änderungen fertig und getestet sind, werden sie in die Hauptentwicklungslinie gemerged, oft nach umfassender Überprüfung und Konfliktlösung. Dieser Ansatz ist in Open-Source-Software verbreitet, wo Community-Beitragende oft keine direkten Zugriff auf die Hauptlinie haben. Die Dauer eines "langandauernden" Branches hängt von der Aktivität im Code ab, nicht von der Kalenderzeit. Wichtiger ist die Menge der Änderungen seit der Erstellung des Branches in der Hauptlinie.
        [14]

      * __Git Flow__
        Git Flow: Diese Branching-Strategie ist in der Branche beliebt. Sie beinhaltet die Erstellung von zwei langfristigen Branches, nämlich den "master"-Branch und den "develop"-Branch. Der "master"-Branch enthält den produktionsbereiten Code, während der "develop"-Branch den neuesten Code enthält, an dem gearbeitet wird. Entwickler erstellen Feature-Branches, um an bestimmten Funktionen zu arbeiten, und mergen sie zurück in den "develop"-Branch, sobald die Funktion abgeschlossen ist. Es gibt auch Release-Branches und Hotfix-Branches, die vom "develop"-Branch erstellt werden, um Veröffentlichungen und dringende Fehlerkorrekturen zu handhaben. [12]

        * __Feature, develop, release, hotfix und master branch__
          * Feature Branch: Feature Branches werden verwendet, um neue Features zu entwickeln. Sie werden vom develop-Branch abgezweigt und in den develop-Branch zurückgeführt, wenn die Entwicklung abgeschlossen ist. Feature Branches sollten immer vom develop-Branch abgezweigt werden. Sie sollten niemals direkt vom master-Branch abgezweigt werden. Feature Branches werden in der Regel mit dem Namen feature/feature-name benannt. [0]

          * Develop Branch: Der develop-Branch ist der Hauptentwicklungs-Branch. Er ist der Branch, von dem alle Feature-Branches abgezweigt werden, und der Branch, in den alle Feature-Branches zurückgeführt werden. Der develop-Branch ist der Branch, der für die nächste Veröffentlichung bereit ist. [0]

          * Release Branch: Release-Branches werden verwendet, um eine Veröffentlichung vorzubereiten. Sie werden vom develop-Branch abgezweigt und in den develop- und master-Branch zurückgeführt, wenn die Veröffentlichung abgeschlossen ist. Release-Branches werden in der Regel mit dem Namen release/release-name benannt. [0]

          * Hotfix Branch: Hotfix-Branches werden verwendet, um einen Hotfix zu entwickeln. Sie werden vom master-Branch abgezweigt und in den develop- und master-Branch zurückgeführt, wenn der Hotfix abgeschlossen ist. Hotfix-Branches werden in der Regel mit dem Namen hotfix/hotfix-name benannt. [0]

          * Master Branch: Der master-Branch ist der Haupt-Branch. Er ist der Branch, von dem alle Release-Branches abgezweigt werden, und der Branch, in den alle Release-Branches zurückgeführt werden. Der master-Branch ist der Branch, der für die aktuelle Veröffentlichung bereit ist. [0]

      * __Github Flow__
        Github Flow: Diese Branching-Strategie ist eine vereinfachte Version von Git Flow und wird von Teams verwendet, die häufig Code in die Produktion deployen. Sie beinhaltet die Erstellung eines einzigen langfristigen Branches, nämlich den "main"-Branch, der den produktionsbereiten Code enthält. Entwickler erstellen Feature-Branches, um an bestimmten Funktionen zu arbeiten, und mergen sie zurück in den "main"-Branch, sobald die Funktion abgeschlossen ist. Es gibt keine Release-Branches oder Hotfix-Branches in dieser Strategie. [12]

    * __Merging strategies__
      Ein Merge in Git tritt auf, wenn zwei Branches kombiniert werden. Git sucht nach einem gemeinsamen Basis-Commit zwischen diesen Branches und erstellt dann einen Merge-Commit, der die Änderungen aus den zusammengeführten Commits enthält. Ein Merge-Commit ist im Grunde genommen ein normaler Commit mit zwei Eltern-Commits.
      Git wählt automatisch eine Merge-Strategie aus, es sei denn, sie wird explizit angegeben. Die verfügbaren Merge-Strategien bestimmen, wie Git den gemeinsamen Basis-Commit findet und den Merge durchführt. Die Auswahl der Strategie erfolgt in der Regel automatisch, basierend auf den gegebenen Branches.
      [15]

      * __Merge Commit__
        Beim Mergen von Commits in einem Pull Request auf GitHub.com werden alle Commits aus dem Featurebranch in den Basisbranch in einem zusätzlichen Merge-Commit zusammengeführt. Dieser Merge wird standardmäßig mit der --no-ff-Option durchgeführt.

        Du benötigst Schreibberechtigungen im Repository, um Pull Requests mergen zu können.
        ![](media\standard-merge-commit-diagram.webp)
        In einem Diagramm wird der Standardablauf für Merge- und Commitvorgänge dargestellt, bei dem die Commits aus einem Featurebranch in den Hauptbranch hinzugefügt werden, und es wird ein zusätzlicher Merge-Commit erstellt. [16]

      * __Squash and Merge__
        Beim Squashen und Mergen von Commits in einem GitHub-Pull Request werden alle einzelnen Commits zu einem einzigen zusammengefasst und in den Hauptbranch integriert. Dies schafft einen sauberen Git-Verlauf. Schreibberechtigungen im Repository und die Einstellung zur Unterstützung des Squash-Mergens sind erforderlich. Das ermöglicht eine optimierte Version des Git-Verlaufs, indem alle Arbeitscommits in einem einzigen übersichtlichen Commit konsolidiert werden. 
        ![](media\commit-squashing-diagram.webp)
        [16]

      * __Rebase and Merge__
        Die Option "Rebase und Merge" in einem GitHub-Pull Request ermöglicht das Hinzufügen von Commits aus einem Feature-Branch einzeln und ohne einen separaten Merge-Commit in den Haupt-Branch. Dies führt zu einem linearen Projektverlauf. Es ist wichtig zu beachten, dass das Verhalten von "Rebase und Merge" auf GitHub von "git rebase" außerhalb von GitHub abweicht.

        Um "Rebase und Merge" in einem GitHub-Pull Request durchzuführen, benötigt man Schreibberechtigungen im Repository, und das Repository muss die Option "Rebase und Merge" aktiviert haben.

        Es gibt bestimmte Fälle, in denen automatisches "Rebase und Merge" auf GitHub.com nicht möglich ist, z. B. bei Merge-Konflikten oder Unsicherheiten im Rebase-Prozess. In solchen Fällen kann ein manuelles Rebase in der Befehlszeile durchgeführt werden, gefolgt von der Behebung von Konflikten und einem erzwungenen Push der Rebase-Commits. Personen mit Schreibberechtigungen können dann die Änderungen über die Rebase- und Merge-Option auf GitHub.com zusammenführen. [16]

    * __Aufbau und Inhalt von Commit messages__
      * <https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53>
        Commit-Nachrichten sollten bestimmten Richtlinien folgen:

        Eine kurze Zusammenfassung (maximal 72 Zeichen) und ein detaillierter erläuternder Text (maximal 72 Zeichen pro Zeile).

        Eine leere Zeile, die Zusammenfassung vom Haupttext trennt, es sei denn, der Haupttext fehlt.

        Die erste Zeile ist die wichtigste und sollte den Satz "Wenn angewandt, wird dieser Commit <Ihre Betreffzeile hier>" vervollständigen. Die Betreffzeile sollte großgeschrieben und im Imperativ geschrieben sein.

        Beschreibung des Ziels oder des Grunds für die Änderung in klarem Englisch mit einem Präfix, das auf die Komponente oder die Aufgaben-ID hinweist.

        Wenn sich der Commit auf ein Problem bezieht, sollte dies in der Nachricht vermerkt werden.

        Kein Punkt am Ende der Nachricht, und jede Absatz sollte großgeschrieben sein.

        Keine Patch-Set-spezifischen Kommentare, Beschreibung eventueller Einschränkungen des aktuellen Codes.

        Weitere Absätze sollten nach leeren Zeilen folgen, Aufzählungspunkte sind in Ordnung.

        Konsistente Wortwahl zur Beschreibung von Änderungen ist wichtig.

        Commit-Nachrichten-Linting kann konfiguriert werden, um Standards durchzusetzen und mit semantischer Versionierung übereinzustimmen.

        Das Schreiben guter Commit-Nachrichten erleichtert die Kommunikation und Zusammenarbeit im Team.

        [17]

* __AI-driven development__
  * __Conversational AI vs. Generative AI__
    Conversational AI-Systeme sind auf die Kommunikation mit Benutzern spezialisiert und werden auf kleineren Dialogdatensätzen trainiert. Sie dienen hauptsächlich der Interaktion zwischen Menschen und Maschinen, wobei die Generierung von Antworten nur ein Nebenprodukt ist.

    Generative KI-Tools sind darauf ausgerichtet, originale Inhalte zu erstellen und lernen aus Datenmustern. Ihr Hauptzweck ist die Generierung von einzigartigem Inhalt in verschiedenen Formaten, während die Kommunikation mit Benutzern nicht ihre Hauptfunktion ist. Generative KI ist flexibler und vielseitiger in Bezug auf die Art des erstellten Inhalts. [18]

  * __Prompt engineering__
    Prompt Engineering ist der Prozess der Erstellung von Prompts, die die gewünschten Ergebnisse erzielen. Es ist ein iterativer Prozess, der die Erstellung, das Testen und die Anpassung von Prompts umfasst, um die gewünschten Ergebnisse zu erzielen. [0]

  * __ChatGPT, Github Copilot__
    ChatGPT ist ein leistungsstarkes KI-Modell von OpenAI, das menschenähnlichen Text auf natürliche Weise generieren kann. Es ist ein nützliches Werkzeug für die Texterstellung, Recherche und Unterstützung bei einer Vielzahl von Aufgaben.

    GitHub Copilot ist eine Erweiterung für Visual Studio Code, die von GitHub in Zusammenarbeit mit OpenAI entwickelt wurde. Sie bietet Unterstützung für Entwickler, indem sie intelligente Code-Vervollständigungen, -vorschläge und -dokumentationen bietet. GitHub Copilot ist ein wertvolles Werkzeug für die Softwareentwicklung und kann die Produktivität von Entwicklern erheblich steigern.
      [0]

  * __Best practices für "googling"__
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

    Diese Tipps helfen, genauere und relevantere Suchergebnisse zu erzielen.

    [19]


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
