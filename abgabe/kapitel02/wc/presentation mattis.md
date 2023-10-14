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
---

1. Visualisierung von Systemarchitekturen
1. Systemarchitekturmuster
1. Modulare Architekturen

---

## Client-Server-Modell

- **Grundkonzept:** Trennung von Frontend (Client) und Backend (Server).
  
- **Beispiele:** 
    - In der Webentwicklung, wo der Browser auf dem Client-Ende arbeitet und der Server die Daten bereitstellt.
    - Kommunikation zwischen zwei Rechnern, bei der der Client Anfragen stellt und der Server Antworten liefert.

- **Anwendungen:** 
    - Von einfachen Google-Suchanfragen bis hin zu komplexen Unternehmensdatenbanksystemen.
---

## Anwendungsbeispiele

- **E-Mail-Client:**
  - Schreiben, Senden, Empfangen von E-Mails.
  - Beispiele: Outlook, Thunderbird, Apple Mail.

- **FTP-Client:**
  - Datei-Upload/-Download via FTP-Server.

- **SSH-Client:**
  - Sichere SSH-Verbindungen.
  - Beispiel: PuTTY (Windows).

- **Webbrowser:**
  - Anfragen an Webserver (HTTP).
  - Bekannte: Chrome, Firefox.

- **DNS-Client:**
  - Löst Computernamen in IP-Adressen auf.
  - Hintergrund-Client im TCP/IP-Protokoll.
---

## PWA vs SPA vs MPA
---
### Progressive Web App (PWA):
- Merkmale:
  - Ressourceneffizient und schnell.
  - Bietet Offline-Funktionalität und Push-Benachrichtigungen.
  - Kann auf dem Startbildschirm eines Geräts installiert werden.
- Verwendungsszenarien:
  - Gut geeignet für breite Anwendungsbereiche, insbesondere auf Mobilgeräten.
  - Erhöht die Reichweite von Webanwendungen und verbessert die Benutzerbindung.
---
### Single Page Application (SPA):
- Merkmale:
  - Laden in einem einzigen HTML-Dokument, dynamische Inhaltsänderung ohne Seitenneuladung.
  - Verwendet JavaScript-Frameworks wie Angular, React oder Vue.js.
  - Schnelle Benutzererfahrung durch bedarfsgesteuertes Nachladen von Daten.
- Verwendungsszenarien:
  - Ideal für interaktive Anwendungen, bei denen Seitenwechsel ohne Neuladen erforderlich ist, z.B. soziale Medien und E-Commerce.
---
### Multi-Page Application (MPA):
- Merkmale:
  - Besteht aus mehreren HTML-Seiten, jede mit eigener Ansicht.
  - Navigation durch Klicken auf Links, separate Seitenladung vom Server.
- Verwendungsszenarien:
  - Geeignet für traditionelle Websites und Anwendungen mit klar getrennten Inhalten und Funktionen, z.B. Unternehmenswebsites und Blogs.

---
## Peer-to-Peer (P2P)

**Definition (Cambridge Dictionary):** Ein Computernetzwerk, bei dem jeder Computer als Server für andere fungieren kann, wodurch Dateien und Ressourcen gemeinsam genutzt werden können.[3]

| **Vorteile**                                    | **Nachteile**                                       |
|-----------------------------------------------|----------------------------------------------------|
| - Schneller Aufbau                           | - Aufwändige Verwaltung je größer das Netzwerk     |
| - Kein zentraler Server                      | - Komplexe Dateisuche im Netzwerk                  |
| - Skalierbar, ausfallsicher                  | - Heterogene Leistung und Bandbreite im Netzwerk  |
| - Dezentrale Kommunikation, schützt vor Zensur|                                                    |
| - Potenziell sicherer als Client-Server       |                                                    |
---
## Anwendungsbeispiele

- **Datenaustausch:** 
  - Bekannte Filesharing-Netzwerke: Dropbox, Google Drive.

