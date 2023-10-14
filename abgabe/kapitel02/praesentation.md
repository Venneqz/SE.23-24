---
title: Software Systeme
author: Marvin Petschulat, Mattis Wellenbüscher
---

# Inhaltsverzeichnis

- Verteilte Softwaresysteme
- Systemarchitektur verteilter Softwaresysteme
- Systemdesign
- Quellen

---

# Verteilte Softwaresysteme

1. Verteilte Softwaresysteme Definition
1. Eigenschaften
1. Vorteile
1. Nachteile
1. Motivation (Warum man Verteilung braucht)
1. Distributed vs decentralized
1. Concurrent vs parallel

---

# Verteilte Softwaresysteme Definition

ein Programmsystem, das aus Teilsystemen besteht,
die auf mehreren lose gekoppelten Prozessoren implementiert
und über eine Netzwerk verbunden sind.

Lose gekoppelt heißt in diesem Zusammenhang, dass Prozessoren standortbezogen von einander getrennt sind.

In verteilten Systemen können verschiedene Leute und Programme gemeinsam auf Dinge wie Drucker, Dateien und Speicher zugreifen. Das hilft, die Dinge effizienter zu nutzen und spart Ressourcen.

---

# Eigenschaften

1. Gemeinsame Ressourcennutzung

   - Hardware, Software und Daten gemeinsam nutzen.

1. Simultane Verarbeitung

   - Mehrere Rechner bearbeiten gleichzeitig dieselben Aufgaben.

1. Skalierbarkeit

   - Kapazität erweiterbar durch Hinzufügen von Rechnern.

1. Fehlererkennung

   - Einfachere Fehlererkennung im verteilten System.

1. Transparenz

   - Kommunikation und Zugriff zwischen den Systemknoten.


---

# Vorteile

- **Effiziente Ressourcennutzung:** Gemeinsame Nutzung von Druckern und Speicher für maximale Effizienz.
- **Offenheit und Interoperabilität:** Integration verschiedener Hersteller und Technologien.
- **Parallelität für Leistungssteigerung:** Gleichzeitige Prozessausführung auf verschiedenen Ressourcen.
- **Skalierbarkeit:** Anpassungsfähigkeit an wachsende Anforderungen.
- **Fehlertoleranz:** Umschalten auf alternative Ressourcen bei Hardware- oder Softwareausfällen.
- **Benutzerfreundlichkeit:** Nutzung ohne vertiefte Kenntnisse der Verteilung.
- **Kosteneffizienz:** Niedrigere Gesamtkosten in kleineren verteilten Systemen.


---

# Nachteile

- **Komplexität:** Höherer Entwicklungsaufwand und Wartungsaufwand.
- **Sicherheit:** Schwierigere Kontrolle und Gefährdung der Datensicherheit.
- **Manageability:** Koordination verschiedener Komponenten erfordert hohen Wartungsaufwand.
- **Unvorhersehbarkeit:** Schwierig vorhersehbares Verhalten, insbesondere bei Lastverteilung.
- **Kommunikationsaufwand:** Erhöhter Kommunikationsaufwand in verteilten Systemen.
- **Konsistenzprobleme:** Schwierigkeiten bei der Aufrechterhaltung der Datenkonsistenz über verschiedene Knoten hinweg.
- **Skalierbarkeitsprobleme:** Unzureichende Skalierbarkeitsplanung kann Probleme verursachen.

  *Trotzdem dieser Nachteile sind verteilte Systeme in vielen Fällen unverzichtbar, da sie Flexibilität, Ressourcennutzung und Skalierbarkeit bieten. Mit sorgfältiger Planung und Sicherheitsmaßnahmen können die Nachteile minimiert werden.*

---

# Motivation (Warum man Verteilung braucht):

## Mangelnde Möglichkeiten der Zentralrechner
- Verbesserte Antwortzeiten durch Lastverteilung.
- Effizientere Ausführung interaktiver Anwendungen.
- Unterstützung komplexer Benutzerschnittstellen und Grafiken.

