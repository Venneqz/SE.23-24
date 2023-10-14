# Kapitel 2

**Autor:** Marvin Petschulat, Mattis Wellenbüscher

---
# Verteilte Softwaresysteme

  ### Definiton

    Ein verteiltes System ist ein Programmsystem,
    das aus Teilsystemen besteht,
    die auf mehreren lose gekoppelten Prozessoren implementiert
    und über eine Netzwerk verbunden sind.

    Lose gekoppelt heißt in diesem Zusammenhang, dass Prozessoren standortbezogen von einander getrennt sind.

    In verteilten Systemen können verschiedene Leute und Programme gemeinsam auf Dinge wie Drucker, Dateien und Speicher zugreifen. Das hilft, die Dinge effizienter zu nutzen und spart Ressourcen.
    [1]

  ## Eigenschaften, Vorteile, Nachteile:
  ### Eigenschaften:

    Nutzung gemeinsamer Ressourcen – Ein verteiltes System kann Hardware, Software oder Daten gemeinsam nutzen.

    Simultane Verarbeitung – Mehrere Rechner können dieselbe Funktion simultan verarbeiten.

    Skalierbarkeit – Die Rechen- und Verarbeitungskapazität kann bei Bedarf skaliert werden, wenn sie auf weitere Rechner ausgeweitet wird.

    Fehlererkennung – Fehler werden einfacher erkannt.

    Transparenz – Ein Knoten kann auf andere Knoten im System zugreifen und mit diesen kommunizieren.
    [2]
    

  ### Vorteile:
    Ressourcennutzung: Effiziente gemeinsame Nutzung von Ressourcen wie Druckern und Speichergeräten.

    Offenheit: Integration proprietärer Technologien und Ressourcen verschiedener Hersteller für Interoperabilität.

    Parallelität: Gleichzeitige Ausführung von Prozessen auf verschiedenen Ressourcen zur Leistungssteigerung.

    Skalierbarkeit: Leicht erweiterbar, um sich an wachsende Anforderungen anzupassen.

    Fehlertoleranz: Toleranz gegenüber Hardware- oder Software-Ausfällen durch Umschalten auf alternative Ressourcen.

    Transparenz: Benutzerfreundliche Nutzung ohne detaillierte Kenntnisse der Verteilung.

    Kosteneffizienz: In kleineren verteilten Systemen wie PCs und LANs niedrigere Gesamtkosten durch effiziente Ressourcennutzung.
    [3] [4]


  ### Nachteile:
    Komplexität: Verteilte Systeme erfordern höheren Entwicklungsaufwand und sind schwerer zu warten. Benutzer können die Systeme schwerer verstehen.

    Sicherheit: Die Sicherheit in verteilten Systemen ist schwerer zu kontrollieren, und Datensicherheit ist gefährdet.

    Manageability: Die Koordination von Komponenten verschiedener Hersteller und Versionen erfordert einen hohen Wartungsaufwand.

    Unpredictability: Das Verhalten von verteilten Systemen, insbesondere in Bezug auf Lastverteilung, ist schwer vorhersehbar.

    Kommunikationsaufwand: In verteilten Systemen erfordert die Kommunikation zwischen Komponenten über das Netzwerk erhöhten Aufwand.

    Konsistenzprobleme: Die Aufrechterhaltung der Konsistenz von Daten über verschiedene Knoten hinweg kann problematisch sein und zu Konflikten führen.

    Skalierbarkeitsprobleme: Das Hinzufügen von Komponenten und Knoten kann Skalierbarkeitsprobleme verursachen, wenn die Skalierbarkeit nicht ordnungsgemäß geplant ist.

    Trotz dieser Nachteile sind verteile Systeme in vielen Fällen unverzichtbar, da sie Flexibilität, Ressourcennutzung und Skalierbarkeit bieten. Die Nachteile können mit sorgfältiger Planung, Architektur und Sicherheitsmaßnahmen minimiert werden.
    [3] [4]
  
  ## Motivation (Warum man Verteilung braucht):

  ### Mangelnde Möglichkeiten der Zentralrechner:


    Antwortzeiten: Verteilte Systeme ermöglichen es, die Last auf mehrere Computer zu verteilen, was die Antwortzeiten verbessert, da Aufgaben parallel verarbeitet werden können.

    Interaktivität: Durch die Verteilung von Anwendungen auf mehrere Knoten in einem verteilten System können interaktive Anwendungen effizienter ausgeführt werden, da die Verarbeitung über verschiedene Ressourcen verteilt ist.

    Benutzerschnittstellen und Grafik: Verteilte Systeme können komplexe Benutzerschnittstellen und Grafiken unterstützen, da sie auf leistungsstarken Workstations und Servern ausgeführt werden können.
    [5]

  ### Anforderungen neuer Anwendungen:

    Grafische Benutzerschnittstellen: Moderne Anwendungen profitieren von grafischen Benutzerschnittstellen, und verteilte Systeme bieten die Leistung und Ressourcen, um diese effizient bereitzustellen.

    Kurze Antwortzeiten: Verteilte Systeme sind in der Lage, Lastspitzen zu bewältigen und können auf verschiedene Ressourcen zugreifen, um kurze Antwortzeiten für Benutzer zu gewährleisten.
    [5]

  ### Weite Verbreitung mächtiger PCs und Workstations:

    Die Verwendung leistungsstarker PCs und Workstations als Teil verteilter Systeme ermöglicht die effiziente Ausführung anspruchsvoller Anwendungen und die Bereitstellung von Rechenleistung und Speicherressourcen.
    Fortgeschrittene Netztechnologien (LAN, WAN, MAN, wireless):

    Fortgeschrittene Netzwerkinfrastrukturen erlauben die Kommunikation und Koordination zwischen den Komponenten verteilter Systeme, unabhängig von der geografischen Entfernung. Dies trägt zur Skalierbarkeit und Flexibilität des Systems bei.
    [5]
  ### Gemeinsame Nutzung von Ressourcen (bzw. Diensten):

    Verteilte Systeme ermöglichen die gemeinsame Nutzung von Ressourcen und Diensten über verschiedene Plattformen hinweg, was zu effizienterer Ressourcennutzung und Kostenersparnis führt.
    Geringere Hardware-Kosten (!?!) - Grosch's Gesetz / Amdahl's Law:

    Verteilte Systeme können dazu beitragen, die Gesamtkosten zu senken, indem sie die vorhandene Hardware effizienter nutzen und Skaleneffekte erzielen. Dies entspricht Grosch's Gesetz (größere Systeme sind kosteneffizienter) und Amdahl's Law (Verbesserungen in einem Teil des Systems führen zu Verbesserungen im Gesamtsystem).
    [5]

  ## Distributed (Verteilt) vs decentralized:
  ### Vergleich: Dezentral vs. Verteilt:

    1. Kontrolle:

    Dezentrale Systeme:

    Keine zentrale Kontrolle; Entscheidungen von einzelnen Teilnehmern.
    Betont Autonomie und Unabhängigkeit.
    Beispiel: Bitcoin - keine zentrale Bank.
    Verteilte Systeme:

    Koordination kann zentral oder begrenzt sein.
    Verteilung von Ressourcen über Knoten.
    Beispiel: CDNs - Datenverteilung mit zentraler Steuerung.
    2. Widerstandsfähigkeit:

    Dezentrale Systeme:

    Hohe Widerstandsfähigkeit gegenüber Ausfällen oder Angriffen.
    Beispiel: Blockchain-Netzwerke.
    Verteilte Systeme:

    Widerstandsfähigkeit hängt von der Architektur ab.
    Beispiel: Cloud-Plattformen - Robustheit durch Verteilung.
    3. Skalierbarkeit:

    Dezentrale Systeme:

    Skalierbarkeit kann eine Herausforderung sein.
    Beispiel: Bitcoin-Skalierbarkeitsprobleme.
    Verteilte Systeme:

    Bessere Skalierbarkeit durch Ressourcenverteilung.
    Beispiel: Cloud-Computing.
    4. Datenkonsistenz:

    Dezentrale Systeme:

    Konsistenz kann herausfordernd sein, erfordert Konsensmechanismen.
    Beispiel: Blockchain-Netzwerke.
    Verteilte Systeme:

    Einfachere Konsistenz dank zentraler Koordination.
    Beispiel: Zentrale Unternehmensdatenbanken.
    [4]
    
  ### Concurrent(Gleichzeitig) vs parallel(Concurrency):

    "Concurrent" in verteilten Systemen bezieht sich auf die gleichzeitige Ausführung von Aufgaben oder Prozessen, bei denen die Reihenfolge, in der sie ausgeführt werden, nicht explizit festgelegt ist.
    In einem verteilten System können mehrere Aufgaben oder Prozesse parallel ablaufen, aber sie müssen nicht zwingend gleichzeitig gestartet werden oder die gleiche Reihenfolge haben.
    Concurrent Computing ermöglicht die effiziente Nutzung von Ressourcen und die gleichzeitige Verarbeitung von Anfragen, ohne dass eine bestimmte Abhängigkeit zwischen den Prozessen erforderlich ist.
    Parallel (Parallelität):

    "Parallel" in verteilten Systemen bezieht sich auf die tatsächliche gleichzeitige Ausführung von Aufgaben oder Prozessen auf verschiedenen Knoten oder Systemen, wobei eine explizite Koordination erforderlich ist.
    In einem parallelen verteilten System arbeiten separate Knoten oder Systeme zusammen, um eine Aufgabe aufzuteilen und Teilaufgaben parallel auszuführen.
    Parallel Computing erfordert eine koordinierte Zusammenarbeit zwischen den Knoten, um sicherzustellen, dass die Teilaufgaben synchronisiert werden und ein kohärentes Ergebnis erzeugen.
    Beispiel:

    Angenommen, Sie haben ein verteiltes System zur Verarbeitung von Echtzeittransaktionen in einem E-Commerce-Unternehmen:

    Concurrent: Mehrere Kunden geben gleichzeitig Bestellungen auf der Website auf. Die Server im verteilten System verarbeiten diese Bestellungen ohne eine festgelegte Reihenfolge, da sie unabhängig voneinander sind.

    Parallel:
    Wenn es Spitzenzeiten gibt, könnten separate Server in verschiedenen Rechenzentren parallel arbeiten, um die Bestellungen zu verarbeiten. Diese Server müssen jedoch in Echtzeit synchronisiert werden, um sicherzustellen, dass die Bestellungen korrekt und konsistent verarbeitet werden.

    In verteilten Systemen ist die Unterscheidung zwischen Concurrent und Parallel wichtig, da sie Auswirkungen auf die Skalierbarkeit, Leistung und Synchronisation haben kann. Concurrent Computing ermöglicht Flexibilität, während Parallel Computing zusätzliche Koordination erfordert, um sicherzustellen, dass die Ergebnisse korrekt sind.

    [4]