- **Direktnachrichten und Videotelefonie:** 
  - P2P Voice- und Videokommunikation: Skype, Microsoft Teams.

- **Kollaboration:** 
  - Teamarbeit mit Groupware: z.B. Adobe Connect.

- **Blockchain:** 
  - P2P-Transaktionen in Kryptowährungen über Blockchains.

---
## Event-Typen

**1. Domain Event:**
- Historische Datensätze im Domain-Driven Design (DDD).
- Erfassen Absicht und Kontext bedeutsamer Zeitpunkte.
- Benannt in menschenverständlicher Sprache (z.B., "OrderWasShipped").
- Geeignet für Lese-Modelle und event-sourced Systeme.

**2. Trigger oder Signal Event:**
- Kleinste Art von Ereignissen, enthält ID und Zeitstempel.
- Verwendet, um Reaktionen auszulösen oder Geschäftsprozesse zu benachrichtigen.
- Hilfreich bei Datenschutzanforderungen (DSGVO).

**3. RESTful oder "Fat" Event:**
- Enthält die vollständige Ressourcenrepräsentation aus einer RESTful-API.
- Ideal für Integration und externe Verbraucher.
- Verhindert Umwege zur API und reduziert Aufwand für Verbraucher.

---
## Message Broker

- **Definition:** Software, die Kommunikation und Informationsaustausch zwischen Anwendungen, Systemen und Diensten ermöglicht.
- **Funktionen:** Übersetzt Nachrichten zwischen verschiedenen Nachrichtenprotokollen, validiert, speichert, routet und leitet sie an die richtigen Empfänger weiter.
- **Vorteile:** Entkoppelt Prozesse und Dienste, ermöglicht Kommunikation zwischen unterschiedlichen Plattformen und Programmiersprachen.

---
## ESB vs. Message Queue

| **Enterprise Service Bus (ESB)** | **Message Queue**               |
|-----------------------------------|---------------------------------|
| Zentrale SOA-Komponente           | Asynchrone Kommunikation         |
| Integrationsschnittstelle         | Entkoppelt Produzenten und Konsumenten |
| Nachrichtenübersetzung und Weiterleitung | Einsatz von Nachrichtenbrokern (z.B. RabbitMQ) |
| Komplex und umfangreich            | Fokussiert auf Nachrichtenverwaltung |
---
## Anwendungsbeispiele

- **E-Commerce:**
  - Bestellverarbeitung, Inventaraktualisierung, Benachrichtigungen.

- **IoT (Internet of Things):**
  - Überwachung und Steuerung vernetzter Geräte und Sensoren.

- **Finanzdienstleistungen:**
  - Handel, Überweisungen, Betrugserkennung.

- **Logistik und Lieferkettenmanagement:**
  - Sendungsverfolgung, Routenoptimierung.

- **Gesundheitswesen:**
  - Patientenüberwachung, klinische Alarme.

- **Social Media:**
  - Benachrichtigungen, Feeds, Aktivitätsströme.

---
## Serviceorientierte Architektur (SOA)

- **Definition:** Methode der Softwareentwicklung, bei der Services (Softwarekomponenten) für Geschäftsanwendungen genutzt werden.
- **Merkmale:** Services erfüllen spezifische Geschäftsfunktionen, sind plattform- und sprachübergreifend, ermöglichen Wiederverwendung und Kombination für komplexe Aufgaben.

**Anwendungsbeispiel:**
- Benutzerauthentifizierung: Ein Authentifizierungsservice wird erstellt und von allen Anwendungen wiederverwendet.
---
## Service Discovery

- **Definition:** Prozess zur Lokalisierung von Webdienstanbietern und Abruf von Dienstbeschreibungen durch Diensteregister.
- **Zweck:** Entkoppelt Dienstnutzer von Bereitstellungstopologien, ermöglicht effiziente und flexible Kommunikation in SOA, ohne umfangreiche manuelle Konfiguration.
---
## Microservices

