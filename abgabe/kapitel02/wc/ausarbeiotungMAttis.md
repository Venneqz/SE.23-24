# Systemarchitektur verteilter Softwaresysteme
## Visualisierung von Systemarchitekturen
## Systemarchitekturmuster
### Client Server
Wie der Name schonm sagt, besteht das ganze aus zwei sepreaten Teilen. Dem Client praktisch auf dem Front End der die UI ausführt und dem Server Aspekt auf dem das Backend läuft.
Das ganze kenne viele schon durch zB Webentwicklung, wo ein Teil der Anwendung im Browser also auf dem Server läuft und der andere Teil eben auf dem lokalen Rechner des Nutzers. [18]

Anwendung findet das Client Server Modell jedoch in vielen Bereichen in welchen Kommunikation zwischen zwei Rechnern stattfindet, bzw wo der Client eine Anfrage an den Server schickt und dieser dann eine Antwort zurückgibt. Das kann von einer einfachen Google Suche bis hin zu einem komplexen System für Firmendatenbanken reichen.[19]
#### Anwendungsbespiele
Die Anwendung von Clients findet täglich unzählige Male durch das Nutzen von Endgeräten statt. Manche Clients setzen Benutzerinnen und Benutzer bewusst ein, andere laufen unbemerkt verdeckt im Hintergrund.[23]

__E-Mail-Client__
Unter dem E-Mail-Client versteht man das E-Mail-Programm. Die Software eröffnet den Nutzerinnen und Nutzern alle Aktivitäten in der Interaktion mit E-Mails. Der E-Mail-Client ermöglicht, das Schreiben, Senden, Empfangen, Lesen, Filtern und Suchen von E-Mails. Protokolle zur Erfüllung dieser Funktionalitäten sind SMTP, IMAP oder POP. E-Mail-Clients sind entweder als eigenständiges Programm installiert oder integriert in Browser- oder Smartphone-Plugins. Bekannte Beispiele für E-Mail-Clients sind Microsoft Outlook, Mozilla Thunderbird und Apple Mail.[23]

__FTP-Client__
Der FTP-Client kommt dann zum Einsatz, wenn man Dateien auf einen FTP-Server hochlädt oder etwas von diesem herunterlädt. Der Client baut eine FTP-Verbindung zum Server auf. Der Datenaustausch findet über diese Verbindung statt.[23]

__SSH-Client__
Der SSH-Client ist ein Programm, das eine sichere und authentifizierte SSH-Verbindung zu einem Server herstellt. Das SSH-Protokoll ermöglicht es, dass die Datenübertragung zwischen den beiden verbundenen Computern sicher ist. SSH-Verbindungen finden somit bei der Verwaltung von Servern, Übermittlung von Daten sowie bei der Fernwartung ihre Anwendung. Ein sehr bekannter SSH-Client ist beispielsweise PuTTY unter Windows.[23]

__Webbrowser__
Der Webbrowser ermöglicht, Anfragen an Webserver zu senden und damit beispielsweise eine Webseite beim Server anzufragen und anzuzeigen. Das Protokoll, welches das Senden der Anfragen ermöglicht, ist HTTP. Bekannte und weitverbreitete Webbrowser sind Google Chrome und Firefox.[23]

__DNS-Client__
Ein DNS-Client gehört zu den Clients, welche unbemerkt für den Nutzer im Hintergrund laufen. Dieser ist im Netzwerkprotokoll TCP/IP eingebunden. Er löst den Computernamen oder die Webadresse in die dazugehörige IP-Adresse auf. Der Client ist somit der Vermittler zwischen dem Domain Name Service (DNS) und dem Programm, welches die IP-Adresse des Servers benötigt.[23]
#### Web Architekturen
##### PWA vs SPA vs MPA
1. __Progressive Web App (PWA)__:
Merkmale:
PWA ist im Wesentlichen eine Website oder Webanwendung, die bestimmte Technologien und Best Practices verwendet, um eine bessere Benutzererfahrung zu bieten.
PWAs sind ressourceneffizient und schnell.
Sie bieten Offline-Funktionalität, Push-Benachrichtigungen und können auf dem Startbildschirm eines Geräts installiert werden.
Verwendungsszenarien:
PWAs sind gut geeignet, um eine breite Palette von Anwendungen zu entwickeln, insbesondere solche, die auf Mobilgeräten gut funktionieren sollen.
Sie eignen sich für Unternehmen, die die Reichweite ihrer Webanwendungen erhöhen und die Benutzerbindung verbessern möchten.[4]