---
# System Design
### Defintion
    Beim Systemdesign werden die Elemente eines Systems wie Architektur, Module und Komponenten, die verschiedenen Schnittstellen dieser Komponenten und die Daten, die das System durchlaufen, definiert. Es soll die spezifischen Bedürfnisse und Anforderungen eines Unternehmens oder einer Organisation durch die Entwicklung eines kohärenten und gut funktionierenden Systems erfüllen.
    [7]

### API Gateway:
      Ein API-Gateway ist ein essenzieller Bestandteil einer Microservices-Architektur. Es dient als zentraler Koordinator für alle Client-Anfragen an die Backend-Dienste. Dies ermöglicht zentralisierte Authentifizierung und Autorisierung, Ratenbegrenzungen, Anpassung von Anfragen und Antworten sowie eine umfassende Überwachung und Protokollierung. Beispiele wie Netflix setzen erfolgreich auf API-Gateways, um komplexe Microservices-Systeme zu verwalten und eine skalierbare, sichere und flexible Lösung für Millionen täglicher API-Aufrufe bereitzustellen. Insgesamt sind API-Gateways unverzichtbare Werkzeuge zur effizienten Verwaltung und Absicherung von APIs in modernen Anwendungen. [6]

  ### Proxy:
      Ein Proxy ist eine Zwischeninstanz oder Vermittler, der als Schnittstelle zwischen einem Client und einem Server fungiert. Er empfängt Anfragen vom Client und leitet sie an den Zielserver weiter. Proxies werden häufig eingesetzt, um den Datenverkehr zu steuern, zu überwachen, zu sichern und zu optimieren. Sie ermöglichen es, den Zugriff auf Ressourcen zu kontrollieren, die Privatsphäre zu schützen und die Performance zu optimieren. Im Systemdesign dienen Proxies dazu, Netzwerksicherheit, Zugriffskontrolle und die Verbesserung der Systemleistung zu ermöglichen. [4]
