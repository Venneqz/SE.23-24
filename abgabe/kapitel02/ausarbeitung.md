# Kapitel 2

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
Beispiel: CDNs - Datenverteilung mit zentraler Steuerung. 2. Widerstandsfähigkeit:

Dezentrale Systeme:

Hohe Widerstandsfähigkeit gegenüber Ausfällen oder Angriffen.
Beispiel: Blockchain-Netzwerke.
Verteilte Systeme:

Widerstandsfähigkeit hängt von der Architektur ab.
Beispiel: Cloud-Plattformen - Robustheit durch Verteilung. 3. Skalierbarkeit:

Dezentrale Systeme:

Skalierbarkeit kann eine Herausforderung sein.
Beispiel: Bitcoin-Skalierbarkeitsprobleme.
Verteilte Systeme:

Bessere Skalierbarkeit durch Ressourcenverteilung.
Beispiel: Cloud-Computing. 4. Datenkonsistenz:

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

# Systemarchitektur verteilter Softwaresysteme

## Visualisierung von Systemarchitekturen

## Systemarchitekturmuster

### Client Server

  Wie der Name schonm sagt, besteht das ganze aus zwei sepreaten Teilen. Dem Client praktisch auf dem Front End der die UI ausführt und dem Server Aspekt auf dem das Backend läuft.
  Das ganze kenne viele schon durch zB Webentwicklung, wo ein Teil der Anwendung im Browser also auf dem Server läuft und der andere Teil eben auf dem lokalen Rechner des Nutzers. [18]

  Anwendung findet das Client Server Modell jedoch in vielen Bereichen in welchen Kommunikation zwischen zwei Rechnern stattfindet, bzw wo der Client eine Anfrage an den Server schickt und dieser dann eine Antwort zurückgibt. Das kann von einer einfachen Google Suche bis hin zu einem komplexen System für Firmendatenbanken reichen.[19]

#### Anwendungsbespiele

Die Anwendung von Clients findet täglich unzählige Male durch das Nutzen von Endgeräten statt. Manche Clients setzen Benutzerinnen und Benutzer bewusst ein, andere laufen unbemerkt verdeckt im Hintergrund.[23]

**E-Mail-Client**
Unter dem E-Mail-Client versteht man das E-Mail-Programm. Die Software eröffnet den Nutzerinnen und Nutzern alle Aktivitäten in der Interaktion mit E-Mails. Der E-Mail-Client ermöglicht, das Schreiben, Senden, Empfangen, Lesen, Filtern und Suchen von E-Mails. Protokolle zur Erfüllung dieser Funktionalitäten sind SMTP, IMAP oder POP. E-Mail-Clients sind entweder als eigenständiges Programm installiert oder integriert in Browser- oder Smartphone-Plugins. Bekannte Beispiele für E-Mail-Clients sind Microsoft Outlook, Mozilla Thunderbird und Apple Mail.[23]

**FTP-Client**
Der FTP-Client kommt dann zum Einsatz, wenn man Dateien auf einen FTP-Server hochlädt oder etwas von diesem herunterlädt. Der Client baut eine FTP-Verbindung zum Server auf. Der Datenaustausch findet über diese Verbindung statt.[23]

**SSH-Client**
Der SSH-Client ist ein Programm, das eine sichere und authentifizierte SSH-Verbindung zu einem Server herstellt. Das SSH-Protokoll ermöglicht es, dass die Datenübertragung zwischen den beiden verbundenen Computern sicher ist. SSH-Verbindungen finden somit bei der Verwaltung von Servern, Übermittlung von Daten sowie bei der Fernwartung ihre Anwendung. Ein sehr bekannter SSH-Client ist beispielsweise PuTTY unter Windows.[23]

**Webbrowser**
Der Webbrowser ermöglicht, Anfragen an Webserver zu senden und damit beispielsweise eine Webseite beim Server anzufragen und anzuzeigen. Das Protokoll, welches das Senden der Anfragen ermöglicht, ist HTTP. Bekannte und weitverbreitete Webbrowser sind Google Chrome und Firefox.[23]

