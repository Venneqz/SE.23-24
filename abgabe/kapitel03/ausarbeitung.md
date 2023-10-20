# Kapitel 3

**Autor:** Marvin Petschulat, Mattis Wellenbüscher

---
#Lernziele:

1. Überblick über Vertilte Softwaresysteme:
  - Eigenschaften, Vorteile, Nachteile
  - Welche Arten von Systemarschitekturen gibt es?
    - Client Server, P2P, EDA, Microservices
  -Wo werden diese Angewendet, und welche Vor- und Nachteile haben diese?
  
2. Überblick über Systemdesign:
  - Api Gateways, Proxys und Load Balancer
  - Was ist bei Skalierungsmustern zu beachten?
    - Skalierung, Replication, Partitioning, Sharding, Load Balancing, Caching
---

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

# Code reading
## How to read code?
Folgen Sie einer "Aktionskette", indem Sie rückwärts von einer bekannten Funktion oder Aktion im Code beginnen und schrittweise herausfinden, wie diese umgesetzt wird. Dadurch gewinnen Sie Einblicke in die Struktur, den Stil und die Denkweise des Entwicklers.

Wiederholen Sie diesen Prozess, um Ihr Verständnis zu erweitern und mehr Teile des Codes zu beleuchten.

Exponieren Sie sich kontinuierlich für hochwertige Codebeispiele und verschiedene Arten von Codes, um Ihr Verständnis zu vertiefen und schneller zu lernen.

Durch die regelmäßige Auseinandersetzung mit Code verbessern Sie nicht nur Ihr Verständnis für den Code anderer, sondern auch Ihre eigenen Programmierfähigkeiten.

Die Wechselwirkung mit qualitativ hochwertigen Codebeispielen und die Erlangung von Expertenwissen sind entscheidend, um ein tieferes Verständnis und intuitive Fähigkeiten im Umgang mit Code zu entwickeln.

Dieser Lernprozess erstreckt sich über die Zeit und führt zu weniger Unterbrechungen, schnellerem Fortschritt und mehr Spaß beim Programmieren.

Es wird empfohlen, qualitativ hochwertige Codebeispiele in Lernmaterialien oder von Experten zu nutzen, um Ihr Verständnis zu beschleunigen und sich mit verschiedenen Programmieransätzen vertraut zu machen.

Das kontinuierliche Lernen und die Anwendung dieser Prinzipien helfen dabei, Code effektiver zu lesen und zu verstehen und gleichzeitig Ihre eigenen Fähigkeiten zu verbessern.

[20]


# Bug report writing
## Best practices

Wie schreibe ich einen Fehlerbericht?
Ein guter Fehlerbericht sollte es dem Entwickler und dem Management ermöglichen, das Problem zu verstehen. Zu den zu berücksichtigenden Richtlinien gehören:

1. Alle relevanten Informationen müssen mit dem Fehlerbericht bereitgestellt werden
Zur Beschreibung des Fehlers sollten einfache Sätze verwendet werden. Für erfahrene Tester ist das Melden von Fehlern nichts weniger als eine Fertigkeit. Wir haben einige Tipps zusammengestellt, die Testern helfen, diese besser zu meistern:

2. Reproduzierbare Fehler melden:
Beim Melden eines Fehlers muss der Tester sicherstellen, dass der Fehler reproduzierbar ist. Die Schritte zur Reproduktion des Fehlers müssen erwähnt werden. Alle Voraussetzungen für die Ausführung von Schritten und alle Testdatendetails sollten dem Fehler hinzugefügt werden.

3. Seien Sie prägnant und klar:
Versuchen Sie, das Problem in wenigen Worten zusammenzufassen, kurz, aber umfassend. Vermeiden Sie es, lange Beschreibungen des Problems zu verfassen.

Beschreiben Sie das Problem in Stichworten und vermeiden Sie Absätze. Es ist wichtig, alle relevanten Informationen bereitzustellen, und es hilft den Entwicklern, das Problem zu verstehen, ohne dass zusätzliches Hin und Her über den Fehler entsteht. Der Entwickler muss das zugrunde liegende Problem anhand des Fehlerberichts klar verstehen.

4. Melden Sie Fehler frühzeitig:
Es ist wichtig, Fehler zu melden, sobald Sie sie finden. Eine frühzeitige Meldung des Fehlers hilft dem Team, den Fehler frühzeitig zu beheben und das Produkt frühzeitig auszuliefern.

5. Vermeiden Sie Rechtschreib- und Sprachfehler:
Lesen Sie alle Sätze Korrektur und überprüfen Sie die Problembeschreibung auf Rechtschreib- und Grammatikfehler.

Bei Bedarf kann man Tools von Drittanbietern nutzen, z.B. Grammatikalisch. Dies hilft dem Entwickler, den Fehler ohne Mehrdeutigkeit und Falschdarstellung zu verstehen.

6. Dokumentation zeitweiliger Probleme:
Manchmal sind nicht alle Fehler reproduzierbar. Sie haben bestimmt bemerkt, dass eine mobile App manchmal abstürzt und Sie die App neu starten müssen, um fortzufahren. Diese Art von Fehlern ist nicht jedes Mal reproduzierbar.

In solchen Fällen müssen Tester versuchen, ein Video des Fehlers zu erstellen und es dem Fehlerbericht beizufügen. Ein Video ist oft hilfreicher als ein Screenshot, da es Details zu Schritten enthält, die schwer zu dokumentieren sind.

Beispielsweise stürzt eine mobile App ab, während zwischen Anwendungen gewechselt wird oder eine App in den Hintergrund verschoben und in den Vordergrund gebracht wird.

7. Vermeiden Sie die Wiederholung von Fehlern:
Beim Melden eines Fehlers muss sichergestellt werden, dass der Fehler keinen bereits gemeldeten Fehler dupliziert. Überprüfen Sie außerdem die Liste der bekannten und offenen Probleme, bevor Sie Fehler melden. Das Melden doppelter Fehler könnte den Entwicklern doppelten Aufwand kosten und sich somit auf den Testlebenszyklus auswirken .

8. Erstellen Sie separate Fehler für nicht zusammenhängende Probleme:
Wenn im selben Fehler mehrere Probleme gemeldet werden, kann er nicht geschlossen werden, es sei denn, alle Probleme wurden behoben. Daher sollten separate Fehler erstellt werden, wenn Probleme nicht miteinander zusammenhängen.

Angenommen , ein Tester stößt in einer Anwendung in verschiedenen Modulen auf zwei Probleme. Ein Problem besteht in der Funktion zum Verfassen von E-Mails, bei der der Benutzer keine E-Mail verfassen kann, und ein anderes Problem besteht darin, dass der Benutzer keine E-Mail drucken kann. Diese Themen müssen separat angesprochen werden, da sie unabhängig voneinander sind.

9. Verwenden Sie keinen autoritativen Ton:
Vermeiden Sie bei der Dokumentation des Fehlers einen befehlenden Ton, harte Worte und machen Sie sich nicht über den Entwickler lustig.

Das Ziel eines guten Fehlerberichts besteht darin, dem Entwickler und dem Management zu helfen, den Fehler und seine Auswirkungen auf das System zu verstehen. Je genauer und detaillierter der Fehlerbericht ist, desto schneller und effektiver kann der Fehler behoben werden. Schreibe das ein wenig um und kürze wenn es geht.

[21] https://testsigma.com/blog/how-to-write-a-good-bug-report-some-tips/#How_to_Write_a_Bug_Report


# Debugging

Definition: Debugging ist der Prozess der Identifizierung, Lokalisierung und Behebung von Fehlern, Fehlfunktionen oder Problemen in einer Softwareanwendung oder einem Programmcode.
[3 Chatgpt]
## Problem solving, Root cause analysis
Problem solving:
Definition: Problem solving ist der allgemeine Prozess, bei dem Probleme oder Herausforderungen erkannt, analysiert und gelöst werden, sei es in der Softwareentwicklung oder in anderen Bereichen.

Ziel: Das Hauptziel des Problem solving besteht darin, eine nachhaltige Lösung für ein Problem zu finden und sicherzustellen, dass es nicht erneut auftritt.

Methoden: Problem solving kann verschiedene Techniken und Ansätze umfassen, darunter das Identifizieren von Ursachen (Root Cause Analysis), das Entwickeln von Lösungen, das Implementieren von Veränderungen und das Überwachen der Wirksamkeit.

Herausforderungen: Die Herausforderungen beim Problem solving umfassen die genaue Identifizierung des Problems, das Finden geeigneter Lösungen und die Gewährleistung, dass die Lösung effektiv ist und langfristig hält.