### Reverse Proxy:
    Ein Reverse-Proxy ist eine entscheidende Komponente in modernen Webarchitekturen, die auf der Anwendungsschicht (Layer 7) des OSI-Modells operiert. Er bietet zahlreiche Vorteile, darunter verbesserte Leistung, Sicherheit und Wartbarkeit für Webanwendungen. Reverse-Proxys können Aufgaben wie SSL-Terminierung und Inhaltskomprimierung übernehmen, wodurch die Serverentlastung und die Anwendungsleistung gesteigert werden. Sie dienen auch als Sicherheitsschutzschild, indem sie den eingehenden Datenverkehr filtern und bösartige Anfragen abwehren. Darüber hinaus vereinfachen sie die Verwaltung und Skalierung von Servern, was die Wartbarkeit der Anwendung verbessert. Plattformen wie GitHub verlassen sich auf Reverse-Proxys, um effiziente und leistungsstarke Webdienste bereitzustellen. Insgesamt sind Reverse-Proxys unverzichtbar, um Webanwendungen sicherer, leistungsfähiger und leichter wartbar zu machen. [6]


### Load Balancer:
    Durch den Load Balancer können Webanwendungen Millionen von Anfragen verarbeitet werden. Durch den Loadbalancer wird eine optimale Ressourcennutzung gewährleistet, die den Durchsatz maximieren und die Antwortzeit minimieren.

    Sie benutzen verschiedene Algorithmen um die best mögliche Verteilung zu gewährleisten. Load Balancer spielen eine entscheidende Rolle bei der Gewährleistung hoher Verfügbarkeit und Fehlertoleranz, indem sie die Arbeitslast gleichmäßig verteilen und den Datenverkehr bei Serverausfällen umleiten. Dadurch läuft Ihre Anwendung auch bei Spitzenlastzeiten oder Serverausfällen reibungslos.
    [6]