**DNS-Client**
Ein DNS-Client gehört zu den Clients, welche unbemerkt für den Nutzer im Hintergrund laufen. Dieser ist im Netzwerkprotokoll TCP/IP eingebunden. Er löst den Computernamen oder die Webadresse in die dazugehörige IP-Adresse auf. Der Client ist somit der Vermittler zwischen dem Domain Name Service (DNS) und dem Programm, welches die IP-Adresse des Servers benötigt.[23]

#### Web Architekturen

##### PWA vs SPA vs MPA

1. **Progressive Web App (PWA)**:
   Merkmale:
   PWA ist im Wesentlichen eine Website oder Webanwendung, die bestimmte Technologien und Best Practices verwendet, um eine bessere Benutzererfahrung zu bieten.
   PWAs sind ressourceneffizient und schnell.
   Sie bieten Offline-Funktionalität, Push-Benachrichtigungen und können auf dem Startbildschirm eines Geräts installiert werden.
   Verwendungsszenarien:
   PWAs sind gut geeignet, um eine breite Palette von Anwendungen zu entwickeln, insbesondere solche, die auf Mobilgeräten gut funktionieren sollen.
   Sie eignen sich für Unternehmen, die die Reichweite ihrer Webanwendungen erhöhen und die Benutzerbindung verbessern möchten.[4]

2. **Single Page Application (SPA)**:
   Merkmale:
   SPAs sind Webanwendungen, die in einem einzigen HTML-Dokument geladen werden und den Inhalt dynamisch ändern, ohne die Seite neu zu laden.
   Sie verwenden JavaScript-Frameworks wie Angular, React oder Vue.js.
   SPAs bieten eine schnelle Benutzererfahrung, da sie nur Daten und Inhalte nachladen, die geändert werden müssen.
   Verwendungsszenarien:
   SPAs sind ideal für Anwendungen, bei denen Benutzer interaktiv auf verschiedenen Seiten navigieren, ohne die Seite jedes Mal neu zu laden, wie z. B. soziale Medien, E-Commerce und Dashboards.[4]

3. **Multi-Page Application (MPA)**:
   Merkmale:
   MPAs bestehen aus mehreren HTML-Seiten, von denen jede eine eigene Ansicht darstellt.
   Benutzer navigieren zwischen den Seiten, indem sie auf Links klicken, und jede Seite wird separat vom Server geladen.
   Verwendungsszenarien:
   MPAs sind geeignet für traditionelle Websites und Anwendungen, bei denen jede Seite eine klare Trennung von Inhalten und Funktionen aufweist, wie z. B. Unternehmenswebsites, Blogs und Nachrichtenportale.[4]

### Peer to peer

Cambridge Dictionary: a computer network in which each computer can act as a server for the others, allowing shared access to files and peripherals without the need for a central server. [20]

    Vorteile:
    -Schneller und einfacher Aufbau
    -Kein zentraler Server
    -Je mehr Teilnehmer desto besser, da mehr Ressourcen zur Verfügung stehen und es ausfallsicherer ist.
    -Keine zentrale Instanz, die die Kommunikation überwacht, kann zB vor Zensur schützen
    -ggf sicherer als Client-Server, da keine zentrale Instanz angegriffen werden kann [21]

    Nachteile:
    -Je größer desto aufwändiger wird die Verwaltung
    -Aufwendige Suche nach Dateien innerhalb des Netzwerks
    -Heterogen bezogen auf Leistung und Bandbreite [21]

#### Anwendungsbespiele

-**Datenaustausch**: Filesharing gehört zu den meistgenutzten Funktionen des P2P. Bekannte Filesharing-Netzwerke sind etwa Dropbox oder Google Drive.[22]

-**Direktnachrichten und Videotelefonie**: Besonders während der Pandemie hat dieses Peer-to-Peer-Beispiel an Bedeutung gewonnen. P2P Voice- und Videokommunikation erfolgt über Anbieter wie Skype oder Microsoft Teams.[22]