## Anforderungen neuer Anwendungen
- Grafische Benutzerschnittstellen für moderne Anwendungen.
- Bewältigung von Lastspitzen für kurze Antwortzeiten.

## Weite Verbreitung mächtiger PCs und Workstations
- Effiziente Ausführung anspruchsvoller Anwendungen.
- Bereitstellung von Rechenleistung und Speicherressourcen.

## Fortgeschrittene Netztechnologien
- Kommunikation und Koordination über verschiedene Entfernungen.
- Skalierbarkeit und Flexibilität des Systems.

## Gemeinsame Nutzung von Ressourcen
- Effiziente Ressourcennutzung und Kostenersparnis.

## Geringere Hardware-Kosten
- Effiziente Nutzung vorhandener Hardware.
- Realisierung von Skaleneffekten.

---

# Distributed vs decentralized

## Kontrolle

### Dezentrale Systeme
- Keine zentrale Kontrolle; Entscheidungen von einzelnen Teilnehmern.
- Betont Autonomie und Unabhängigkeit.
- Beispiel: Bitcoin - keine zentrale Bank.

### Verteilte Systeme
- Koordination kann zentral oder begrenzt sein.
- Verteilung von Ressourcen über Knoten.
- Beispiel: CDNs - Datenverteilung mit zentraler Steuerung.

## Widerstandsfähigkeit

### Dezentrale Systeme
- Hohe Widerstandsfähigkeit gegenüber Ausfällen oder Angriffen.
- Beispiel: Blockchain-Netzwerke.

### Verteilte Systeme
- Widerstandsfähigkeit hängt von der Architektur ab.
- Beispiel: Cloud-Plattformen - Robustheit durch Verteilung.

## Skalierbarkeit

### Dezentrale Systeme
- Skalierbarkeit kann eine Herausforderung sein.
- Beispiel: Bitcoin-Skalierbarkeitsprobleme.

### Verteilte Systeme
- Bessere Skalierbarkeit durch Ressourcenverteilung.
- Beispiel: Cloud-Computing.

## Datenkonsistenz

### Dezentrale Systeme
- Konsistenz kann herausfordernd sein, erfordert Konsensmechanismen.
- Beispiel: Blockchain-Netzwerke.

### Verteilte Systeme
- Einfachere Konsistenz dank zentraler Koordination.
- Beispiel: Zentrale Unternehmensdatenbanken.

---

# Concurrent vs parallel

## Concurrent (Gleichzeitige Abläufe)

- Bezieht sich auf die gleichzeitige Ausführung von Aufgaben oder Prozessen in einem verteilten System.
- Reihenfolge der Ausführung ist nicht explizit festgelegt.
- Effiziente Nutzung von Ressourcen und Verarbeitung von Anfragen ohne spezifische Abhängigkeiten zwischen den Prozessen.

## Parallel (Tatsächlich gleichzeitige Ausführung)

- Bezieht sich auf die tatsächliche gleichzeitige Ausführung von Aufgaben oder Prozessen auf verschiedenen Knoten oder Systemen.
- Erfordert eine explizite Koordination zwischen den Knoten.
- Aufteilung einer Aufgabe in Teilaufgaben und parallele Ausführung mit Synchronisation für kohärente Ergebnisse.

## Beispiel: Echtzeittransaktionsverarbeitung

- Concurrent: Kunden geben gleichzeitig Bestellungen auf der Website auf, die unabhängig voneinander verarbeitet werden, ohne feste Reihenfolge.

- Parallel: In Spitzenzeiten arbeiten separate Server in verschiedenen Rechenzentren parallel, um Bestellungen zu verarbeiten. Echtzeit-Synchronisation gewährleistet kohärente Ergebnisse.