### API Gateway vs Proxy vs Reverse Proxy vs Load Balancer

    Aber was ist jetzt der Unterschied zwischen den ganzen?:
    Diese Komponenten weisen einige Gemeinsamkeiten auf, dienen jedoch in modernen Webarchitekturen unterschiedlichen Zwecken.

    Load Balancer priorisieren die Verbesserung der Leistung, Verfügbarkeit und Fehlertoleranz, indem sie Anfragen gleichmäßig auf mehrere Backend-Server verteilen und arbeiten hauptsächlich auf Netzwerkebene. Sie sind die Wahl, wenn die Hauptanforderung die Lastverteilung ist.

    Reverse Proxys operieren auf der Anwendungsebene und bieten Zusatzfunktionen wie URL-Umschreiben, Inhaltskomprimierung und Zugriffskontrolle. Sie sind nützlich, wenn erweiterte Anwendungsebenenfunktionen erforderlich sind, um die Sicherheit und Wartbarkeit zu verbessern.

    Proxies sind Vermittler zwischen Client und Server. Ihre Funktionen variieren, einschließlich Sicherheitsaspekte wie Zugriffskontrolle. Der Schwerpunkt liegt auf Datenverkehrssteuerung und Sicherheit. 

    API-Gateways sind ideal für Microservices-Architekturen, in denen verschiedene APIs zentrale Verwaltung, Sicherheit und Skalierbarkeit benötigen. Im Gegensatz zu Load Balancern und Reverse Proxys bieten sie erweiterte Funktionen wie Authentifizierung, Ratenbegrenzung, Anfrage-/Antworttransformation und Überwachung. Wenn Ihre Anwendung stark von APIs abhängt, ist ein API-Gateway eine wertvolle Ergänzung für das Management und die Sicherheit Ihrer Schnittstellen.

    [6]

# Skalierungsmuster
### Definition 
    Ein Skalierungsmuster, auch als Skalierungsmuster oder Skalierungstyp bezeichnet, ist ein bewährter Ansatz oder eine bewährte Methode zur Bewältigung von Skalierbarkeitsanforderungen in Software- oder Informationssystemen. Skalierungsmuster bieten Richtlinien und bewährte Praktiken, um die Leistung, Verfügbarkeit und Kapazität einer Anwendung oder eines Systems zu erhöhen, wenn die Anforderungen steigen.

    Diese Muster helfen bei der Bewältigung von Herausforderungen wie einem zunehmenden Datenverkehr, steigenden Benutzerzahlen oder wachsenden Datenmengen. Beispiele für Skalierungsmuster sind das Load-Balancing, das Caching, die vertikale und horizontale Skalierung, das Sharding und viele andere. Jedes dieser Muster bietet eine spezifische Methode zur Verbesserung der Skalierbarkeit und hilft Entwicklern und Systemarchitekten dabei, geeignete Lösungen für ihre Anwendungen zu entwickeln. 
    [4]