Debugging und Problem solving sind entscheidende Fähigkeiten in der Softwareentwicklung und im IT-Bereich. Während Debugging speziell auf die Behebung von Fehlern in der Software ausgerichtet ist, ist Problem solving ein breiteres Konzept, das die Bewältigung von Herausforderungen und die Identifizierung von Lösungen in verschiedenen Kontexten umfasst. Beide sind integraler Bestandteil des Entwicklungsprozesses, um qualitativ hochwertige und zuverlässige Software zu erstellen.
[21]

Root cause analysis:
Die Root Cause Analysis (RCA) ist ein wichtiger Prozess, um die grundlegende Ursache eines Problems zu identifizieren und nicht nur seine Symptome zu behandeln. Um eine RCA erfolgreich durchzuführen, können folgende Schritte befolgt werden:

Definition des Problems: Klar definieren, welches Problem oder welche Herausforderung gelöst werden muss.

Problemreproduktion: Das Problem in einer kontrollierten Umgebung reproduzieren, um mögliche Ursachen einzugrenzen.

Code-Analyse: Den Programmcode überprüfen, um mögliche Fehler oder Probleme zu identifizieren, die das Problem verursachen könnten.

Testen und Debuggen: Test- und Debugging-Tools verwenden, um die Wurzelursache zu ermitteln. Dies beinhaltet das schrittweise Durchgehen des Codes und das Ausführen von Testfällen.

Überprüfen von Fehlermeldungen und Protokollen: Alle relevanten Fehlermeldungen und Protokolle auf Hinweise zur Wurzelursache überprüfen.

Konsultation von Kollegen: Den Austausch mit Kollegen oder erfahrenen Programmierern suchen, um die Wurzelursache zu identifizieren.

Lösungsentwicklung: Eine Lösung entwickeln, die die Wurzelursache des Problems angeht, sei es durch Codeänderungen oder die Implementierung neuer Prozesse.

Lösungstest und Validierung: Die entwickelte Lösung testen, um sicherzustellen, dass sie das Problem effektiv behebt und keine neuen Probleme verursacht.

Dokumentation der Ergebnisse: Die Ergebnisse der RCA dokumentieren, einschließlich der identifizierten Wurzelursache und der implementierten Lösung, um zukünftige Problemlösungen zu unterstützen und die Codequalität zu verbessern.

Es ist wichtig, relevante Stakeholder, wie das Management, Kunden und Aufsichtsbehörden, über die RCA und die ergriffenen Maßnahmen zur Problemlösung zu informieren.

Die Vorteile der RCA umfassen eine verbesserte Problemlösung, erhöhte Effizienz, verbesserte Qualität des Codes und eine Verringerung des Risikos zukünftiger Probleme. Nachteile können die zeitaufwändige Natur des Prozesses, zusätzliche Ressourcenanforderungen und die Komplexität der Probleme sein.
[23] 

## Debugging vs. Testen
Testen und Debugging sind zwei unerlässliche Prozesse in der Softwareentwicklung, die jeweils unterschiedliche Ziele und Zeitpunkte haben. Beim Testen geht es darum, sicherzustellen, dass eine Software den festgelegten Anforderungen entspricht und etwaige Fehler aufzudecken. Dieser Prozess kann von Entwicklern, Testern und Endbenutzern durchgeführt werden und beginnt nach Abschluss der Softwareentwicklung.

Auf der anderen Seite ist Debugging ein reaktiver Prozess, bei dem Entwickler vorhandenen Code durchsuchen, um Fehler zu finden und zu beheben. Es startet, sobald Fehler während des Testvorgangs erkannt werden und ist in der Regel Aufgabe der Entwickler. Die Werkzeuge unterscheiden sich ebenfalls: Testen nutzt Testautomatisierungs- und Testmanagement-Tools, während Debugging Debugger, Profiler und andere Debugging-Tools einsetzt.

Insgesamt sind Testen und Debugging unterschiedliche Ansätze in der Softwarequalitätskontrolle. Während Testen darauf abzielt, Qualitätsmängel zu verhindern, konzentriert sich Debugging auf die Identifizierung und Behebung von Fehlern in existierendem Code. Beide Prozesse sind entscheidend, um qualitativ hochwertige Softwareprodukte bereitzustellen und das Vertrauen der Benutzer zu gewinnen.

[24] 

## Rubber Duck Debugging
Der Ansatz des "Rubber Duck Debugging" ist eine humorvolle und dennoch effektive Methode zum Lösen von Programmierproblemen. Diese Methode beinhaltet die Verwendung einer Badeente als imaginären Gesprächspartner, um Code-Fehler zu finden und zu beheben. Der Prozess sieht folgendermaßen aus:

Holen Sie sich eine Badeente (Badewannenversion), sei es durch Leihen, Kaufen oder andere Mittel.

Stellen Sie die Gummiente auf Ihren Schreibtisch und erklären Sie ihr, dass Sie beabsichtigen, Ihren Code mit ihrer Hilfe zu durchgehen.

Beginnen Sie damit, der Ente zu erklären, was Ihr Code tun soll. Gehen Sie anschließend detailliert vor und erläutern Sie Ihren Code Zeile für Zeile.

Während des Erklärungsprozesses werden Sie oft feststellen, dass Sie sich vertun oder herausfinden, dass das, was Sie tatsächlich tun, nicht dem entspricht, was Sie zuvor beabsichtigt hatten. Die Ente sitzt still da, zufrieden mit dem Wissen, dass sie Ihnen geholfen hat, den Fehler zu identifizieren.

Hinweis: Wenn nötig, kann ein Kollege die Ente ersetzen, aber oft ist es effektiver, die Ente um Hilfe zu bitten, bevor Sie Kollegen involvieren.

Die Methode des "Rubber Duck Debugging" mag auf den ersten Blick amüsant erscheinen, hat sich jedoch als nützliche Möglichkeit erwiesen, um festgefahrene Gedanken zu klären und Codierfehler zu finden. Das Erklären des Codes laut hilft Entwicklern, die zugrunde liegenden Probleme zu erkennen und Lösungen zu finden, selbst wenn der Gesprächspartner nur aus Kunststoff ist.

[25]

## Time-travel debugging (reverse debugging)
Zeitreise-Debugging, auch als Reverse Debugging bekannt, ermöglicht Entwicklern, die gesamten Aktivitäten eines laufenden Programms aufzuzeichnen und dann rückwärts und vorwärts durch die Aufzeichnung zu navigieren, um den Programmstatus zu überprüfen. Im Vergleich zu herkömmlichen Debuggern, die nur Vorwärts-Debugging unterstützen, eignet sich Zeitreise-Debugging besonders für schwer reproduzierbare Fehler und große Anwendungen.

Mit herkömmlichen Debuggern kann ein Entwickler Schritt für Schritt durch den Code gehen, was bei einfachen Fehlern effektiv sein kann. Bei schwer reproduzierbaren Fehlern, bei denen der Fehlerort unbekannt ist, ist dies jedoch schwierig. Zeitreise-Debugger ermöglichen es, die Ausführung rückwärts zu verfolgen, um die Ursache des Fehlers an verschiedenen Stellen des Programms zu finden.

Das Zeitreise-Debugging erfordert eine Aufzeichnung der Programmausführung, einschließlich Fehler und der Abfolge von Ereignissen, die dazu geführt haben. Dies kann die Leistung beeinträchtigen, wobei die Verlangsamung je nach verwendetem Zeitreise-Debugger variiert.

Die Anwendung von Zeitreise-Debugging ist prinzipiell in allen Programmiersprachen möglich, wobei die Unterstützung in GDB-kompatiblen Sprachen wie C/C++, Go und Fortran am häufigsten ist. Es gibt auch spezielle Zeitreise-Debugging-Tools für andere Sprachen wie Python und JavaScript.

Insgesamt ermöglicht Zeitreise-Debugging Entwicklern, effektiv schwerwiegende Fehler zu beheben, indem sie die Ausführung des Programms rückwärts verfolgen können, um die Wurzel des Problems zu finden. Dies ist besonders nützlich bei komplexen und schwer zu reproduzierenden Fehlern.
[26]

## Logging / Tracing
Protokollierung (Logging):

Logging ist die grundlegendste Form der Anwendungsüberwachung und dient der Identifizierung von Vorfällen oder Fehlern.
Dabei werden zeitgestempelte Daten verschiedener Anwendungen oder Dienste in regelmäßigen Abständen aufgezeichnet.
Loggingebenen wie FATAL, ERROR, WARN, DEBUG, INFO, TRACE und ALL helfen dabei, wichtige Informationen aus den Logging zu filtern.
Logging sind oft unstrukturiert und erfordern spezielle Tools zur Analyse.