-**Kollaboration**: Die Zusammenarbeit von Teams wird durch Groupware, also kollaborative Softwarelösungen, erleichtert, indem Peers gemeinsam an Projekten arbeiten können. Ein typisches Beispiel hierfür ist die Meetinganwendung Adobe Connect.[22]

-**Blockchain**: P2P findet auch bei Kryptowährungen Anwendung, da Transaktionen über Blockchains ohne zentralen Server abgewickelt werden.[22]

### Event Driven Architecture

#### Event types

Ein Domain Event ist ein wichtiger Ereignistyp in der Domain-Driven Design (DDD)-Methodik. Es handelt sich um einen historischen Datensatz, der die Absicht und den relevanten Kontext eines bedeutsamen Zeitpunkts erfasst. Domain Events konzentrieren sich auf den "Bereich" oder das Geschäft und werden in der Vergangenheitsform ausgedrückt.

Diese Ereignisse sind benannt, um die Absicht klar auszudrücken und werden idealerweise in menschenverständlicher Sprache benannt. Anstatt Begriffe wie "OrderStateChanged" oder "OrderEvent" zu verwenden, ist es ratsam, Begriffe wie "OrderWasShipped" zu verwenden.

Im Gegensatz zu anderen Ereignistypen sind Domain Events hervorragend geeignet, um Absichten und Veränderungen festzuhalten. Sie bieten Einblicke in das Geschehen und sind besonders wichtig in event-sourced Systemen, in denen sie die Grundlage des Softwaremodells bilden.

Domain Events eignen sich besonders gut für die Erstellung von Lese-Modellen. Sie werden in Situationen verwendet, in denen die Anforderungen des Lese-Falls stark von den Datenmodellen abweichen, die zur Entscheidungsfindung verwendet werden. Diese ereigniszentrierte Darstellung ist nützlich für die Aggregation, sowohl bei der Erstellung von Lese-Modellen als auch bei analytischen Datenmodellen.[25]

**The Trigger or Signal Event**
Ein Trigger-Ereignis oder Signalereignis ist das kleinste Ereignis überhaupt. Normalerweise besteht ein solches Ereignis nur aus einer ID zur Referenzierung eines Aggregats oder einer Entität sowie gegebenenfalls einem Zeitstempel. Wie der Name "Trigger" andeutet, werden diese Ereignisse verwendet, um eine Reaktion auf der empfangenden Seite auszulösen. Trigger werden in der Regel verwendet, um andere Geschäftsprozesse über eine Änderung zu benachrichtigen. In Fällen, in denen sensible Daten gespeichert werden (insbesondere im Hinblick auf die DSGVO), können Trigger dazu beitragen, die Offenlegung der Ereignisinfrastruktur gegenüber anspruchsvollen Anforderungen zu verhindern.[25]

**The RESTful or "Fat" Event**
Die letzte Ereignis-Archetyp ist das "fat" Ereignis. Persönlich bevorzuge ich den Begriff "RESTful" Ereignis, da er besser beschreibt, was sich im Nutzlast (Payload) befindet. Diese Art von Ereignis enthält die vollständige Ressourcenrepräsentation, wie sie aus einer RESTful-API abgerufen wird. Es handelt sich um ein hervorragendes Integrationsereignis und ist besonders nützlich für externe Verbraucher. Dieser Ereignistyp wird auch als Event Carried State Transfer-Ereignis bezeichnet.

Im Vergleich zu Triggern verhindern RESTful-Ereignisse, dass Verbraucher einen Umweg zur API machen müssen. Im Vergleich zu Domain-Ereignissen vermeiden sie, dass Verbraucher mehrere Ereignisse kombinieren müssen, um ein vollständiges Bild zu erhalten.[25]

#### Message Broker