## Horizontale Skalierung vs vertikale Skalierung:
    Horizontale Skalierung und vertikale Skalierung sind zwei verschiedene Ansätze zur Erweiterung und Anpassung von IT-Infrastrukturen. Bei der horizontalen Skalierung werden Daten in mehrere Knoten partitioniert, wodurch die Datenlast auf mehrere Server verteilt wird, während bei der vertikalen Skalierung alle Daten auf einem einzelnen Knoten verbleiben und die Skalierung durch die Erweiterung von CPU- und RAM-Ressourcen auf diesem Knoten erfolgt.

    Ein Beispiel für horizontale Skalierung ist die Verwendung von Datenbanken wie Cassandra oder MongoDB, während vertikale Skalierung oft bei relationalen Datenbanken wie MySQL und Amazon RDS zum Einsatz kommt.

    Horizontale Skalierung bietet den Vorteil, dass die Ausfallmöglichkeiten reduziert werden, da bei Bedarf einfach weitere Computer hinzugefügt werden können. Es gibt jedoch eine physikalische Obergrenze für die vertikale Skalierung, die durch die Kapazität der aktuellen Hardware begrenzt ist.

    Beim Nachrichtenaustausch und der Datenübermittlung sind die Kosten bei horizontaler Skalierung höher, da Daten kopiert werden müssen. Bei vertikaler Skalierung wird hingegen angenommen, dass ein gemeinsam genutzter Adressraum vorhanden ist, was die Datenfreigabe und Nachrichtenübermittlung erleichtert.

    Die Wahl zwischen horizontaler und vertikaler Skalierung hängt von verschiedenen Faktoren ab:
    Horizontale Skalierung ist vorteilhaft, wenn Sie die Ausfallmöglichkeiten minimieren und die Gesamtleistung durch die Hinzufügung zusätzlicher Computer verbessern möchten. Sie bietet hohe Zuverlässigkeit und bessere Topografische Verteilung für Anwendungen mit nationaler oder internationaler Kundschaft.

    Vertikale Skalierung hingegen ist sinnvoll, wenn Sie bereits über ausreichende Ressourcen auf einem einzelnen System verfügen und Ihr Budget begrenzt ist. Dieser Ansatz ermöglicht eine schnelle und kostengünstige Erweiterung Ihrer Infrastruktur, ist jedoch durch die Kapazität einer einzelnen Maschine begrenzt und könnte möglicherweise zukünftigen Anforderungen nicht gerecht werden.
    [7]
## Replication
    Replikation ist der Prozess, bei dem Daten von einer Datenbank auf einen anderen Server kopiert werden, um die Datenverfügbarkeit und -leistung zu verbessern. Dies ist besonders nützlich, um die Netzwerklatenz zu reduzieren und Benutzern weltweit schnellere Zugriffe auf Daten zu ermöglichen. Durch die Replikation werden auch Probleme mit Verfügbarkeit, Fehlertoleranz und Datendurchsatz gelöst. Es gibt verschiedene Algorithmen für die Datenbankreplikation, darunter Leader-basierte Replikation mit synchronen und asynchronen Strategien. Die Wahl des Replikationsansatzes hängt von den spezifischen Anforderungen und Kompromissen ab.
    [8]
## Partitioning:
    Mit der Skalierung von Systemen ist eine einzelne Maschine nicht mehr in der Lage, große Datensätze oder einen hohen Abfragedurchsatz zu verarbeiten. Durch die Partitionierung wird der Datensatz in kleinere Teilmengen aufgeteilt. Jede Partition wird zu einer eigenen kleinen Datenbank um die Leistung zu verbessern und die Skalierbarkeit zu erhöhen.
    (Auch zu Sharding).
    [9]