In verteilten Systemen ist die Unterscheidung zwischen Concurrent und Parallel wichtig, da sie Auswirkungen auf Skalierbarkeit, Leistung und Synchronisation haben kann. Concurrent Computing bietet Flexibilität, während Parallel Computing zusätzliche Koordination erfordert, um kohärente Ergebnisse sicherzustellen.

---

# Systemarchitektur verteilter Softwaresysteme

1. Visualisierung von Systemarchitekturen
1. Systemarchitekturmuster
1. Modulare Architekturen

---

# Systemdesign

1. Systemdesign Definition
1. API Gateway vs Proxy vs Reverse Proxy vs Load Balancer
1. Skalierungsmuster


---

# Systemdesign Definition

**Beim Systemdesign werden die Elemente eines Systems wie Architektur, Module und Komponenten, die verschiedenen Schnittstellen dieser Komponenten und die Daten, die das System durchlaufen, definiert. Es soll die spezifischen Bedürfnisse und Anforderungen eines Unternehmens oder einer Organisation durch die Entwicklung eines kohärenten und gut funktionierenden Systems erfüllen.**


---

# API Gateway

- **Definition**
  - Ein essenzieller Bestandteil in Microservices-Architekturen.
  - Zentraler Koordinator für Client-Anfragen an Backend-Dienste.
  
- **Funktionen**
  - Zentrale Authentifizierung und Autorisierung.
  - Ratenbegrenzungen für Anfragen.
  - Anpassung von Anfragen und Antworten.
  - Umfassende Überwachung und Protokollierung.

- **Beispiele**
  - Erfolgreicher Einsatz bei Unternehmen wie Netflix.
  - Verwaltung komplexer Microservices-Systeme.
  - Bereitstellung skalierbarer, sichere und flexible Lösungen für Millionen täglicher API-Aufrufe.

- **Wichtigkeit**
  - Unverzichtbare Werkzeuge zur effizienten Verwaltung und Absicherung von APIs in modernen Anwendungen.

API-Gateways spielen eine entscheidende Rolle in der Verwaltung und Absicherung von APIs, insbesondere in komplexen Microservices-Systemen.

---

# Proxy

- **Definition**
  - Ein Proxy ist eine Zwischeninstanz oder Vermittler, der als Schnittstelle zwischen einem Client und einem Server fungiert.
  - Er empfängt Anfragen vom Client und leitet sie an den Zielserver weiter.

- **Funktionen**
  - Datenverkehrsteuerung: Proxies steuern den Datenverkehr, um den Fluss von Anfragen und Antworten zu regulieren.
  - Überwachung: Sie ermöglichen die Überwachung des Datenverkehrs und bieten Einblicke in die Kommunikation zwischen Client und Server.
  - Sicherheit: Proxies dienen der Sicherung des Datenverkehrs und dem Schutz vor Bedrohungen.
  - Performance-Optimierung: Sie optimieren die Leistung durch Funktionen wie Caching und Komprimierung.

- **Einsatzbereiche**
  - Netzwerksicherheit: Proxies tragen zur Sicherheit von Netzwerken bei, indem sie unerwünschte oder schädliche Inhalte filtern.
  - Zugriffskontrolle: Sie ermöglichen die Steuerung des Zugriffs auf Ressourcen und Dienste.
  - Datenschutz: Proxies schützen die Privatsphäre der Benutzer, indem sie deren Identität verschleiern.
  - Performance-Optimierung: Sie verbessern die Leistung von Webanwendungen durch Caching und Datenkompression.

Proxies sind vielseitige Vermittlerinstanzen, die in vielen Aspekten des Systemdesigns eine wichtige Rolle spielen. Sie tragen zur Netzwerksicherheit, Zugriffskontrolle und Performance-Optimierung bei.


---

# Reverse Proxy

- **Definition**
  - Entschiedene Komponente in modernen Webarchitekturen.
  - Operiert auf der Anwendungsschicht (Layer 7) des OSI-Modells.