Tracing:

In modernen verteilten Softwarearchitekturen, in denen viele Anwendungen miteinander interagieren, ist es wichtig zu verstehen, wie Daten durch das gesamte System fließen.
Tracing zeichnet den Weg einer Anfrage von Anfang bis Ende auf, einschließlich der Interaktion mit verschiedenen Diensten und der Messung der Latenz.
Dies ermöglicht es, den Kontext einer Anfrage zu verstehen und Abweichungen vom normalen Verhalten der Anwendung zu analysieren.
Wann man Logging und Tracing verwenden sollte:

Logging ist unerlässlich für die tägliche Überwachung von Anwendungen und sollte immer aktiviert sein, um Probleme zu identifizieren.
Tracing ist nützlich, um bei der Fehlerbehebung schnell zur Ursache von Problemen zu gelangen, sollte jedoch nicht kontinuierlich verwendet werden, da dies die Leistung beeinträchtigen kann.
Eine effektive Observability-Strategie in verteilten Systemen sollte Platz für beides bieten, da sie unterschiedliche Zwecke erfüllen.
Zusammenfassend ist Logging für die Überwachung von Anwendungen und die Identifizierung von Problemen im täglichen Betrieb unerlässlich, während Tracing bei der schnellen Fehlerbehebung und der Zuordnung von Problemen zu spezifischen Anwendungen oder Diensten hilfreich ist. Eine ausgewogene Kombination von Logging und Tracing ist in verteilten Architekturen empfehlenswert.
[27]

## Ablauf des Debuggings
Reproduktion des Problems: Zunächst muss der Entwickler das Problem reproduzieren, um sicherzustellen, dass es tatsächlich besteht. Dies erfordert oft eine genaue Überprüfung der Schritte oder Bedingungen, die zum Auftreten des Fehlers führen.

Fehlererkennung: Sobald das Problem reproduziert wurde, erfolgt die Erkennung des Fehlers. Dies kann bedeuten, den fehlerhaften Codebereich zu lokalisieren oder festzustellen, welche Aktionen des Programms zu unerwünschtem Verhalten führen.

Code-Inspektion: Der Entwickler analysiert den Code sorgfältig, um den Fehler zu finden. Dies kann das Durchsuchen von Quellcode, das Überprüfen von Variablenwerten und das Identifizieren von Inkonsistenzen im Code einschließen.

Hypothesenbildung: Basierend auf der Analyse des Codes werden Hypothesen darüber aufgestellt, was den Fehler verursachen könnte. Dies kann auf logischen Schlussfolgerungen und Erfahrung basieren.

Testen von Hypothesen: Die aufgestellten Hypothesen werden getestet, um festzustellen, ob sie den Fehler erklären. Dies kann das Hinzufügen von Debugging-Anweisungen, das Ändern von Code oder das erneute Ausführen des Programms unter verschiedenen Bedingungen beinhalten.

Schritt-für-Schritt-Debugging: Ein häufiger Ansatz beim Debuggen ist das schrittweise Durchgehen des Codes, Zeile für Zeile, um festzustellen, an welcher Stelle der Fehler auftritt. Dies kann mit Hilfe von Debugging-Tools und Breakpoints erfolgen.

Überprüfung der Annahmen: Während des Debugging-Prozesses ist es wichtig, kontinuierlich die angenommenen Ursachen für den Fehler zu überprüfen und sicherzustellen, dass sie korrekt sind.

Korrekturen und Tests: Sobald der Fehler gefunden ist, werden entsprechende Korrekturen im Code vorgenommen. Anschließend wird das Programm erneut getestet, um sicherzustellen, dass der Fehler behoben ist und keine neuen Probleme auftreten.

Dokumentation: Eine wichtige, aber oft übersehene Phase des Debuggings ist die Dokumentation. Der Entwickler sollte den gefundenen Fehler, die durchgeführten Änderungen und die Lösung des Problems protokollieren.

Verifikation und Validierung: Nach der Fehlerbehebung sollte das Programm gründlich überprüft und validiert werden, um sicherzustellen, dass der Fehler nicht wieder auftritt und dass keine neuen Probleme entstanden sind.

Rückmeldung und Berichterstattung: In vielen Fällen ist es wichtig, das Debugging-Ergebnis zu dokumentieren und gegebenenfalls Informationen an das Entwicklungsteam oder die relevanten Stakeholder weiterzugeben.

Der Debugging-Prozess kann je nach den Umständen komplex sein und erfordert oft Geduld, analytisches Denken und eine systematische Herangehensweise, um erfolgreich zu sein. Debugging-Tools und -Techniken, einschließlich Breakpoints, Protokollierung und Testumgebungen, können Entwicklern dabei helfen, den Prozess effizienter zu gestalten.
[22]
## Beispiel Debugging
Nullzeiger-Ausnahmen (NullPointerException):

Problem: Das Programm stürzt ab, weil auf eine Variable oder ein Objekt zugegriffen wird, die/das den Wert "null" hat.
Debugging: Setzen Sie Breakpoints und überprüfen Sie die Werte von Variablen, um den Ort zu identifizieren, an dem die Variable null ist. Stellen Sie sicher, dass die Variable ordnungsgemäß initialisiert wurde.
Endlosschleifen:

Problem: Das Programm bleibt in einer Schleife stecken und führt den Code immer wieder aus.
Debugging: Fügen Sie Breakpoints in der Schleife hinzu und verfolgen Sie den Fluss des Programms, um den Grund für die Endlosschleife zu finden. Überprüfen Sie die Bedingungen, die zum Beenden der Schleife führen sollen.
Falsche Ergebnisse bei Berechnungen:

Problem: Das Programm gibt unerwartete oder fehlerhafte Ergebnisse aus.
Debugging: Verwenden Sie Debugging-Anweisungen, um Zwischenergebnisse anzuzeigen. Überprüfen Sie mathematische Berechnungen und Vergleiche, um sicherzustellen, dass sie korrekt sind.
Fehlerhafte Benutzereingaben:

Problem: Das Programm akzeptiert Benutzereingaben, die ungültig oder unerwartet sind.
Debugging: Überwachen und validieren Sie Benutzereingaben. Verwenden Sie Protokollierung, um Eingaben und Verarbeitungsschritte nachzuverfolgen.
Fehler in Schleifen und Bedingungen:

Problem: Schleifen oder bedingte Anweisungen verhalten sich nicht wie erwartet.
Debugging: Setzen Sie Breakpoints innerhalb der Schleifen oder vor bedingten Anweisungen, um den Code schrittweise auszuführen. Überprüfen Sie die Werte von Schleifenvariablen und Bedingungen.
Fehler in Multithreading-Anwendungen:

Problem: In einer Anwendung mit mehreren Threads treten unvorhersehbare Wettlaufbedingungen oder Deadlocks auf.
Debugging: Verwenden Sie spezielle Debugging-Tools für Multithreading, um den Zustand der Threads zu überwachen und Probleme in der Koordination zu identifizieren.
Fehler in der Benutzeroberfläche (UI):

Problem: Die Benutzeroberfläche verhält sich fehlerhaft oder zeigt unerwartete Anzeigeelemente.
Debugging: Überprüfen Sie das UI-Code-Teil und setzen Sie Breakpoints, um den Programmfluss zu verfolgen. Stellen Sie sicher, dass Ereignishandler korrekt konfiguriert sind.
Probleme in der Datenbankkommunikation:

Problem: Das Programm kann keine Verbindung zur Datenbank herstellen oder erhält falsche Daten.
Debugging: Überprüfen Sie die Datenbankverbindungsparameter und Protokolle. Verwenden Sie SQL-Abfrage-Protokollierung, um Datenbankinteraktionen nachzuverfolgen.
Diese Beispiele veranschaulichen typische Situationen, in denen Debugging notwendig ist. Die Wahl der Debugging-Tools und -Techniken hängt von der Programmiersprache, der Entwicklungsplattform und der Art des Problems ab. Ein systematischer Ansatz, bei dem Sie schrittweise den Code durchgehen und wichtige Variablen und Zustände überwachen, ist in den meisten Fällen hilfreich.
[22]

## Debugging Werkzeuge
Trace32 von Lauterbach: Trace32 bietet Hardware- und Software-Tools. Es basiert auf einem modularen Konzept, das universelle Basismodule und architekturspezifische Kabel kombiniert. Entwickler können den "PowerDebug PRO" verwenden, der USB-3.0- und GbE-Anschlüsse bietet und für das Debuggen von verschiedenen Architekturen geeignet ist. Dieses Tool ermöglicht eine umfassende Analyse des Programmablaufs.