- **Definition:** Softwareentwicklungsansatz mit kleinen, unabhängigen Services, die über klare APIs kommunizieren.
- **Organisation:** Services werden von kleinen, eigenständigen Teams entwickelt.

**Vorteile:**
- Vereinfachte Skalierbarkeit und verkürzte Entwicklungszeit.
- Ermöglicht Innovation und beschleunigt die Markteinführung neuer Funktionen.

---
## Monolith vs. Distributed Monolith vs. Microservice

| **Architektur**           | **Eigenschaften**                                         |
|---------------------------|-----------------------------------------------------------|
| Monolithische Architektur | - Eng verknüpfte Anwendung                                |
|                           | - Gesamte Anwendung muss bei Skalierung angepasst werden |
|                           | - Erschwert Experimente und erhöht das Ausfallrisiko    |
| Distributed Monolith      | - Ähnlich wie Monolith, aber auf verschiedene Server verteilt |
| Microservices-Architektur | - Unabhängige, eigenständige Komponenten mit klaren Schnittstellen |
|                           | - Jeder Service erfüllt spezifische Funktion, unabhängige Aktualisierung und Skalierung |
|                           | - Verbesserte Flexibilität und Verfügbarkeit der Anwendung |
---
## Choreography Pattern vs. Orchestration Pattern

- **Choreografie:**
  - Services interagieren direkt, ohne zentrale Kontrolle.
  - Ereignisbasierte Kommunikation.
  - Vorteile: lose Kopplung, dezentrale Kontrolle.
  - Nachteile: komplexe Wartung, geringe Transparenz.

- **Orchestrierung:**
  - Zentraler Orchestrator steuert die Services.
  - Befehlsbasierte Kommunikation.
  - Vorteile: einfache Kontrolle, gute Sichtbarkeit, einfache Fehlerbehebung.
  - Nachteile: engere Kopplung, Single Point of Failure.

- **Wann Choreografie nutzen:**
  - Bei unabhängigen Services, lose gekoppelt, Flexibilität benötigt.

- **Wann Orchestrierung nutzen:**
  - Abhängige Services, spezifische Reihenfolge, gute Überwachung.

- **Mischung:**
  - Beide Ansätze können kombiniert werden, um Flexibilität und Kontrolle zu bieten, je nach den Anforderungen der Architektur.

---
## Service Mesh

Ein **Service Mesh** ist eine anpassbare Infrastrukturebene für Microservices-Anwendungen. Es gewährleistet die zuverlässige Übermittlung von Anfragen innerhalb der komplexen Dienststruktur einer cloudbasierten Anwendung. Das Service Mesh ermöglicht flexible, zuverlässige und schnelle Kommunikation zwischen den einzelnen Diensten. Es bietet Funktionen wie Diensterkennung, Lastenausgleich, Verschlüsselung, Authentifizierung, Autorisierung und mehr.[16]

---

# Systemdesign

1. Systemdesign Definition
1. API Gateway vs Proxy vs Reverse Proxy vs Load Balancer
1. Skalierungsmuster


---

# Systemdesign Definition

**Beim Systemdesign werden die Elemente eines Systems wie Architektur, Module und Komponenten, die verschiedenen Schnittstellen dieser Komponenten und die Daten, die das System durchlaufen, definiert. Es soll die spezifischen Bedürfnisse und Anforderungen eines Unternehmens oder einer Organisation durch die Entwicklung eines kohärenten und gut funktionierenden Systems erfüllen.**


---

# API Gateway vs Proxy vs Reverse Proxy vs Load Balancer

1. API Gateway vs Proxy vs Reverse Proxy vs Load Balancer
1. Skalierungsmuster

---


# Quellen

- [Quelle 1](Link zur Quelle 1)
- [Quelle 2](Link zur Quelle 2)
