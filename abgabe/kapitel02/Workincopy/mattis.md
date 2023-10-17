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

      * __Trunk-based Development__
      * __Long-lived branches__
      * __Git Flow__
        * __Feature, develop, release, hotfix und master branch__
      * __Github Flow__
    * __Merging strategies__
      * __Merge Commit__
      * __Squash and Merge__
      * __Rebase and Merge__
    * __Aufbau und Inhalt von Commit messages__
      * <https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53>
* __AI-driven development__
  * __Conversational AI vs. Generative AI__
  * __Prompt engineering__
  * __ChatGPT, Github Copilot__
  * __Best practices für "googling"__

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