ULINKplus von Arm Keil: ULINKplus ist ein Debugger, Leistungsmessgerät und I/O-Schnittstelle in einem Gerät. Es bietet Einblicke in die Funktion, das Timing und die Leistungsaufnahme von Embedded-Anwendungen. Entwickler können es an Arm-Cortex-basierte Geräte anschließen und Funktionen wie SWV-Trace und Multi-Core-Debugging nutzen.

J-Link von Segger: J-Link ist ein Hardware-Debugger, der bis zu 3 Mbyte/s RAM-Download-Geschwindigkeit bietet und eine unbegrenzte Anzahl von Breakpoints im Flash-Speicher von MCUs unterstützt. Es kann mit verschiedenen CPUs und Architekturen verwendet werden und bietet Software-Tools wie Embedded Studio, System View und Ozone.

Universal Debug Engine (UDE) von PLS Programmierbare Logik & Systeme: Die UDE ist ein Software-Tool für die Systemanalyse, Tests und Debugging von High-End-SoCs und eingebetteten Multicore-Systemen. Es ermöglicht das Darstellen von Systemzuständen, das Setzen von Breakpoints und die Laufzeitanalyse. Die UDE unterstützt verschiedene Architekturen und bietet Funktionen wie Trace, Profiling und Code-Coverage-Analyse.

Diese Debugging-Werkzeuge helfen Entwicklern, Softwarefehler zu identifizieren, zu isolieren und zu beheben, um sicherzustellen, dass ihre Software fehlerfrei und leistungsstark ist. Sie bieten eine breite Palette von Funktionen, die von Hardware-Debugging bis hin zu Software-Simulation reichen, je nach den Anforderungen des Entwicklungsprojekts.
[28]

# Agile testing workflows 
Agiles Testen ist eine Testpraxis, die den Regeln und Prinzipien der agilen Softwareentwicklung folgt. Im Gegensatz zur Wasserfallmethode kann Agile Testing bereits zu Beginn des Projekts mit einer kontinuierlichen Integration zwischen Entwicklung und Test beginnen. Die agile Testmethode ist nicht sequentiell (in dem Sinne, dass sie erst nach der Codierungsphase ausgeführt wird), sondern kontinuierlich.

Die Prinzipien des agilen Testens betonen die Zusammenarbeit, kontinuierliche Verbesserung und die Integration von Entwicklung und Test. Der agile Testlebenszyklus umfasst Phasen wie Anforderungsschätzung, Testplanung, Release-Vorbereitung und Übergang. Agile Tests erfolgen in verschiedenen Quadranten, die interne Codequalität, Geschäftsorientierung, Feedback und nicht-funktionale Anforderungen abdecken. Es gibt auch Herausforderungen im agilen Testen, einschließlich hoher Fehlerwahrscheinlichkeit und der Notwendigkeit einer effektiven Testautomatisierung. Insgesamt dient Agile Testing dazu, die Qualität und Anpassungsfähigkeit von Softwareprodukten in agilen Umgebungen sicherzustellen.

[29]
## TDD, BDD, ATDD
Testgetriebene Entwicklung (TDD) ist eine Methode, bei der Entwickler automatisierte Testfälle vor der Codierung schreiben und den Code so anpassen, dass die Tests erfolgreich durchlaufen werden. BDD (Behavioral-Driven Development) ist eine Erweiterung von TDD, die den Schwerpunkt auf das Verhalten eines Systems legt und Testfälle in natürlicher Sprache mit "Given-When-Then" formuliert. ATDD (Acceptance Test-Driven Development) ähnelt BDD, konzentriert sich jedoch mehr auf das Erfassen genauer Anforderungen und verbessert die Zusammenarbeit zwischen Entwicklern, Kunden und Qualitätssicherungskräften.

Die Unterschiede zwischen TDD, BDD und ATDD liegen in den beteiligten Personen, der verwendeten Sprache, dem Hauptaugenmerk und den verwendeten Tools. TDD ist stark auf Entwickler ausgerichtet, verwendet die Programmiersprache des Systems und konzentriert sich auf Unit-Tests. BDD bezieht Kunden und QA-Teams ein, verwendet eine einfache natürliche Sprache und betont das Verhalten des Systems. ATDD ist ähnlich wie BDD, legt jedoch mehr Wert auf die Erfassung genauer Anforderungen und die Verwendung von Abnahmetests. Je nach Projekt und Anforderungen kann eine dieser Methoden oder eine Kombination am effizientesten sein.

[30] https://www.browserstack.com/guide/tdd-vs-bdd-vs-atdd

### Motivation, Ablauf, Inhalte, Frameworks
Test-Driven Development (TDD):

Motivation:
TDD zielt darauf ab, die Qualität der Software zu verbessern, indem Entwickler zuerst Tests schreiben, bevor sie neuen Code hinzufügen. Dieser Ansatz reduziert Fehler, fördert die frühzeitige Fehlererkennung und erhöht die Gesamtqualität der Anwendung.

Ablauf:

Ein Entwickler schreibt automatisierte Tests für eine bestimmte Funktion oder ein Feature.
Diese Tests werden ausgeführt und sollten fehlschlagen, da das Feature noch nicht implementiert ist.
Der Entwickler schreibt den Code, um die Tests bestehen zu lassen.
Dieser Zyklus wird wiederholt, um schrittweise Funktionen zu entwickeln und sicherzustellen, dass bestehender Code funktioniert.
Inhalte:

TDD konzentriert sich auf Unit-Tests, bei denen einzelne Teile des Codes getestet werden.
Die Tests beschreiben erwartetes Verhalten und spezifizieren die Funktionalität der Software.
Frameworks:

Gängige Frameworks für TDD sind JUnit (für Java), pytest (für Python) und NUnit (für .NET).
Behavior-Driven Development (BDD):

Motivation:
BDD konzentriert sich auf das Verhalten der Software aus Sicht der Benutzer, um die Kommunikation zwischen Entwicklern, Testern und Stakeholdern zu verbessern und eine gemeinsame Sprache für die Anforderungen zu schaffen.

Ablauf:

Anhand von "Given-When-Then" Szenarien wird das erwartete Verhalten der Software beschrieben.
Automatisierte Tests werden basierend auf diesen Szenarien geschrieben und ausgeführt.
Inhalte:

Die Tests sind benutzerorientiert und beschreiben, wie die Anwendung sich aus Benutzersicht verhalten sollte.
Frameworks:

Beliebte BDD-Frameworks sind Cucumber, SpecFlow, und Behave.
Acceptance Test-Driven Development (ATDD):

Motivation:
ATDD konzentriert sich auf die Erfassung genauer Anforderungen und die Verbesserung der Zusammenarbeit zwischen Entwicklern, Testern und Stakeholdern, um sicherzustellen, dass die Software die Bedürfnisse der Benutzer erfüllt.

Ablauf:

Akzeptanztests werden aus Benutzersicht erstellt, um die funktionalen Anforderungen klar zu definieren.
Diese Tests werden automatisiert und als Messlatte für die Entwicklung verwendet.
Inhalte:

Die Tests spezifizieren, wie die Anwendung aus Benutzersicht funktionieren soll.
Frameworks:

ATDD kann mit denselben Frameworks wie BDD (z.B. Cucumber und SpecFlow) implementiert werden.
Diese Zusammenfassung bietet eine kurze Übersicht über die Motivation, den Ablauf, die Inhalte und die gängigen Frameworks für jede der genannten agilen Testmethoden.
[22]

## Test doubles
Testdoubles sind in agilen Test-Workflows, wie TDD, von entscheidender Bedeutung. Sie werden verwendet, um das Verhalten echter Abhängigkeiten zu simulieren und dienen dazu, die zu testende Codeeinheit von anderen Teilen des Systems zu isolieren. Dies ermöglicht schnellere und zuverlässigere Tests und fördert besseres Design, Feedback und Kommunikation. Testdoubles machen den Einsatz externer Ressourcen, wie Datenbanken oder Webdienste, überflüssig und helfen bei der klaren Definition von Anforderungen.

Der Prozess der Verwendung von Testdoubles in TDD beginnt mit dem Schreiben eines fehlgeschlagenen Tests, in dem das gewünschte Verhalten beschrieben wird. Testdoubles ersetzen alle nicht relevanten oder nicht verfügbaren Abhängigkeiten. Dann wird die minimale Menge an Code geschrieben, damit der Test besteht, und die Testdoubles dienen als Leitfaden für die Interaktionen zwischen dem Code und seinen Abhängigkeiten.