- **Vorteile**
  - Verbesserte Leistung, Sicherheit und Wartbarkeit für Webanwendungen.
  - Übernahme von Aufgaben wie SSL-Terminierung und Inhaltskomprimierung zur Entlastung der Server und Steigerung der Anwendungsleistung.

- **Sicherheitsschutz**
  - Filterung des eingehenden Datenverkehrs und Abwehr bösartiger Anfragen.
  - Schutzschild für die Sicherheit von Webanwendungen.

- **Serververwaltung und Skalierung**
  - Vereinfacht die Verwaltung und Skalierung von Servern.
  - Verbessert die Wartbarkeit der Anwendung.

- **Beispiele**
  - Plattformen wie GitHub setzen Reverse-Proxys ein, um effiziente und leistungsstarke Webdienste bereitzustellen.

- **Wichtigkeit**
  - Unverzichtbar, um Webanwendungen sicherer, leistungsfähiger und leichter wartbar zu machen.

Reverse-Proxys spielen eine entscheidende Rolle bei der Verbesserung der Leistung und Sicherheit von Webanwendungen sowie bei der Vereinfachung der Serververwaltung und Skalierung.

---

# Load Balancer

- **Funktion**
  - Ermöglicht die Verarbeitung von Millionen von Anfragen durch Webanwendungen.
  - Gewährleistet optimale Ressourcennutzung zur Maximierung des Durchsatzes und zur Minimierung der Antwortzeit.

- **Algorithmen**
  - Verwendet verschiedene Algorithmen zur bestmöglichen Verteilung der Arbeitslast.
  - Trägt zur Effizienz des Ressourceneinsatzes bei.

- **Hohe Verfügbarkeit und Fehlertoleranz**
  - Spielt eine entscheidende Rolle bei der Gewährleistung hoher Verfügbarkeit und Fehlertoleranz.
  - Gleichmäßige Verteilung der Arbeitslast und Umleitung des Datenverkehrs bei Serverausfällen.

- **Reibungsloser Betrieb**
  - Gewährleistet einen reibungslosen Betrieb, auch bei Spitzenlastzeiten oder Serverausfällen.
  - Optimiert die Anwendungsleistung und die Nutzererfahrung.

Load Balancer sind von entscheidender Bedeutung für die Verbesserung der Leistung, Skalierbarkeit und Verfügbarkeit von Webanwendungen.

---

# API Gateway vs Proxy vs Reverse Proxy vs Load Balancer

Aber was ist jetzt der Unterschied zwischen den ganzen? Diese Komponenten weisen einige Gemeinsamkeiten auf, dienen jedoch in modernen Webarchitekturen unterschiedlichen Zwecken.

- **Load Balancer:**
  - Priorisieren die Verbesserung der Leistung, Verfügbarkeit und Fehlertoleranz.
  - Verteilen Anfragen gleichmäßig auf mehrere Backend-Server und arbeiten hauptsächlich auf Netzwerkebene.
  - Die Hauptanforderung liegt in der Lastverteilung.

- **Reverse Proxys:**
  - Operieren auf der Anwendungsebene (Layer 7) und bieten Zusatzfunktionen wie URL-Umschreiben, Inhaltskomprimierung und Zugriffskontrolle.
  - Verbessern die Sicherheit und Wartbarkeit von Anwendungen.
  - Ideal, wenn erweiterte Anwendungsebenenfunktionen benötigt werden.

- **Proxys:**
  - Allgemeine Vermittlerinstanzen zwischen Client und Server.
  - Funktionen variieren je nach Art des Proxys, können Sicherheitsfunktionen wie Zugriffskontrolle und Inhaltsfilterung bieten.
  - Fokus auf Datenverkehrssteuerung und Sicherheit.