2. __Single Page Application (SPA)__:
    Merkmale:
    SPAs sind Webanwendungen, die in einem einzigen HTML-Dokument geladen werden und den Inhalt dynamisch ändern, ohne die Seite neu zu laden.
    Sie verwenden JavaScript-Frameworks wie Angular, React oder Vue.js.
    SPAs bieten eine schnelle Benutzererfahrung, da sie nur Daten und Inhalte nachladen, die geändert werden müssen.
    Verwendungsszenarien:
    SPAs sind ideal für Anwendungen, bei denen Benutzer interaktiv auf verschiedenen Seiten navigieren, ohne die Seite jedes Mal neu zu laden, wie z. B. soziale Medien, E-Commerce und Dashboards.[4]

3. __Multi-Page Application (MPA)__:
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
-__Datenaustausch__: Filesharing gehört zu den meistgenutzten Funktionen des P2P. Bekannte Filesharing-Netzwerke sind etwa Dropbox oder Google Drive.[22]

-__Direktnachrichten und Videotelefonie__: Besonders während der Pandemie hat dieses Peer-to-Peer-Beispiel an Bedeutung gewonnen. P2P Voice- und Videokommunikation erfolgt über Anbieter wie Skype oder Microsoft Teams.[22]

-__Kollaboration__: Die Zusammenarbeit von Teams wird durch Groupware, also kollaborative Softwarelösungen, erleichtert, indem Peers gemeinsam an Projekten arbeiten können. Ein typisches Beispiel hierfür ist die Meetinganwendung Adobe Connect.[22]

-__Blockchain__: P2P findet auch bei Kryptowährungen Anwendung, da Transaktionen über Blockchains ohne zentralen Server abgewickelt werden.[22]
### Event Driven Architecture
#### Event types
Ein Domain Event ist ein wichtiger Ereignistyp in der Domain-Driven Design (DDD)-Methodik. Es handelt sich um einen historischen Datensatz, der die Absicht und den relevanten Kontext eines bedeutsamen Zeitpunkts erfasst. Domain Events konzentrieren sich auf den "Bereich" oder das Geschäft und werden in der Vergangenheitsform ausgedrückt.

Diese Ereignisse sind benannt, um die Absicht klar auszudrücken und werden idealerweise in menschenverständlicher Sprache benannt. Anstatt Begriffe wie "OrderStateChanged" oder "OrderEvent" zu verwenden, ist es ratsam, Begriffe wie "OrderWasShipped" zu verwenden.

Im Gegensatz zu anderen Ereignistypen sind Domain Events hervorragend geeignet, um Absichten und Veränderungen festzuhalten. Sie bieten Einblicke in das Geschehen und sind besonders wichtig in event-sourced Systemen, in denen sie die Grundlage des Softwaremodells bilden.

Domain Events eignen sich besonders gut für die Erstellung von Lese-Modellen. Sie werden in Situationen verwendet, in denen die Anforderungen des Lese-Falls stark von den Datenmodellen abweichen, die zur Entscheidungsfindung verwendet werden. Diese ereigniszentrierte Darstellung ist nützlich für die Aggregation, sowohl bei der Erstellung von Lese-Modellen als auch bei analytischen Datenmodellen.[25]

