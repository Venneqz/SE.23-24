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

# API Gateway vs Proxy vs Reverse Proxy vs Load Balancer

1. API Gateway vs Proxy vs Reverse Proxy vs Load Balancer
1. Skalierungsmuster

---


# Quellen

- [Quelle 1](Link zur Quelle 1)
- [Quelle 2](Link zur Quelle 2)