Die Verwendung von Testdoubles sollte in TDD in folgenden Situationen in Betracht gezogen werden:

Wenn Sie eine Codeeinheit isoliert von ihren Abhängigkeiten testen möchten.
Um verschiedene Szenarien oder Grenzfälle zu testen, die mit echten Abhängigkeiten schwer oder gar nicht zu reproduzieren sind.
Um den Testprozess zu beschleunigen oder zu vereinfachen und Zeit und Ressourcen zu sparen.
Die Auswahl des richtigen Testdoubles hängt von Faktoren wie Komplexität, Kontrolle, Abstraktion und Realismus ab. Tools und Frameworks wie Mockito, JUnit, Sinon, Jest und RSpec stehen zur Verfügung, um Testdoubles zu erstellen. Die Wahl des richtigen Testdoubles hängt von den Anforderungen ab und soll eine verbesserte Codierung ermöglichen.

Zusammenfassend unterstützen Testdoubles agile Test-Workflows, indem sie die Isolation von Codeeinheiten erleichtern und bessere Tests, Design-Praktiken und Kommunikation fördern.
[31] https://www.linkedin.com/advice/3/how-do-you-use-test-doubles-mocks-stubs

### Mocks vs Fakes vs Stubs vs Spy
Mock:
Ein Mock ist ein Objekt, das sowohl indirekte Eingabe als auch Ausgabe steuern kann und über einen Mechanismus zur automatischen Durchsetzung von Erwartungen und Ergebnissen verfügt .

Stellen Sie sich vor, die ShoppingCart-Klasse ruft die Datenbank auf und führt große und komplexe Funktionen aus. Aus diesem Grund können wir diese Klasse aufgrund der Kopplung nicht korrekt einem Unit-Test unterziehen.
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
In solchen Situationen ist Mocking die beste Option, wenn wir diese Klasse nicht einfach ändern können (vielleicht wird die Klasse in verschiedenen Teilen verwendet) und die Umgestaltung zu lange dauern könnte.

Meine Lieblingslösung hierfür ist „ Extract Method Refactoring “:
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
Fake:
Ein Fake ist eine einfachere Umsetzung realer Objekte.

Fakes werden verwendet, wenn wir eine Infrastrukturklasse testen möchten. Mit anderen Worten: Fakes gelten für Klassen, die außerhalb unseres Anwendungslimits liegen (z. B. Repositorys oder Warteschlangen).

Wie Sie im ersten Bild (dem Diagramm) sehen können, befindet sich ein Fake nicht in der hierarchischen Linie innerhalb von Dummy, Stub, Spy oder Mock. Dies liegt daran, dass sich ein Fake für unseren konkreten Anwendungsfall wie ein Dummy, Stub, Spion oder Spott verhalten kann.
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
Wenn wir also dieses gefälschte Repository verwenden, erhalten wir einen Stub-Benutzer.

Stub:
Ein Stub ist ein Objekt, das gefälschte Daten zurückgibt.

Stellen wir uns vor, unser Dienst hängt von einem Benutzermodell ab, dann führt der Dienst etwas aus und gibt schließlich die UUID des Benutzers zurück. Wir können ein Stub-Objekt mit gefälschten Werten erstellen, um sicherzustellen, dass der Dienst wie erwartet funktioniert.
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

Spy
Ein Testspy ist ein Objekt, das in der Lage ist, indirekte Ausgaben zu erfassen und bei Bedarf indirekte Eingaben bereitzustellen. Der indirekte Output ist etwas, das wir nicht direkt beobachten können.

Dies können wir erreichen, indem wir die ursprüngliche Klasse erweitern und die Funktionsparameter als Klassenargumente speichern.

Im folgenden Snippet können wir genau erfahren, wie oft die log()-Methode aufgerufen wurde und welchen Inhalt die Nachrichten haben. Der Sinn dieses Spions besteht darin, im Gegenzug für eine tiefere Kopplung viel mehr Wissen über den internen Objektzustand zu haben, was in Zukunft problematisch sein könnte, weil es unsere Tests fragiler macht.
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
[32]

### Frameworks
Test Double Frameworks, auch als Mocking Frameworks oder Test Frameworks bezeichnet, sind Tools oder Bibliotheken, die in der Softwareentwicklung und im Softwaretesten verwendet werden, um Testdoubles zu erstellen und zu verwalten. Diese Frameworks erleichtern die Erstellung von Dummy-Objekten, Stubs, Mocks und Spies, die in Unit-Tests und Integrationstests verwendet werden, um die Abhängigkeiten einer Codeeinheit zu ersetzen und deren Verhalten zu steuern. Hier sind einige wichtige Informationen zu Test Double Frameworks:

Erstellung von Testdoubles: Test Double Frameworks bieten Funktionen zur einfachen Erstellung von Testdoubles. Entwickler können spezielle Methoden oder Annotationen verwenden, um Mocks, Stubs oder andere Testdoubles zu erstellen.

Verhaltensdefinition: Diese Frameworks ermöglichen es, das erwartete Verhalten der Testdoubles festzulegen. Dies umfasst, wie oft Methoden aufgerufen werden sollten, welche Rückgabewerte sie liefern sollen und wie sie auf Eingaben reagieren sollen.

Integration mit Test-Frameworks: Test Double Frameworks sind oft nahtlos in Test-Frameworks wie JUnit für Java oder pytest für Python integriert. Dies erleichtert die Verwendung von Testdoubles in Unit-Tests und Integrationstests.

Einfache Handhabung von Testdoubles: Diese Frameworks bieten einfache APIs zur Handhabung von Testdoubles. Entwickler können sie leicht erstellen, konfigurieren und in ihre Tests integrieren.

Überwachung und Verifikation: Test Double Frameworks ermöglichen die Überwachung und Verifikation des Verhaltens von Testdoubles. Entwickler können überprüfen, ob bestimmte Methodenaufrufe erfolgt sind und ob sie den erwarteten Ergebnissen entsprechen.

Testisolation: Die Verwendung von Test Double Frameworks ermöglicht die Isolation von Tests. Dies bedeutet, dass Tests unabhängig voneinander und von externen Ressourcen wie Datenbanken oder Webservices durchgeführt werden können.

Beliebte Frameworks: Es gibt eine Vielzahl von Test Double Frameworks für verschiedene Programmiersprachen. Einige der beliebtesten Frameworks sind Mockito für Java, Sinon für JavaScript, PHPUnit für PHP und Pytest-mock für Python.

Die Verwendung von Test Double Frameworks erleichtert die Erstellung und Verwaltung von Testdoubles und trägt dazu bei, effektive und zuverlässige Tests in agilen und Test-getriebenen Entwicklungsumgebungen durchzuführen. Diese Frameworks sind ein wichtiger Bestandteil der Werkzeuge und Praktiken, die in der agilen Softwareentwicklung eingesetzt werden, um die Qualität von Softwareprodukten sicherzustellen.
[22]

# Pair programming
Pair Programming oder Programmieren in Paaren ist eine zentrale Technik aus dem Extreme Programming (XP). Beim Pair Programming sitzen zwei Entwickler gleichberechtigt an einem Rechner und arbeiten gemeinsam an einer Aufgabe. Die zwei Entwickler:innen nehmen unterschiedliche Rollen ein, welche oft mit „Pilot“ und „Navigator“ bezeichnet werden.

Der „Pilot“ schreibt den Code, während der „Navigator“ die Korrektheit des Codes und des Lösungsansatzes überwacht und parallel über Verbesserungen am Design nachdenkt. Weil beide Entwickler:innen gleichberechtigt sind, gibt es keine feste Aufgabenteilung. Deshalb wechselt der „Pilot“ alle paar Minuten zum „Navigator“ und der „Navigator“ wird zum „Piloten“. Auch zwischen den Paaren werden die Partner:innen kontinuierlich gewechselt. So wird sichergestellt, dass jedes Teammitglied alle Teile des Projektes kennenlernt. ist das die Definition von Pair programming

[33]

## Ablauf
Der Ablauf beim Pair Programming ist in der Regel recht einfach:

Es gibt zwei Schlüsselrollen: den Driver oder Piloten und den Navigator oder Beobachter. Der Driver ist derjenige, der aktiv am Computer arbeitet und den Code schreibt. Währenddessen erklärt der Driver, was er tut, so dass der Navigator seine Gedanken und Absichten verstehen kann. Der Navigator hingegen beobachtet aufmerksam die Codierung und bietet Feedback zur Implementierung. Gleichzeitig denkt der Navigator darüber nach, wie die Aufgabe möglicherweise optimiert werden kann. Die Idee hinter dieser Rollenteilung besteht darin, zwei verschiedene Perspektiven auf den Code zu haben: Der Driver konzentriert sich auf die unmittelbaren Details und Codezeilen, während der Navigator eine übergeordnete, strategische Sichtweise einnimmt und das Gesamtbild im Auge behält.

