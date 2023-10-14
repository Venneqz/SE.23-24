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

  ### Anforderungen neuer Anwendungen:

    Grafische Benutzerschnittstellen: Moderne Anwendungen profitieren von grafischen Benutzerschnittstellen, und verteilte Systeme bieten die Leistung und Ressourcen, um diese effizient bereitzustellen.

    Kurze Antwortzeiten: Verteilte Systeme sind in der Lage, Lastspitzen zu bewältigen und können auf verschiedene Ressourcen zugreifen, um kurze Antwortzeiten für Benutzer zu gewährleisten.

  ### Weite Verbreitung mächtiger PCs und Workstations:

    Die Verwendung leistungsstarker PCs und Workstations als Teil verteilter Systeme ermöglicht die effiziente Ausführung anspruchsvoller Anwendungen und die Bereitstellung von Rechenleistung und Speicherressourcen.
    Fortgeschrittene Netztechnologien (LAN, WAN, MAN, wireless):

    Fortgeschrittene Netzwerkinfrastrukturen erlauben die Kommunikation und Koordination zwischen den Komponenten verteilter Systeme, unabhängig von der geografischen Entfernung. Dies trägt zur Skalierbarkeit und Flexibilität des Systems bei.
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


## Quellen

[1]: Dijkstra, E. W. (1968). Go to statement considered harmful. 
Communications of the ACM, 11(3), 147-148.