Ein Message Broker ist eine Software, die es Anwendungen, Systemen und Diensten ermöglicht, miteinander zu kommunizieren und Informationen auszutauschen. Dies geschieht, indem der Message Broker Nachrichten zwischen formalen Nachrichtenprotokollen übersetzt. Dadurch können voneinander abhängige Dienste direkt miteinander "sprechen", selbst wenn sie in verschiedenen Programmiersprachen geschrieben oder auf unterschiedlichen Plattformen implementiert wurden. [24]

Message Broker können Nachrichten validieren, speichern, routen und an die entsprechenden Empfänger weiterleiten. Sie fungieren als Vermittler zwischen anderen Anwendungen, was es Sendern ermöglicht, Nachrichten zu senden, ohne zu wissen, wo die Empfänger sich befinden, ob sie aktiv sind oder wie viele es gibt. Dies erleichtert die Entkopplung von Prozessen und Diensten innerhalb von Systemen. [24]

#### ESB vs Message Queue

Ein Enterprise Service Bus (ESB) ist eine zentrale Komponente in einer serviceorientierten Architektur (SOA). Die SOA ermöglicht es Systemen, miteinander zu kommunizieren und Daten über XML-formatierte Nachrichten auszutauschen. Der ESB fungiert als zentrale Schnittstelle für alle Systeme und vereinfacht die Integration, indem er sicherstellt, dass jedes System nur mit dem ESB kommunizieren muss. Der ESB übersetzt dann die Nachrichten in das richtige Format und leitet sie an das entsprechende System weiter. [26]

MessageQueue ermöglichen die asynchrone Kommunikation zwischen verschiedenen Komponenten oder Systemen, um die Systemzuverlässigkeit, Skalierbarkeit und Flexibilität zu erhöhen. Dies wird durch Hinzufügen eines Nachrichtenbrokers (wie RabbitMQ oder LavinMQ) erreicht, um Nachrichten oder Daten zwischen Prozessen oder Systemen zu übermitteln. Nachrichten werden von einem Produzenten an die Nachrichtenwarteschlange gesendet, wo sie gehalten werden, bis sie von einem Konsumenten verarbeitet werden. Dies entkoppelt den Produzenten vom Konsumenten und ermöglicht es ihnen, unabhängig voneinander zu arbeiten. Nachrichtenwarteschlangen können für verteiltes Computing, Aufgabenplanung und Workflow-Management verwendet werden. [27]

Ein ESB ist in der Regel umfangreicher und komplexer, während eine Message Queue auf die Verwaltung und Verteilung von Nachrichten beschränkt ist.

#### Anwendungsbeispiele

EDA findet in verschiedenen Anwendungsdomänen Anwendung, darunter: -**E-Commerce**: Verarbeitung von Bestellungen, Inventaraktualisierungen und Benachrichtigungen.

-**IoT (Internet of Things)**: Überwachung und Steuerung von vernetzten Geräten und Sensoren.

-**Finanzdienstleistungen**: Handel, Überweisungen und Betrugserkennung.

-**Logistik und Lieferkettenmanagement:** Sendungsverfolgung und Routenoptimierung.

-**Gesundheitswesen**: Patientenüberwachung und klinische Alarme.

-**Social Media**: Benachrichtigungen, Feeds und Aktivitätsströme.
[4]

## Modulare Architekturen

### Service oriented architecture (SOA)

Serviceorientierte Architektur (SOA) ist eine Methode der Softwareentwicklung, bei der Softwarekomponenten, sogenannte Services, genutzt werden, um Geschäftsanwendungen zu erstellen. Jeder Service erfüllt eine spezifische Geschäftsfunktion und kann plattform- und sprachübergreifend mit anderen Services kommunizieren. Entwickler setzen SOA ein, um Services in verschiedenen Systemen zu wiederverwenden oder unabhängige Services zu kombinieren, um komplexe Aufgaben zu lösen.
Ein Beispiel für die Anwendung von SOA ist die Benutzerauthentifizierung in einem Unternehmen. Statt den Authentifizierungscode für jede Anwendung neu zu schreiben, kann ein einziger Authentifizierungsservice erstellt und von allen Anwendungen wiederverwendet werden. In ähnlicher Weise können verschiedene Systeme in einer Gesundheitsorganisation, wie Patientenverwaltung und elektronische Gesundheitsakten, einen gemeinsamen Service aufrufen, um die Patientenregistrierung effizient durchzuführen. [28]