- **API-Gateways:**
  - Ideal für Microservices-Architekturen, in denen verschiedene APIs zentrale Verwaltung, Sicherheit und Skalierbarkeit benötigen.
  - Bieten erweiterte Funktionen wie Authentifizierung, Ratenbegrenzung, Anfrage-/Antworttransformation und Überwachung.
  - Unverzichtbar, wenn Ihre Anwendung stark von APIs abhängt und Sie das Management und die Sicherheit Ihrer Schnittstellen optimieren möchten.

---

# Skalierungsmuster

1. Definiton
1. Horizontale Skalierung vs vertikale Skalierung
1. Replikation
1. Partitionierung
1. Sharding
1. Load Balancing
1. Caching


---

# Skalierungsmuster Defintion

**Ein Skalierungsmuster, auch als Skalierungsmuster oder Skalierungstyp bezeichnet, ist ein bewährter Ansatz oder eine bewährte Methode zur Bewältigung von Skalierbarkeitsanforderungen in Software- oder Informationssystemen. Skalierungsmuster bieten Richtlinien und bewährte Praktiken, um die Leistung, Verfügbarkeit und Kapazität einer Anwendung oder eines Systems zu erhöhen, wenn die Anforderungen steigen.**

*Diese Muster helfen bei der Bewältigung von Herausforderungen wie einem zunehmenden Datenverkehr, steigenden Benutzerzahlen oder wachsenden Datenmengen. Beispiele für Skalierungsmuster sind das Load-Balancing, das Caching, die vertikale und horizontale Skalierung, das Sharding und viele andere. Jedes dieser Muster bietet eine spezifische Methode zur Verbesserung der Skalierbarkeit und hilft Entwicklern und Systemarchitekten dabei, geeignete Lösungen für ihre Anwendungen zu entwickeln.*


---

# Horizontale Skalierung vs vertikale Skalierung

## Horizontale Skalierung

- Daten werden auf mehrere Knoten partitioniert.
- Verteilt die Datenlast auf mehrere Server.
- Beispiele: Cassandra, MongoDB.
- Vorteile: Reduzierte Ausfallmöglichkeiten, bessere Leistung durch Hinzufügung weiterer Computer.
- Geeignet für Anwendungen mit nationaler oder internationaler Kundschaft.

## Vertikale Skalierung

- Alle Daten bleiben auf einem einzelnen Knoten.
- Skalierung durch Erweiterung von CPU- und RAM-Ressourcen auf einem Knoten.
- Beispiele: MySQL, Amazon RDS.
- Vorteile: Schnelle und kostengünstige Erweiterung der Infrastruktur.
- Begrenzt durch Kapazität einer einzelnen Maschine.

---

# Welche Skalierung?

Die Entscheidung zwischen horizontaler und vertikaler Skalierung hängt von verschiedenen Faktoren ab:

## Horizontale Skalierung

- Minimiert Ausfallmöglichkeiten.
- Verbessert die Gesamtleistung durch Hinzufügen von Computern.
- Bietet hohe Zuverlässigkeit.
- Geeignet für Anwendungen mit nationaler oder internationaler Kundschaft.

## Vertikale Skalierung

- Sinnvoll bei ausreichenden Ressourcen auf einem einzelnen System.
- Schnelle und kostengünstige Erweiterung der Infrastruktur.
- Begrenzt durch die Kapazität einer einzelnen Maschine.
- Möglicherweise nicht für zukünftige Anforderungen ausreichend.

---

# Replikation: Verbesserung von Datenverfügbarkeit und -leistung

## Was ist Replikation?

- Prozess, bei dem Daten von einer Datenbank auf einen anderen Server kopiert werden.
- Ziel: Verbesserung der Datenverfügbarkeit und -leistung.
- Reduziert Netzwerklatenz und ermöglicht weltweit schnellere Datenzugriffe.
- Löst Probleme in Bezug auf Verfügbarkeit, Fehlertoleranz und Datendurchsatz.

## Replikationsalgorithmen

- Leader-basierte Replikation: Mit synchronen und asynchronen Strategien.
- Wahl des Replikationsansatzes abhängig von spezifischen Anforderungen und Kompromissen.

