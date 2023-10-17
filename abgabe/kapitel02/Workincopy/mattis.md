* __Version control systems / Source code management__
  Version Control, auch als Quellcodeverwaltung bezeichnet, ist die Praxis, Änderungen am Software-Code zu verfolgen und zu verwalten. Version-Control-Systeme sind Software-Tools, die Software-Teams dabei helfen, diese Änderungen effizient zu managen, insbesondere in beschleunigten Entwicklungsumgebungen. Sie sind besonders vorteilhaft für DevOps-Teams, da sie die Entwicklungszeit verkürzen und erfolgreiche Bereitstellungen fördern. Diese Software hält jede Code-Änderung in einer speziellen Datenbank fest und ermöglicht es Entwicklern, Fehler zu beheben, indem sie auf frühere Code-Versionen zurückgreifen, ohne die Teammitglieder zu stark zu beeinträchtigen. [1]

  * __Centralized vs Distributed Version Control__
    Zentralisierte Versionskontrolle verlässt sich auf einen zentralen Server, was einfache Einrichtung und Workflow-Kontrolle bietet. Sie hat jedoch Nachteile wie das Risiko eines einzigen Serverausfalls und Schwierigkeiten bei Merging und Branching. Verteilte Versionskontrolle hingegen bietet multiple Backups, ermöglicht Offline-Commits und schnelles Branching, da sie keinen einzelnen Fehlerpunkt hat. Git ist ein bekanntes Beispiel für ein verteiltes Versionskontrollsystem, das in der Softwareentwicklung weit verbreitet ist. [2]

  * __Git__
    Git ist das am weitesten verbreitete moderne Versionskontrollsystem der Welt. Es ist ein ausgereiftes, quelloffenes Projekt, das von Linus Torvalds, dem Schöpfer des Linux-Betriebssystemkernels, entwickelt wurde. Git wird von einer breiten Palette von Softwareprojekten für die Versionskontrolle verwendet und ist bekannt für seine Verteilungsarchitektur, die es Entwicklern ermöglicht, die vollständige Historie ihrer Änderungen in ihren Arbeitskopien zu haben. Git wurde auch mit Schwerpunkt auf Leistung, Sicherheit und Flexibilität entworfen. [3]
    
    * __Remote repositories__
        Remote Repositories sind Versionen des Projekts, die im Internet oder irgendwo im Netzwerk gehostet werden. Sie können mehrere davon haben, von denen jede in der Regel entweder schreibgeschützt oder schreibgeschützt ist. Die Zusammenarbeit mit anderen beinhaltet die Verwaltung dieser remote Repositories und das Übertragen von Daten zu und von ihnen, wenn Sie Arbeit teilen müssen. Die Verwaltung von remote Repositories umfasst das Hinzufügen von remote Repositories, das Entfernen von nicht mehr gültigen Remotes, die Verwaltung verschiedener entfernter Branches und deren Definition als tracked oder untracked, und vieles mehr.


    * __Visualisierung von relevanten git-Kommandos und -Workflows__
      * https://marklodato.github.io/visual-git-guide/index-en.html
      * https://onlywei.github.io/explain-git-with-d3/#
      * __Sequenzdiagramm für git data transfer commands__
        * https://blog.osteele.com/2008/05/my-git-workflow/
    * __Multirepos vs. Monorepos__
    * __Submodules__
    * __Pull requests__
    * __Branching strategies__
      * https://mermaid.js.org/syntax/gitgraph.html
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
      * https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53
* __AI-driven development__
  * __Conversational AI vs. Generative AI__
  * __Prompt engineering__
  * __ChatGPT, Github Copilot__
  * __Best practices für "googling"__


  # Quellen

  [1]: Atlassian. "What is Version Control?" Atlassian Git Tutorial, URL: https://www.atlassian.com/git/tutorials/what-is-version-control (abgerufen am 17. Oktober 2023)

  [2]: GitLab Inc. "Why it’s time to move to a Distributed Version Control System." GitLab Blog, URL: https://about.gitlab.com/blog/2020/11/19/move-to-distributed-vcs/ (abgerufen am 17. Oktober 2023)

  [3]: Atlassian. "What is Git? | Atlassian Git Tutorial." Atlassian, URL: https://www.atlassian.com/git/tutorials/what-is-git (abgerufen am 17. Oktober 2023)