#### Service Discovery

Service Discovery (Dienstevermittlung) in Bezug auf Serviceorientierte Architektur (SOA) ist der Prozess, bei dem Webdienstanbieter lokalisiert und Webdienstbeschreibungen abgerufen werden, die zuvor veröffentlicht wurden. Dieser Prozess wird hauptsächlich durch ein Diensteregister durchgeführt, das relevante Metadaten zu verfügbaren und zukünftigen Diensten sowie Verweise auf die entsprechenden Dienstvertragsdokumente enthält, die Service Level Agreements (SLAs) enthalten können.
Besonders in modernen Architekturen, in denen einzelne Dienstinstanzen dynamisch erscheinen und verschwinden können, ist es entscheidend, dass Dienstnutzer von der genauen Kenntnis der Bereitstellungstopologie der Architektur entkoppelt sind.
Nach Abschluss des Entdeckungsprozesses sollte der Dienstentwickler oder die Client-Anwendung den exakten Standort eines Webdienstes (URI), dessen Fähigkeiten und die Art und Weise, wie auf ihn zugegriffen werden kann, kennen. Dies ermöglicht eine effiziente und flexible Kommunikation zwischen Diensten und Anwendungen in SOA, ohne umfangreiche manuelle Konfigurationen durchführen zu müssen. [29]

### Microservices

Microservices sind ein architekturbezogener und organisatorischer Ansatz in der Softwareentwicklung, bei dem Software aus kleinen unabhängigen Services besteht, die über sorgfältig definierte APIs kommunizieren. Diese Services gehören kleinen, eigenständigen Teams.
Microservices-Architekturen vereinfachen die Skalierbarkeit und verringern die Entwicklungszeit von Anwendungen, ermöglichen Innovationen und verkürzen die Markteinführungszeit für neue Funktionen. [30]

#### Monolith vs. Distributed Monolith vs. Microservice

**Monolithische Architektur** ist eine zusammenhängende Anwendung, bei der alle Prozesse eng miteinander verbunden sind. Wenn ein Prozess Probleme hat, muss die gesamte Anwendung skaliert werden, was bei wachsendem Code komplizierter wird. Dies erschwert Experimente und erhöht das Risiko für Ausfälle.

**Microservices-Architektur** hingegen baut Anwendungen aus unabhängigen, eigenständigen Komponenten auf, die über klare Schnittstellen kommunizieren. Jeder Service erfüllt eine bestimmte Funktion und kann unabhängig aktualisiert, bereitgestellt und skaliert werden, was die Flexibilität und Verfügbarkeit der Anwendung verbessert.[30]

#### Choreography Pattern vs Orchestration Pattern

**Choreografie**: Services interagieren direkt miteinander, ohne zentrale Kontrolle. Ereignisbasierte Kommunikation. Vorteile: lose Kopplung, dezentrale Kontrolle. Nachteile: komplexe Wartung, geringe Transparenz.

**Orchestrierung**: Zentraler Orchestrator steuert die Services. Befehlsbasierte Kommunikation. Vorteile: einfache Kontrolle, gute Sichtbarkeit, einfache Fehlerbehebung. Nachteile: engere Kopplung, Single Point of Failure.

**Wann Choreografie nutzen**: Bei unabhängigen Services, lose gekoppelt, Flexibilität benötigt.

**Wann Orchestrierung nutzen**: Abhängige Services, spezifische Reihenfolge, gute Überwachung.

**Mischung**: Beide Ansätze können kombiniert werden, um Flexibilität und Kontrolle zu bieten, je nach den Anforderungen der Architektur. [31]

#### Service Mesh