Die Rollen zwischen den beiden Entwicklern wechseln regelmäßig ab, wobei jeder abwechselnd die Rolle des Drivers und des Navigators übernimmt.

Die Paarprogrammierer arbeiten idealerweise eng zusammen und fördern eine ständige Kommunikation. Sie klären Unklarheiten oder Fragen bezüglich des Vorgehens, der Programmierung und der Tests so schnell wie möglich.

Es ist nicht ungewöhnlich, dass einer der beiden Entwickler nach einer bestimmten Zeit (z. B. alle paar Tage oder eine Woche) das Paar verlässt und einem anderen Kollegen Platz macht. Dies wird als Paar-Rotation oder Pair Rotation bezeichnet. In einigen Publikationen wird die Person, die im Team bleibt, als "Anker" bezeichnet. Die Absicht dahinter, sofern sie nicht auf Urlaub oder Krankheit zurückzuführen ist, besteht darin, frische Perspektiven und neue Energie ins Team zu bringen und die Bildung von Wissenssilos zu vermeiden. Natürlich sollte jede Organisation individuell entscheiden, ob und wann ein Wechsel sinnvoll ist.

In der Praxis kann die Art und Weise, wie die Entwickler zusammenarbeiten, variieren. Manche teilen sich einen Computer, während andere jeweils ihren eigenen Computer verwenden und auf einem gemeinsamen Code-Stand arbeiten. Die Verwendung von gängigen Versionsverwaltungstools ermöglicht es, selbst mit getrennten Rechnern problemlos zusammenzuarbeiten.
[34]

## Best practices
Best Practices für Pair Programming:

1. Gemeinsam planen: Bevor Sie mit dem Programmieren beginnen, klären Sie Ihre Ziele und Aufgaben, die Dauer der Sitzung und Rollenwechsel. Nehmen Sie sich Zeit, sich über persönliche Vorlieben auszutauschen.

1. Regelmäßiger Rollenwechsel: Wechseln Sie regelmäßig zwischen den Rollen des Piloten und des Navigators, idealerweise alle 30 Minuten. Dies ermöglicht verschiedene Perspektiven und fördert die Zusammenarbeit.

1. Gutes Audio- und Video-Setup: Achten Sie auf eine klare Audio- und Videokommunikation, insbesondere bei Remote-Pair Programming. Verwenden Sie Headsets und schalten Sie die Videokamera ein, um die Kommunikation zu verbessern.

1. Vermeiden Sie Mikromanagement: Vermeiden Sie es, den Partner zu kontrollieren oder zu diktieren. Schaffen Sie eine sichere Umgebung für die Zusammenarbeit und fördern Sie den Wissensaustausch.

1. Seien Sie nett und geduldig: Seien Sie geduldig und respektvoll, insbesondere bei unterschiedlichen Qualifikationsniveaus. Vermeiden Sie es, den Partner zu überwachen oder zu unterbrechen.

1. Vermeiden Sie äußere Ablenkungen: Ignorieren Sie E-Mails und andere Ablenkungen während der Pair-Programming-Sitzung. Planen Sie Pausen und Aktivitäten außerhalb des Programmierens.

1. Ständige Kommunikation: Halten Sie die Kommunikation während der Sitzung aufrecht, um sicherzustellen, dass beide Partner aktiv teilnehmen und zusammenarbeiten.
[35]


# Code reviews
Eine Codeüberprüfung ist eine Peer-Review von Code, die Entwicklern dabei hilft, die Codequalität sicherzustellen oder zu verbessern, bevor sie ihn zusammenführen und versenden.
[36] 
## Conventional comments

Definition:
Conventional comments sind ein standardisiertes System zur Bereitstellung von Feedback während Code-Reviews und technischer Diskussionen. Sie verwenden vordefinierte Labels zur Kategorisierung von Kommentaren, verbessern die Kommunikation und machen Reviews effizienter.



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


Dekorationen:

non-blocking: Ein Kommentar, der die Code-Akzeptanz nicht blockieren sollte.
blocking: Ein Kommentar, der behoben werden muss, bevor die Akzeptanz erfolgt.
if-minor: Der Autor kann den Kommentar bei geringfügigen Änderungen beheben.

Vorteile:

Verbesserte Klarheit: Standardisierte Labels und Formate machen Kommentare klarer und expliziter.
Strukturiertes Feedback: Kommentare sind organisiert und helfen Entwicklern, schneller zu verstehen und zu reagieren.
Offener Dialog: Labels helfen dabei, die Natur und Absicht des Feedbacks festzulegen und fördern konstruktive Gespräche.
Konventionelle Kommentare verbessern die Effektivität von Code-Reviews, indem sie einen strukturierten und klaren Rahmen für Feedback bieten.
[37]

## Ablauf
. Einreichung des Codes: Der Entwickler, der den Code geschrieben hat, reicht ihn zur Überprüfung ein. Dies kann durch das Erstellen eines Pull Requests in einem Versionskontrollsystem wie Git erfolgen.

2. Auswahl der Überprüfer: In der Regel wählt der Autor des Codes ein oder mehrere Teammitglieder aus, die den Code überprüfen sollen. Dies können erfahrene Entwickler oder Experten auf dem jeweiligen Gebiet sein.

3. Review des Codes: Die ausgewählten Überprüfer gehen den Code Zeile für Zeile durch. Sie suchen nach Fehlern, wie Bugs oder Sicherheitslücken, überprüfen die Codequalität, achten auf Best Practices und stellen sicher, dass der Code den Projektstandards entspricht.

4. Kommentare und Diskussion: Während des Reviews hinterlassen die Überprüfer Kommentare im Code, um auf bestimmte Probleme oder Verbesserungen hinzuweisen. Der Autor des Codes kann auf diese Kommentare antworten, um Klarstellungen zu liefern oder Diskussionen anzustoßen.

5. Überarbeitung: Basierend auf den erhaltenen Kommentaren und Rückmeldungen des Überprüfungsteams überarbeitet der Code-Autor seine Implementierung. Er behebt Fehler, implementiert die vorgeschlagenen Verbesserungen und aktualisiert den Code entsprechend.

6. Weitere Reviews: Der Code-Autor kann den überarbeiteten Code erneut einreichen, um weitere Überprüfungen zu erhalten. Dieser Prozess kann sich mehrmals wiederholen, bis der Code als akzeptabel angesehen wird.

7. Akzeptanz und Zusammenführung: Sobald der Code die Zustimmung der Überprüfer erhält und als fehlerfrei und den Standards entsprechend gilt, kann er in das Hauptprojekt oder den Hauptzweig (Main) zusammengeführt werden.

8. Dokumentation: Nach dem erfolgreichen Zusammenführen des Codes sollte der Autor sicherstellen, dass die Änderungen ordnungsgemäß dokumentiert werden. Dies kann im Changelog oder in der Projektdokumentation erfolgen.

Ein effektives Code-Review fördert den Wissensaustausch, verbessert die Qualität des Codes und erhöht die Zuverlässigkeit der Software. Es ist ein wichtiger Schritt, um sicherzustellen, dass Softwareprojekte erfolgreich abgeschlossen werden und gut warten werden können.
[22]

## Best practices
1. Etablieren Sie einen klaren Prozess:
Definieren Sie klare Regeln und Schritte für den Überprüfungsprozess. Dies schließt ein, wie und wann Pull Requests erstellt werden und wer für die Bewertung zuständig ist.

2. Konzentrieren Sie sich auf das Wesentliche:
Legen Sie den Fokus bei Code-Reviews auf die folgenden Aspekte:

Funktionalität: Verhält sich der Code wie erwartet?
Softwaredesign: Ist der Code gut strukturiert und passt er zur Gesamtarchitektur?
Komplexität: Ist der Code leicht verständlich?
Tests: Enthält die PR gut durchdachte Tests?
Benennung: Sind Variablen und Funktionen sinnvoll benannt?
Kommentare: Sind die Kommentare klar und nützlich?
Dokumentation: Wurde die relevante Dokumentation aktualisiert?
3. Frühzeitige Diskussion auf höchster Ebene:
Besprechen Sie komplexe Aufgaben vor der Implementierung. Dies minimiert Änderungen im Nachhinein und erhöht die Effizienz.

