# Systemarchitektur verteilter Softwaresysteme
## Visualisierung von Systemarchitekturen
## Systemarchitekturmuster
## Client Server
Wie der Name schonm sagt, besteht das ganze aus zwei sepreaten Teilen. Dem Client praktisch auf dem Front End der die UI ausführt und dem Server Aspekt auf dem das Backend läuft.
Das ganze kenne viele schon durch zB Webentwicklung, wo ein Teil der Anwendung im Browser also auf dem Server läuft und der andere Teil eben auf dem lokalen Rechner des Nutzers. [5]

Anwendung findet das Client Server Modell jedoch in vielen Bereichen in welchen Kommunikation zwischen zwei Rechnern stattfindet, bzw wo der Client eine Anfrage an den Server schickt und dieser dann eine Antwort zurückgibt. Das kann von einer einfachen Google Suche bis hin zu einem komplexen System für Firmendatenbanken reichen.[6]
#### Anwendungsbespiele
Die Anwendung von Clients findet täglich unzählige Male durch das Nutzen von Endgeräten statt. Manche Clients setzen Benutzerinnen und Benutzer bewusst ein, andere laufen unbemerkt verdeckt im Hintergrund.[4]

E-Mail-Client
Unter dem E-Mail-Client versteht man das E-Mail-Programm. Die Software eröffnet den Nutzerinnen und Nutzern alle Aktivitäten in der Interaktion mit E-Mails. Der E-Mail-Client ermöglicht, das Schreiben, Senden, Empfangen, Lesen, Filtern und Suchen von E-Mails. Protokolle zur Erfüllung dieser Funktionalitäten sind SMTP, IMAP oder POP. E-Mail-Clients sind entweder als eigenständiges Programm installiert oder integriert in Browser- oder Smartphone-Plugins. Bekannte Beispiele für E-Mail-Clients sind Microsoft Outlook, Mozilla Thunderbird und Apple Mail.[4]

FTP-Client
Der FTP-Client kommt dann zum Einsatz, wenn man Dateien auf einen FTP-Server hochlädt oder etwas von diesem herunterlädt. Der Client baut eine FTP-Verbindung zum Server auf. Der Datenaustausch findet über diese Verbindung statt.[4]

SSH-Client
Der SSH-Client ist ein Programm, das eine sichere und authentifizierte SSH-Verbindung zu einem Server herstellt. Das SSH-Protokoll ermöglicht es, dass die Datenübertragung zwischen den beiden verbundenen Computern sicher ist. SSH-Verbindungen finden somit bei der Verwaltung von Servern, Übermittlung von Daten sowie bei der Fernwartung ihre Anwendung. Ein sehr bekannter SSH-Client ist beispielsweise PuTTY unter Windows.[4]

Webbrowser
Der Webbrowser ermöglicht, Anfragen an Webserver zu senden und damit beispielsweise eine Webseite beim Server anzufragen und anzuzeigen. Das Protokoll, welches das Senden der Anfragen ermöglicht, ist HTTP. Bekannte und weitverbreitete Webbrowser sind Google Chrome und Firefox.[4]

DNS-Client
Ein DNS-Client gehört zu den Clients, welche unbemerkt für den Nutzer im Hintergrund laufen. Dieser ist im Netzwerkprotokoll TCP/IP eingebunden. Er löst den Computernamen oder die Webadresse in die dazugehörige IP-Adresse auf. Der Client ist somit der Vermittler zwischen dem Domain Name Service (DNS) und dem Programm, welches die IP-Adresse des Servers benötigt.[4]
#### Web Architekturen
##### PWA vs SPA vs MPA
1. Progressive Web App (PWA):
Merkmale:
PWA ist im Wesentlichen eine Website oder Webanwendung, die bestimmte Technologien und Best Practices verwendet, um eine bessere Benutzererfahrung zu bieten.
PWAs sind ressourceneffizient und schnell.
Sie bieten Offline-Funktionalität, Push-Benachrichtigungen und können auf dem Startbildschirm eines Geräts installiert werden.
Verwendungsszenarien:
PWAs sind gut geeignet, um eine breite Palette von Anwendungen zu entwickeln, insbesondere solche, die auf Mobilgeräten gut funktionieren sollen.
Sie eignen sich für Unternehmen, die die Reichweite ihrer Webanwendungen erhöhen und die Benutzerbindung verbessern möchten.[6]

2. Single Page Application (SPA):
    Merkmale:
    SPAs sind Webanwendungen, die in einem einzigen HTML-Dokument geladen werden und den Inhalt dynamisch ändern, ohne die Seite neu zu laden.
    Sie verwenden JavaScript-Frameworks wie Angular, React oder Vue.js.
    SPAs bieten eine schnelle Benutzererfahrung, da sie nur Daten und Inhalte nachladen, die geändert werden müssen.
    Verwendungsszenarien:
    SPAs sind ideal für Anwendungen, bei denen Benutzer interaktiv auf verschiedenen Seiten navigieren, ohne die Seite jedes Mal neu zu laden, wie z. B. soziale Medien, E-Commerce und Dashboards.[6]

3. Multi-Page Application (MPA):
     Merkmale:
    MPAs bestehen aus mehreren HTML-Seiten, von denen jede eine eigene Ansicht darstellt.
    Benutzer navigieren zwischen den Seiten, indem sie auf Links klicken, und jede Seite wird separat vom Server geladen.
    Verwendungsszenarien:
    MPAs sind geeignet für traditionelle Websites und Anwendungen, bei denen jede Seite eine klare Trennung von Inhalten und Funktionen aufweist, wie z. B. Unternehmenswebsites, Blogs und Nachrichtenportale.[6]
### Peer to peer
#### Anwendungsbespiele
### Event Driven Architecture
#### Event types
#### Message Broker
#### ESB vs Message Queue
#### Anwendungsbeispiele
## Modulare Architekturen
### Service oriented architecture (SOA) 
#### Service Discovery
### Microservices
#### Monolith vs. Distributed Monolith vs. Microservice
#### Choreography Pattern vs Orchestration Pattern
#### Service Mesh