---

# Partitionierung: Skalierbarkeit und Leistungssteigerung

## Warum Partitionierung?

- Einzelne Maschinen stoßen an ihre Grenzen bei großen Datensätzen und hohem Abfragedurchsatz.
- Partitionierung teilt den Datensatz in kleinere Teilmengen auf.
- Jede Partition wird zu einer eigenen kleinen Datenbank.
- Ziel: Verbesserung der Leistung und Erhöhung der Skalierbarkeit.

---

# Sharding: Skalierbarkeit und Leistungssteigerung

## Was ist Sharding?

- Datenbankoptimierungstechnik zur Aufteilung großer Datenbanktabellen in kleinere Tabellen, genannt Shards oder Partitionen.
- Shards können identische Schemata mit eindeutigen Zeilen (horizontal Sharding) oder Teilschemata der Originaltabelle haben (vertikales Sharding).
- Ziel: Verbesserung der horizontalen Skalierbarkeit und Leistungsfähigkeit.

## Horizontales Sharding

- Geeignet für Abfragen, die oft in Gruppen zusammengefasste Teilzeilen zurückgeben, z.B. Datumsfilter.

## Vertikales Sharding

- Nützlich, wenn Abfragen nur eine Teilmenge der Datenspalten zurückgeben.
- Ermöglicht die Aufteilung von Daten auf separate Server.

## Vorteile von Sharding

- Höhere Verfügbarkeit und reduzierte Auswirkungen von Ausfällen auf betroffene Datenblöcke.
- Backup-Shards können auf zusätzlichen Knoten repliziert werden.

## Unterschied zu Partitionierung

- Sharding verteilt Daten auf mehrere Computer.
- Partitionierung gruppiert Teilmengen von Daten innerhalb einer einzelnen Datenbankinstanz.
- Die Begriffe werden manchmal synonym verwendet, insbesondere bei "horizontal" oder "vertikal" gekennzeichnet.

---

# Load Balancing: Optimierung von Leistung und Verfügbarkeit

## Was ist Load Balancing?

- Technik zur Optimierung der Leistung und Verfügbarkeit von Webservern und IT-Ressourcen.
- Verteilt eingehenden Online-Traffic gleichmäßig auf mehrere Server oder Ressourcen.
- Reduziert Serverauslastung, erhöht Zugriffsgeschwindigkeit und sichert Verfügbarkeit.

## Load Balancer

- Analysiert Benutzeranfragen und leitet sie an am besten geeignete Server weiter.
- Verwendet Algorithmen wie Round Robin, Weighted Round Robin, Least Connections und Weighted Least Connections.

## Bedeutung von Load Balancing

- Stabilität und Hochverfügbarkeit von Online-Diensten.
- Besonders wichtig in Umgebungen mit starkem Online-Traffic und E-Commerce-Branche.

---

# Load Balancing Algorithmen

## Statisches Load Balancing

- Folgt festen Regeln und ist unabhängig vom aktuellen Serverstatus.
- Beispiele für statische Algorithmen:
  - Round-Robin-Methode: Server werden nacheinander ausgewählt.
  - Gewichtete Round-Robin-Methode: Server erhalten unterschiedliche Gewichtungen.
  - IP-Hash-Methode: Die IP-Adresse des Clients wird in eine Nummer umgewandelt und Server zugewiesen.

## Dynamisches Load Balancing

- Untersucht den aktuellen Status der Server, bevor der Datenverkehr verteilt wird.
- Beispiele für dynamische Algorithmen:
  - Least Connection Method: Server mit den wenigsten aktiven Verbindungen werden ausgewählt.
  - Weighted Least Connection Method: Server mit geringer Kapazitätsauslastung werden bevorzugt.
  - Least Response Time Method: Die Antwortzeit und aktive Verbindungen werden kombiniert, um den besten Server auszuwählen.
  - Resource-Based Method: Der Load Balancer berücksichtigt die aktuelle Serverlast basierend auf Ressourcennutzung.