4. Teamoptimierung:
Optimieren Sie für die Teamleistung, nicht nur für die individuelle Produktivität. Stellen Sie sicher, dass alle Teammitglieder aktiv am Überprüfungsprozess beteiligt sind und festlegen, wie schnell auf PRs reagiert wird.

5. Entscheiden Sie sich für Taten:
Setzen Sie technische Entscheidungen in angemessener Zeit um und vermeiden Sie zu lange Entscheidungsprozesse.

6. Halten Sie Pull Requests klein:
Kleinere PRs sind einfacher zu verwalten und beschleunigen den gesamten Prozess. Es gibt keine festen Regeln für die Größe, aber etwa 100 Zeilen pro PR sind eine angemessene Richtlinie.

7. Fördern Sie eine positive Feedback-Kultur:

Geben Sie Feedback zum Code, nicht zum Autor.
Wählen Sie Ihre Schlachten aus.
Akzeptieren Sie verschiedene Lösungsansätze.
Behandeln Sie alle Teammitglieder mit Respekt.
Denken Sie daran, dass PR-Autoren auch Menschen sind und achten Sie auf den Umgangston.
8. Nutzen Sie die kontinuierliche Integration effektiv:
Automatisieren Sie so viele Qualitätsprüfungen wie möglich, um die manuelle Überprüfung auf wichtigere Aspekte zu konzentrieren.

9. Delegieren Sie Kleinigkeiten an den Computer:
Automatisieren Sie Prüfungen für stilistische Details und Kleinigkeiten. Vermeiden Sie lange Diskussionen über stilistische Entscheidungen.

10. Kommunizieren Sie explizit:
Geben Sie klare Anweisungen an den Autor, was genau geändert werden sollte. Nutzen Sie die Funktionen des Tools zur expliziten Kommunikation.

11. Verwenden Sie explizite Überprüfungsanfragen:
Automatisieren Sie Überprüfungsanfragen, um sicherzustellen, dass keine PRs übersehen werden.

12. Überprüfen Sie Ihren eigenen Code:
Bevor Sie eine PR einreichen, gehen Sie den Code selbst durch, um einfache Fehler zu identifizieren.

13. Dokumentieren Sie im Code:
Dokumentieren Sie Codeänderungen und Diskussionen direkt im Code, um die Lesbarkeit und das Verständnis zu verbessern.

14. Schreiben Sie klare PR-Beschreibungen:
Erstellen Sie detaillierte PR-Beschreibungen, um dem Prüfer ein klares Bild der Änderungen zu vermitteln.

15. Nutzen Sie das Shared-Repository-Modell:
In privaten Repositorys ist das Shared-Repository-Modell empfohlen. Dadurch werden Abläufe vereinfacht und Code-Zweige effizienter verwaltet.

16. Halten Sie Diskussionen öffentlich:
Führen Sie Diskussionen innerhalb der PR-Diskussion, damit sie für alle zugänglich und durchsuchbar sind.

Mit diesen bewährten Methoden können Code-Reviews effektiver gestaltet werden, was zu höherer Codequalität und besserer Teamarbeit führt.
[38]

# Refactoring
Refactoring ist eine disziplinierte Technik zur Umstrukturierung eines vorhandenen Codekörpers, bei der seine interne Struktur geändert wird, ohne sein äußeres Verhalten zu ändern.

Sein Herzstück ist eine Reihe kleiner verhaltenserhaltender Transformationen. Jede Transformation (als „Refactoring“ bezeichnet) bewirkt wenig, aber eine Abfolge dieser Transformationen kann zu einer erheblichen Umstrukturierung führen. Da jedes Refactoring klein ist, ist es weniger wahrscheinlich, dass es schiefgeht. Das System bleibt nach jedem Refactoring voll funktionsfähig, wodurch die Wahrscheinlichkeit verringert wird, dass ein System während der Umstrukturierung ernsthaft beschädigt wird.

[39] 


## Ziele des Refactorings
Refactoring verbessert die Lesbarkeit des Codes und macht ihn einfacher zu verstehen und zu warten. Es hilft, die Codequalität zu verbessern, indem es die Komplexität reduziert, die Wartbarkeit erhöht und die Leistung verbessert. Es hilft auch, die Codebasis zu vereinfachen und die technische Schulden zu reduzieren. Refactoring ist ein wichtiger Bestandteil der agilen Softwareentwicklung und wird häufig in Kombination mit Test-Driven Development (TDD) eingesetzt.

[22]
## Refactoring-Patterns

Extract Method: Dieses Muster ist nützlich, um lange und komplexe Methoden in kleinere, leichter verständliche Teile aufzuteilen.
Problem
Sie haben ein Codefragment, das gruppiert werden kann.
```javascript
void printOwing() {
  printBanner();

  // Print details.
  System.out.println("name: " + name);
  System.out.println("amount: " + getOutstanding());
}
```
Lösung
Verschieben Sie diesen Code in eine separate neue Methode (oder Funktion) und ersetzen Sie den alten Code durch einen Aufruf der Methode.

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
[40]


Extract Variable: Dieses Muster wird verwendet, um komplexe Ausdrücke in benannte Variablen zu extrahieren, um den Code verständlicher zu machen.

Problem
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
Lösung
Platzieren Sie das Ergebnis des Ausdrucks oder seiner Teile in separaten Variablen, die selbsterklärend sind.
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
[41]
Inline Method: Umgekehrt zu "Extract Method", das Entfernen kleiner Hilfsmethoden kann den Code vereinfachen.

Problem
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
Lösung
Ersetzen Sie Aufrufe der Methode durch den Inhalt der Methode und löschen Sie die Methode selbst.

```javascript
class PizzaDelivery {
  // ...
  int getRating() {
    return numberOfLateDeliveries > 5 ? 2 : 1;
  }
}
```
[42]
es gibt noch viele weiter Patterns und Methoden wie:
Rename Variable: Die Umbenennung von Variablen in klar verständliche Namen ist entscheidend, um die Lesbarkeit des Codes zu verbessern.

Move Method: Das Verschieben von Methoden in die richtige Klasse kann dazu beitragen, die Struktur des Codes zu verbessern und Abhängigkeiten zu verwalten.

Replace Conditional with Polymorphism: Wenn Sie viele bedingte Anweisungen haben, kann die Umstellung auf polymorphe Strukturen die Wartbarkeit und Lesbarkeit des Codes erheblich verbessern.

Encapsulate Field: Das Einhüllen von Feldern in Methoden, um den Zugriff auf Felder zu steuern und die Flexibilität zu erhöhen.

Introduce Parameter Object: Wenn eine Methode viele Parameter hat, kann das Gruppieren dieser Parameter in einem Objekt die Signatur der Methode vereinfachen.

Encapsulate Collection: Das Einhüllen von Sammlungen in eigene Klassen zur besseren Steuerung und Abstraktion der Daten.

Remove Duplicate Code: Die Entfernung von Duplikaten im Code, um die Wartbarkeit zu erhöhen und Fehler zu reduzieren.

Das sind die in meist genutzten Refactoring Patterns, es gibt noch viele weitere.
[22]

# Werkzeuge
## Testing / Build
Test Tools:
Testautomatisierungs-Frameworks sind eine Reihe von Regeln und Tools, die zur Erstellung von effizienten Testfällen verwendet werden. Diese Frameworks bieten eine Vielzahl von Vorteilen, darunter die Wiederverwendbarkeit von Code, kostengünstige Entwicklung von Testfällen und eine minimale manuelle Interaktion. Sie verbessern die Effizienz, da sie Testabläufe standardisieren und die Testabdeckung maximieren.

Es gibt verschiedene Arten von automatisierten Test-Frameworks:

Datengesteuertes Test-Framework: Ermöglicht das Speichern von Testdaten auf einem externen Laufwerk, um neue Skripte zu Testfällen hinzuzufügen.

Schlüsselwortgesteuertes Test-Framework: Extrahiert Testdaten aus externen Quellen und verwendet Schlüsselwörter, um Testskripte anzupassen und verschiedene Ergebnisse zu erzielen.

Hybrid-Test-Framework: Kombiniert datengesteuerte und schlüsselwortgesteuerte Frameworks, um höhere Produktivität zu erreichen.

Lineares Scripting-Framework: Erfordert manuelle Aufzeichnung von Prozessschritten und ist weniger automatisiert. Bekannt als "Record and Playback Framework."

Modulbasiertes Test-Framework: Erfordert separate Skripte für verschiedene Module und bietet hohe Modularisierung, aber erfordert möglicherweise individuelle Änderungen an den Testdaten.