## Sharding:
    Sharding ist eine Datenbankoptimierungstechnik, bei der große Datenbanktabellen in kleinere Tabellen, genannt Shards oder Partitionen, aufgeteilt werden. Diese Shards können entweder identische Schemata mit eindeutigen Zeilen (horizontal Sharding) oder Teilschemata der Originaltabelle haben (vertikales Sharding).

    Der Zweck von Sharding besteht darin, Daten über mehrere Computer zu verteilen, um die horizontale Skalierbarkeit und die Leistungsfähigkeit zu verbessern. Die logischen Shards werden über verschiedene Knoten hinweg gespeichert und als physische Shards bezeichnet.

    Horizontales Sharding eignet sich besonders für Abfragen, die eine Teilmenge von Zeilen zurückgeben, die oft in Gruppen zusammengefasst sind, wie beispielsweise Abfragen mit Datumsfiltern.

    Vertikales Sharding ist nützlich, wenn Abfragen nur eine Teilmenge der Datenspalten zurückgeben. Es ermöglicht die Aufteilung von Daten auf separate Server.

    Shard-Datenbanken bieten eine höhere Verfügbarkeit und reduzieren die Auswirkungen von Ausfällen auf nur die betroffenen Datenblöcke. In der Praxis können Backup-Shards auf zusätzlichen Knoten repliziert werden.

    Sharding unterscheidet sich von Partitionierung darin, dass Sharding Daten auf mehrere Computer verteilt, während Partitionierung sich auf die Gruppierung von Teilmengen von Daten innerhalb einer einzelnen Datenbankinstanz bezieht. Die Begriffe "Sharding" und "Partitionierung" werden manchmal synonym verwendet, insbesondere wenn sie als "horizontal" oder "vertikal" gekennzeichnet sind.
    [10]

## Load Balancing:

    Load Balancing, auch Lastenausgleich genannt, ist eine Technik zur Optimierung der Leistung und Verfügbarkeit von Webservern und anderen IT-Ressourcen. Es wird eingesetzt, um den eingehenden Online-Traffic auf mehrere Server oder Ressourcen gleichmäßig zu verteilen. Dies hilft dabei, die Auslastung der Server zu reduzieren, die Zugriffsgeschwindigkeit zu erhöhen und die Verfügbarkeit sicherzustellen. Ein Load Balancer analysiert die Anfragen von Benutzern und leitet sie an die am besten geeigneten Server weiter. Dabei können verschiedene Algorithmen wie Round Robin, Weighted Round Robin, Least Connections und Weighted Least Connections verwendet werden, um die Aufgabenverteilung zu steuern. Load Balancing ist insbesondere in Umgebungen mit starkem Online-Traffic und in der E-Commerce-Branche von großer Bedeutung, da es die Stabilität, Hochverfügbarkeit und Skalierbarkeit von Online-Diensten sicherstellt.
    [11]
## Round robin etc.
    Load Balancing Algorithmen lassen sich in zwei Hauptkategorien unterteilen:

    Statisches Load Balancing
    Algorithmen für statisches Load Balancing folgen festen Regeln und sind unabhängig vom aktuellen Serverstatus:

    Round-Robin-Methode: Server werden nacheinander ausgewählt.
    Gewichtete Round-Robin-Methode: Server erhalten unterschiedliche Gewichtungen.
    IP-Hash-Methode: Die IP-Adresse des Clients wird in eine Nummer umgewandelt und Server zugewiesen.

    Dynamisches Load Balancing 
    Dynamische Load Balancing-Algorithmen untersuchen den aktuellen Status der Server, bevor der Datenverkehr verteilt wird:

    Least Connection Method: Server mit den wenigsten aktiven Verbindungen werden ausgewählt.
    Weighted Least Connection Method: Server mit geringer Kapazitätsauslastung werden bevorzugt.
    Least Response Time Method: Die Antwortzeit und aktive Verbindungen werden kombiniert, um den besten Server auszuwählen.
    Resource-Based Method: Der Load Balancer berücksichtigt die aktuelle Serverlast basierend auf Ressourcennutzung.
    [12]  