---

# Caching: Steigerung der Leistung und Effizienz

## Was ist Caching?

- Verfahren zur Steigerung der Leistung und Effizienz von Datenabrufen in Computersystemen.
- Daten werden vorübergehend in einem schnelleren Speicher (Cache) gespeichert.
- Reduziert die Notwendigkeit, auf langsamere Speicherschichten zuzugreifen.

## Cache-Hierarchie

- Caches sind hierarchisch organisiert (z. B. L1, L2, L3) und dienen dem sequenziellen Datenabruf.
- Cache-Zugriffe können "Cache-Treffer" oder "Cache-Fehler" sein.

## Caching-Strategien

- Verschiedene Strategien wie Durchschreibcache, Write-Around-Cache und Write-Back-Cache mit Vor- und Nachteilen.
- Räumungsrichtlinien wie FIFO, LIFO, LRU und andere steuern, welche Daten im Cache bleiben.

## Anwendungsfälle

- Caching in Anwendungsfällen wie Datenbank-Caching, Content Delivery Network (CDN), Domain Name System (DNS)-Caching und API-Caching.
- Nicht sinnvoll, wenn Cache-Zugriff genauso lange dauert wie Zugriff auf primären Speicher oder Daten häufig ändern.

## Vorteile von Caching

- Verbesserte Leistung, geringere Latenz, Entlastung der Datenbank, niedrigere Netzwerkkosten und höherer Lesedurchsatz.

---

# Cache-Arten: Local, Distributed, Hierarchical

## Lokaler Cache

- Clientseitiger Cache.
- Speichert eine Teilmenge der Daten des Master-Space.
- Basierend auf der letzten Aktivität der Client-Anwendung.
- Versucht, Abfragen aus dem Cache zu erfüllen.
- Führt sie im Master-Space aus und speichert Ergebnisse lokal.

## Verteilter Cache

- Kombiniert den Arbeitsspeicher (RAM) mehrerer vernetzter Computer.
- Bildet einen gemeinsamen In-Memory-Datenspeicher.
- Bietet schnellen Datenzugriff.
- Skalierbare Lösung in Umgebungen mit hohem Datenvolumen und hoher Datenlast.

## Hierarchischer Cache

- Cache-Ebenen, die miteinander kommunizieren.
- Erkennt übergeordnete (parent) und untergeordnete (child) Caches.
- Übergeordneter Cache höher in der Hierarchie.
- Untergeordneter Cache, für den der Traffic Server selbst als übergeordneter Cache fungiert.
- Effiziente Organisation von Caches in verschiedenen Ebenen.

---

# Skalierungswürfel

Der Skalierungswürfel ist ein dreidimensionales Modell zur Skalierung von Anwendungen, wie im Buch "The Art of Scalability" beschrieben. Er bietet drei Hauptansätze zur Skalierung:

## X-Achsen-Skalierung

- Verteilung der Last auf mehrere Instanzen.
- Erhöht die Anzahl der Instanzen, um die Gesamtlast zu bewältigen.
- Gleichmäßige Verteilung des Datenverkehrs.

## Y-Achsen-Skalierung

- Aufteilung der Anwendung in Dienste oder Microservices.
- Transformation einer monolithischen Anwendung in skalierbare, unabhängige Dienste.
- Bessere Beherrschung von Komplexität und Skalierbarkeit.

## Z-Achsen-Skalierung

- Teilt Daten auf identische Instanzen auf.
- Leitet Anfragen basierend auf Anfrageattributen weiter.
- Verbessert die Datenaufteilung und Ressourcennutzung.

Der Skalierungswürfel bietet verschiedene Ansätze zur Bewältigung der Skalierbarkeitsanforderungen von Anwendungen.

---

# Quellen

- [Quelle 1](Link zur Quelle 1)
- [Quelle 2](Link zur Quelle 2)