Diese Frameworks bieten die Flexibilität, je nach den Anforderungen und Komplexitätsgraden Ihrer Testfälle ausgewählt zu werden. Sie können die Effizienz, Wiederverwendbarkeit und Kostenreduzierung in Ihren automatisierten Testprozessen maximieren.
[43]

Build Tools:

Build Tools sind Softwarewerkzeuge, die in der Softwareentwicklung eingesetzt werden, um den Prozess der Kompilierung, des Testens und des Bereitstellens von Software zu automatisieren. Sie spielen eine entscheidende Rolle bei der Umwandlung von Quellcode in ausführbare Anwendungen oder Bibliotheken.
1. Jenkins

Ein weit verbreitetes Open-Source-Automatisierungstool für CI/CD.
Einfache Einrichtung auf verschiedenen Plattformen.
Unterstützt Plugin-basierte Integration mit Drittanbieter-Tools.
Ermöglicht verteilte Builds.
Bietet nativ Integration mit Versionskontrollsystemen wie Git.
2. Gradle

Ein Open-Source-Build-Automatisierungstool mit Schwerpunkt auf Anpassbarkeit und Geschwindigkeit.
Verwendet eine Groovy-basierte DSL für Build-Skripts.
Unterstützt inkrementelle Builds und ist flexibel für verschiedene Projekte und Sprachen.
Besonders geeignet für die Android-Entwicklung.
3. Maven

Ein populäres Build-Automatisierungstool, spezialisiert auf die Java-Entwicklung.
Verwendet XML-basierte POM-Dateien zur Steuerung des Builds.
Betont Konvention über Konfiguration und zentralisierte Abhängigkeitsverwaltung.
Unterstützt verschiedene Phasen des Projektzyklus.
4. Travis CI

Eine Cloud-Lösung zur Automatisierung des Builds und Tests von GitHub-Repositories.
Einfache Einrichtung und Integration mit GitHub.
Bietet parallele Builds für schnellere Tests und kürzere Build-Zeiten.
5. CircleCI

Ein Continuous Integration- und Continuous Delivery-Tool in der Cloud.
Fokussiert auf Tests von Code-Änderungen mit Unit-Tests, Integrationstests und Funktionstests.
Arbeitet gut mit Docker-Containern und bietet Caching für schnellere Builds.
Die Wahl des richtigen Build-Tools hängt von den Projektanforderungen, der Plattformunterstützung und der Integration in CI/CD-Pipelines ab. Es gibt keine Einheitslösung, da jedes Tool seine eigenen Stärken und Schwächen hat. Die Entscheidung sollte sorgfältig auf Grundlage der spezifischen Projektanforderungen getroffen werden.
[44]
### Github actions
GitHub Actions ist ein leistungsstarkes Tool für die Automatisierung von Build- und Testprozessen in GitHub-Repositorys. Es ermöglicht Entwicklern, Workflow-Automatisierungen zu erstellen und auszuführen, die auf Ereignissen in ihren Repositorys basieren. Hier sind einige Informationen zu GitHub Actions im Kontext von Testing und Build Tools:

Automatisierte Tests: Mit GitHub Actions können Entwickler automatisierte Tests als Teil ihres Workflow erstellen. Dies bedeutet, dass bei jedem Commit oder Pull Request automatisch Tests ausgeführt werden können, um sicherzustellen, dass der Code fehlerfrei ist. Dies ist besonders nützlich in Continuous Integration (CI) und Continuous Deployment (CD) Pipelines.

Build-Prozesse: Entwickler können ihre Build-Prozesse ebenfalls automatisieren. Dies bedeutet, dass Sie den Code automatisch kompilieren, Bibliotheken herunterladen und Artefakte erstellen können, die für den Bereitstellungsprozess erforderlich sind. Dies kann dazu beitragen, den Build-Prozess zu beschleunigen und menschliche Fehler zu minimieren.

Vielseitigkeit: GitHub Actions unterstützt eine Vielzahl von Programmiersprachen, Build-Tools und Test-Frameworks. Sie können den Workflow an die Anforderungen Ihres Projekts anpassen.

Benutzerdefinierte Workflows: Entwickler können benutzerdefinierte Workflow-Dateien erstellen, um genau festzulegen, welche Schritte ausgeführt werden sollen. Dies bedeutet, dass Sie spezifische Build- und Testaufgaben basierend auf den Anforderungen Ihres Projekts konfigurieren können.

Integrationen: GitHub Actions kann in Kombination mit anderen Tools und Diensten verwendet werden, um erweiterte CI/CD-Pipelines zu erstellen. Zum Beispiel können Sie Docker-Container verwenden, um Umgebungen für Ihre Tests zu erstellen, und Cloud-Dienste für das Deployment nutzen.

Status-Checks: Nach Abschluss eines GitHub-Actions-Workflows können Sie Status-Checks und Berichte in Ihrem Pull Request sehen, um schnell festzustellen, ob Tests erfolgreich durchgeführt wurden und der Code bereit für die Zusammenführung ist.

Skalierbarkeit: GitHub Actions kann sowohl für kleine als auch für große Projekte verwendet werden und bietet die Flexibilität, sich an die Bedürfnisse des Projekts anzupassen.

Insgesamt bietet GitHub Actions eine nahtlose Möglichkeit, CI/CD in Ihren GitHub-Workflow zu integrieren, um sicherzustellen, dass Ihr Code getestet und effizient bereitgestellt wird. Es ist eine wertvolle Ressource für Entwickler, um die Qualität ihres Codes sicherzustellen und Entwicklungsprozesse zu automatisieren.
[22]

## Bug and work tracking
Bug and work Tracking Tools:
Diese Tools sind besonders nützlich für Softwareentwickler, Projektmanager und Teams, um Fehler und Aufgaben effizient zu verfolgen und zu verwalten. Hier sind einige der beliebtesten Optionen:

Jira: Jira ist eines der bekanntesten Bug- und Arbeitsverfolgungstools, das von Atlassian entwickelt wurde. Es bietet eine Vielzahl von Funktionen zur Verfolgung von Aufgaben, Bugs und Projekten. Jira kann stark angepasst werden und wird von vielen Softwareentwicklungsteams weltweit verwendet.

Trello: Trello ist ein visuelles Projektmanagement-Tool, das Boards, Listen und Karten verwendet, um Aufgaben und Fehler zu organisieren. Es ist einfach zu bedienen und eignet sich besonders gut für kleinere Teams und weniger komplexe Projekte.

Asana: Asana ist ein umfassendes Projektmanagement-Tool, das sich gut für die Verfolgung von Aufgaben und Bugs eignet. Es ermöglicht die Zusammenarbeit in Teams und bietet Funktionen wie Zeitleisten und Abhängigkeiten.

GitHub Issues: Wenn du an Open-Source-Projekten arbeitest oder Entwicklungsprojekte auf GitHub hostest, ist GitHub Issues eine großartige Option. Es ermöglicht die Verfolgung von Problemen direkt in deinem GitHub-Repository.

Bugzilla: Bugzilla ist eine Open-Source-Plattform für das Bug-Tracking und bietet eine Vielzahl von Funktionen für die Verfolgung von Bugs und Aufgaben. Es wird von vielen großen Organisationen eingesetzt.

Redmine: Redmine ist eine Open-Source-Projektmanagement- und Bug-Tracking-Plattform. Es bietet flexible Anpassungsmöglichkeiten und ist in der Entwicklergemeinschaft weit verbreitet.

Zendesk: Zendesk ist eine Kunden-Support- und Ticketverwaltungsplattform, die auch für das Bug-Tracking verwendet werden kann. Es ist ideal, wenn du Kundenbetreuung und Fehlerverfolgung in einem Tool kombinieren möchtest.

Mantis Bug Tracker: Mantis ist ein Open-Source-Tool für das Bug-Tracking, das sich durch seine Benutzerfreundlichkeit auszeichnet. Es eignet sich gut für kleinere Entwicklungsteams.

Die Auswahl eines Bug- und Arbeitsverfolgungstools hängt von den spezifischen Anforderungen eines Teams und Projekts ab. Berücksichtige Faktoren wie Teamgröße, Projektumfang, Budget und Integrationsmöglichkeiten, wenn du das richtige Tool für deine Bedürfnisse auswählst.
[22]

---
#Wiederholungsbzw- Verständnisfragen:
1. Was ist ein verteiltes Softwaresystem?
2. Was ist der Unterschied zwischen einem Client-Server-Modell und einem Peer-to-Peer-Modell?
3. Was ist der Unterschied zwischen einem ESB und einer Message Queue?
4. Welche Skalierungsmuster kennst du?
5. Was ist der Unterschied zwischen horizontaler und vertikaler Skalierung?
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