## Caching:
    Caching ist ein Verfahren, das dazu dient, die Leistung und Effizienz von Datenabrufen in Computersystemen zu steigern. Dabei werden Daten vorübergehend in einem schnelleren Speicher (Cache) gespeichert, um die Notwendigkeit zu verringern, auf die langsameren Speicherschichten zuzugreifen. Die Entscheidung, welche Daten im Cache gespeichert werden, basiert auf dem Prinzip der Referenzlokalität, da kürzlich angeforderte Daten wahrscheinlich erneut benötigt werden.

    Caches sind in Hierarchien (z. B. L1, L2, L3) organisiert und dienen dazu, Daten sequenziell abzurufen. Cache-Zugriffe können als "Cache-Treffer" bezeichnet werden, wenn Daten erfolgreich aus dem Cache gelesen werden, oder als "Cache-Fehler", wenn die Daten nicht gefunden werden. (local Caching)

    Es gibt verschiedene Caching-Strategien, darunter Durchschreibcache, Write-Around-Cache und Write-Back-Cache, die jeweils Vor- und Nachteile hinsichtlich Latenz und Datenkonsistenz bieten. Räumungsrichtlinien, wie FIFO, LIFO, LRU und andere, steuern, welche Daten im Cache behalten werden.

    Caching wird in verschiedenen Anwendungsfällen eingesetzt, darunter Datenbank-Caching, Content Delivery Network (CDN), Domain Name System (DNS)-Caching und API-Caching. Es ist jedoch nicht sinnvoll, Caching zu verwenden, wenn der Cache-Zugriff genauso lange dauert wie der Zugriff auf den primären Speicher, wenn Anfragen selten wiederholt werden oder wenn Daten häufig ändern.

    Die Vorteile von Caching umfassen die Verbesserung der Leistung, die Reduzierung von Latenz, die Entlastung der Datenbank, die Senkung der Netzwerkkosten und die Steigerung des Lesedurchsatzes.
    [13]

## Local, Distributed, Hierarchical, etc.
    Local Cache:
    Ein lokaler Cache ist ein clientseitiger Cache, der eine Teilmenge der Daten des Master-Space basierend auf der letzten Aktivität der Client-Anwendung verwaltet. Der lokale Cache wird leer erstellt, und wenn die Clientanwendung eine Abfrage ausführt, versucht der lokale Cache zunächst, diese aus dem Cache zu erfüllen. Andernfalls führt er sie im Master-Space aus und speichert das Ergebnis lokal für zukünftige Abfragen zwischen.

    Distributed Cache:
    Ein Distributed Cache ist ein System, das den Arbeitsspeicher (RAM) mehrerer vernetzter Computer in einem einzigen In-Memory-Datenspeicher zusammenfasst, um schnellen Datenzugriff zu ermöglichen. Diese verteilte Architektur ist besonders nützlich in Umgebungen mit hohem Datenvolumen und hoher Datenlast, da sie eine skalierbare Lösung bietet.

    Beliebte Anwendungsfälle für einen verteilten Cache umfassen die Beschleunigung von Anwendungen, das Speichern von Websitzungsdaten, die Reduzierung der Netzwerknutzung und -kosten sowie die Erhöhung der Hochverfügbarkeit. Der verteilte Cache ermöglicht es, häufig benötigte Daten in einer verteilten Umgebung effizient zu speichern und abzurufen.
    
    Hierarchical Cache:

    In einem Hierarchical Cache bestehen Cache-Ebenen, die miteinander kommunizieren. Diese Hierarchie erkennt das Konzept von übergeordneten (parent) und untergeordneten (child) Caches an. Der übergeordnete Cache ist dabei ein Cache weiter oben in der Hierarchie, an den Anfragen vom Traffic Server weitergeleitet werden können, während der untergeordnete Cache als ein Cache betrachtet wird, für den der Traffic Server selbst als übergeordneter Cache fungiert. Dieses Konzept ist typisch für Hierarchical Caches und ermöglicht die effiziente Organisation von Caches in verschiedenen Ebenen.
    [14] [15] [16]
## Skalierungswürfel
    Der Skalierungswürfel ist eine Visualisierung eines dreidimensionalen Skalierbarkeitsmodells, das im Buch "The Art of Scalability" beschrieben wird. Es definiert drei Möglichkeiten zur Skalierung einer Anwendung: X-Achse, Y-Achse und Z-Achse. Die X-Achsen-Skalierung verteilt die Last auf mehrere Instanzen, die Z-Achsen-Skalierung teilt Daten auf identische Instanzen auf und leitet Anfragen basierend auf Anfrageattributen weiter. Die Y-Achsen-Skalierung hingegen zerlegt die Anwendung in Dienste, wodurch eine monolithische Anwendung in unabhängige, skalierbare Microservices aufgeteilt wird. Dies ermöglicht eine bessere Beherrschung von Komplexität und verbesserte Skalierbarkeit.
    [17]

---
## Quellen

Hie Quellen Einfügen