## Ein Service Mesh 
ist eine anpassbare Infrastrukturebene für eine Microservices-Anwendung. Es sorgt dafür, dass Anfragen in der komplexen Struktur von Diensten in einer cloudbasierten Anwendung zuverlässig übermittelt werden. Es ermöglicht flexible, zuverlässige und schnelle Kommunikation zwischen den einzelnen Diensten. Das Mesh bietet Funktionen wie die Erkennung von Diensten, Lastenausgleich, Verschlüsselung, Authentifizierung, Autorisierung und andere Möglichkeiten.[32]

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
#Wiederholungsbzw- Verständnisfragen:
1. Was ist ein verteiltes Softwaresystem?
2. Was ist der Unterschied zwischen einem Client-Server-Modell und einem Peer-to-Peer-Modell?
3. Was ist der Unterschied zwischen einem ESB und einer Message Queue?
4. Welche Skalierungsmuster kennst du?
5. Was ist der Unterschied zwischen horizontaler und vertikaler Skalierung?
---

## Quellen

[1]: karteikarte.com "hannemac" o.V. Definition: Verteiltes System (o. J.) https://www.karteikarte.com/card/164978/definition-verteiltes-system (11.10.2023)
[2]: Kev Z. Was ist ein verteiltes System? (o. J.) https://www.atlassian.com/de/microservices/microservices-architecture/distributed-architecture (11.10.2023)
[3]: karteikarte.com o.V hannemac Vorteile und Nachteile verteilter Systeme (o.J.) https://www.karteikarte.com/card/164978/definition-verteiltes-system (11.10.2023)
[4]: Chat GPT https://chat.openai.com/
[5]: vsis-www.informatik.uni-hamburg.de o. V. (o. J.) https://vsis-www.informatik.uni-hamburg.de/oldServer/teaching/ws-11.12/vis/folien/01-GRUNDL.pdf (11.10.2023)
[6]: Arslan Ahmad Load Balancer vs. Reverse Proxy vs. API Gateway (17.05.2023) https://medium.com/geekculture/load-balancer-vs-reverse-proxy-vs-api-gateway-e9ec5809180c#:~:text=Remember%20that%20load%20balancers%20distribute,these%20components%20for%20optimal%20results. (12.10.2023)
[7]: theastrologypage.com o.V (2023) https://theastrologypage.com/system-design (12.10.2023)
[8]: Pulkit Gupta System Design: Database Replication (Part 1) (02.04.2020) https://medium.com/@pulkitent/system-design-database-replication-part-1-3dcf4a300db1 (12.10.2023)
[9]: jguamie o.V Partitioning (2018) https://github.com/jguamie/system-design/blob/master/notes/partitioning.md (13.10.2023)
[10]: hazelcast.com o.V What is Sharding? (o. J.) https://hazelcast.com/glossary/sharding/ (13.10.2023)
[11] ovhcloud.com o.V. Was ist Loadbalancing? (o. J.)https://www.ovhcloud.com/de/public-cloud/what-load-balancing/#:~:text=Die%20Technologie%20des%20Loadbalancing%20(Lastenverteilung,Effizienz%20und%20Kapazit%C3%A4t%20der%20Infrastruktur.
[12] aws.amazon.com o.V Was ist Lastenverteilung? (o. J.) https://aws.amazon.com/de/what-is/load-balancing/ (13.10.2023)
[13] Karan Pratap Singh Caching (03.09.2022) https://dev.to/karanpratapsingh/system-design-caching-18j4 (13.10.2023)
[14] docs.gigaspaces.com o.V. Local Cache (o. J.) https://docs.gigaspaces.com/dev-java/local-cache.html (13.10.2023)
[15] hazelcast.com o.V. What Is a Distributed Cache? (o. J.) https://hazelcast.com/glossary/distributed-cache/ (13.10.2023)
[16] docs.trafficserver.apache.org o.V. Hierarchical Caching (o. J.) https://docs.trafficserver.apache.org/en/9.0.x/admin-guide/configuration/hierarchical-caching.en.html (13.10.2023)
[17] Karan Sharma The Scale Cube (11.07.2023) https://cserkaran.medium.com/the-scale-cube-d84ca0c2e900 (13.10.2023)
[18]: thenativewebGmbH. "Client-Server-Architekturen // deutsch" YouTube, hochgeladen von thenativewebGmbH, hochgeladen am [16.09.2020], URL: https://www.youtube.com/watch?v=GqjLcAbB5qE&ab_channel=thenativewebGmbH (abgerufen am 11.10.2023)
[19]: IT&Medieneinfacherklärt. "CLIENT-SERVER-MODELL einfach erklärt!" YouTube, hochgeladen von IT&Medieneinfacherklärt,hochgeladern am [27.04.2020] URL: https://www.youtube.com/watch?v=LwziP-ZrbUs (abgerufen am 11.10.2023)
[20]: Cambridge Dictionary. "peer-to-peer." Cambridge English Dictionary, URL: https://dictionary.cambridge.org/dictionary/english/peer-to-peer (abgerufen am 11.10.2023)
[21]: FlorianDalwigk. "Peer-To-Peer (einfach erklärt) | P2P (einfach erklärt)" YouTube, hochgeladen von FlorianDalwigk, hochgeladen am [07.11.2022], URL: https://www.youtube.com/watch?v=QR2Y2bdDWoM (abgerufen am 11.10.2023)
[22]: HubSpot. "Peer-to-Peer (P2P): Definition, Funktionsweise und Beispiele" HubSpot Blog, URL: https://blog.hubspot.de/website/peer-to-peer (abgerufen am 11.10.2023)
[23]: IONOS. "Was ist ein Client?" IONOS Digital Guide, URL: https://www.ionos.de/digitalguide/server/knowhow/was-ist-ein-client/ (abgerufen am 11.10.2023)
[24]: IBM. "Message Brokers." IBM Topics, URL: https://www.ibm.com/topics/message-brokers#:~:text=A%20message%20broker%20is%20software,messages%20between%20formal%20messaging%20protocols. (abgerufen am 11.10.2023)
[25]: Frank de Jonge. "The Different Types of Events in Event-Driven Systems." Frank de Jonge's Blog, URL: https://blog.frankdejonge.nl/the-different-types-of-events-in-event-driven-systems/#:~:text=Three%20event%20archetypes&text=These%20types%20of%20events%20are,The%20RESTful%20or%20%22Fat%22%20Event (abgerufen am 11.10.2023)
[26]: LoiLiangYang. "Enterprise Service Bus" YouTube, hochgeladen von LoiLiangYang, URL: https://www.youtube.com/watch?v=VHzWswQNtgk&ab_channel=LoiLiangYang (abgerufen am 11.10.2023)
[27]: CloudAMQP. "What is Message Queuing?" CloudAMQP Blog, URL: https://www.cloudamqp.com/blog/what-is-message-queuing.html (abgerufen am 11.10.2023)
[28]: Amazon Web Services (AWS). "Service-Oriented Architecture (SOA)." AWS, URL: https://aws.amazon.com/de/what-is/service-oriented-architecture/ (abgerufen am 11.10.2023)
[29]: Coforge. "SOA Service Discovery, Repository and Service Discovery." Coforge Blog, URL: https://www.coforge.com/blog/soa-service-registry/repository-and-service-discovery#:~:text=SOA%20Service%20Discovery,that%20have%20been%20previously%20published. (abgerufen am 11.10.2023)
[30]: Amazon Web Services (AWS). "Microservices." AWS, URL: https://aws.amazon.com/de/microservices/ (abgerufen am 14. Oktober 2023)
[31]: Camunda. "Orchestration vs. Choreography." Camunda Blog, URL: https://camunda.com/blog/2023/02/orchestration-vs-choreography/ (abgerufen am 14. Oktober 2023)
[32]: TriggerMesh. "What Is a Service Mesh?" TriggerMesh FAQ, URL: https://www.triggermesh.com/faq/what-is-a-service-mesh (abgerufen am 14. Oktober 2023)