__The Trigger or Signal Event__
Ein Trigger-Ereignis oder Signalereignis ist das kleinste Ereignis überhaupt. Normalerweise besteht ein solches Ereignis nur aus einer ID zur Referenzierung eines Aggregats oder einer Entität sowie gegebenenfalls einem Zeitstempel. Wie der Name "Trigger" andeutet, werden diese Ereignisse verwendet, um eine Reaktion auf der empfangenden Seite auszulösen. Trigger werden in der Regel verwendet, um andere Geschäftsprozesse über eine Änderung zu benachrichtigen. In Fällen, in denen sensible Daten gespeichert werden (insbesondere im Hinblick auf die DSGVO), können Trigger dazu beitragen, die Offenlegung der Ereignisinfrastruktur gegenüber anspruchsvollen Anforderungen zu verhindern.[259]

__The RESTful or "Fat" Event__
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
EDA findet in verschiedenen Anwendungsdomänen Anwendung, darunter:
-__E-Commerce__: Verarbeitung von Bestellungen, Inventaraktualisierungen und Benachrichtigungen.

-__IoT (Internet of Things)__: Überwachung und Steuerung von vernetzten Geräten und Sensoren.

-__Finanzdienstleistungen__: Handel, Überweisungen und Betrugserkennung.

-__Logistik und Lieferkettenmanagement:__ Sendungsverfolgung und Routenoptimierung.

-__Gesundheitswesen__: Patientenüberwachung und klinische Alarme.

-__Social Media__: Benachrichtigungen, Feeds und Aktivitätsströme.
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
__Monolithische Architektur__ ist eine zusammenhängende Anwendung, bei der alle Prozesse eng miteinander verbunden sind. Wenn ein Prozess Probleme hat, muss die gesamte Anwendung skaliert werden, was bei wachsendem Code komplizierter wird. Dies erschwert Experimente und erhöht das Risiko für Ausfälle.

__Microservices-Architektur__ hingegen baut Anwendungen aus unabhängigen, eigenständigen Komponenten auf, die über klare Schnittstellen kommunizieren. Jeder Service erfüllt eine bestimmte Funktion und kann unabhängig aktualisiert, bereitgestellt und skaliert werden, was die Flexibilität und Verfügbarkeit der Anwendung verbessert.[30]
#### Choreography Pattern vs Orchestration Pattern
__Choreografie__: Services interagieren direkt miteinander, ohne zentrale Kontrolle. Ereignisbasierte Kommunikation. Vorteile: lose Kopplung, dezentrale Kontrolle. Nachteile: komplexe Wartung, geringe Transparenz.

__Orchestrierung__: Zentraler Orchestrator steuert die Services. Befehlsbasierte Kommunikation. Vorteile: einfache Kontrolle, gute Sichtbarkeit, einfache Fehlerbehebung. Nachteile: engere Kopplung, Single Point of Failure.

__Wann Choreografie nutzen__: Bei unabhängigen Services, lose gekoppelt, Flexibilität benötigt.

__Wann Orchestrierung nutzen__: Abhängige Services, spezifische Reihenfolge, gute Überwachung.

__Mischung__: Beide Ansätze können kombiniert werden, um Flexibilität und Kontrolle zu bieten, je nach den Anforderungen der Architektur. [31]
#### Service Mesh
Ein Service Mesh ist eine anpassbare Infrastrukturebene für eine Microservices-Anwendung. Es sorgt dafür, dass Anfragen in der komplexen Struktur von Diensten in einer cloudbasierten Anwendung zuverlässig übermittelt werden. Es ermöglicht flexible, zuverlässige und schnelle Kommunikation zwischen den einzelnen Diensten. Das Mesh bietet Funktionen wie die Erkennung von Diensten, Lastenausgleich, Verschlüsselung, Authentifizierung, Autorisierung und andere Möglichkeiten.[32]

#Quellen:
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
Deine Quellen:
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
