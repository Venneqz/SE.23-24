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

[1]


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

[2] https://testsigma.com/blog/how-to-write-a-good-bug-report-some-tips/#How_to_Write_a_Bug_Report


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
[3]

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
[4] 

## Debugging vs. Testen
Testen und Debugging sind zwei unerlässliche Prozesse in der Softwareentwicklung, die jeweils unterschiedliche Ziele und Zeitpunkte haben. Beim Testen geht es darum, sicherzustellen, dass eine Software den festgelegten Anforderungen entspricht und etwaige Fehler aufzudecken. Dieser Prozess kann von Entwicklern, Testern und Endbenutzern durchgeführt werden und beginnt nach Abschluss der Softwareentwicklung.

Auf der anderen Seite ist Debugging ein reaktiver Prozess, bei dem Entwickler vorhandenen Code durchsuchen, um Fehler zu finden und zu beheben. Es startet, sobald Fehler während des Testvorgangs erkannt werden und ist in der Regel Aufgabe der Entwickler. Die Werkzeuge unterscheiden sich ebenfalls: Testen nutzt Testautomatisierungs- und Testmanagement-Tools, während Debugging Debugger, Profiler und andere Debugging-Tools einsetzt.

Insgesamt sind Testen und Debugging unterschiedliche Ansätze in der Softwarequalitätskontrolle. Während Testen darauf abzielt, Qualitätsmängel zu verhindern, konzentriert sich Debugging auf die Identifizierung und Behebung von Fehlern in existierendem Code. Beide Prozesse sind entscheidend, um qualitativ hochwertige Softwareprodukte bereitzustellen und das Vertrauen der Benutzer zu gewinnen.

[5] 

## Rubber Duck Debugging
Der Ansatz des "Rubber Duck Debugging" ist eine humorvolle und dennoch effektive Methode zum Lösen von Programmierproblemen. Diese Methode beinhaltet die Verwendung einer Badeente als imaginären Gesprächspartner, um Code-Fehler zu finden und zu beheben. Der Prozess sieht folgendermaßen aus:

Holen Sie sich eine Badeente (Badewannenversion), sei es durch Leihen, Kaufen oder andere Mittel.

Stellen Sie die Gummiente auf Ihren Schreibtisch und erklären Sie ihr, dass Sie beabsichtigen, Ihren Code mit ihrer Hilfe zu durchgehen.

Beginnen Sie damit, der Ente zu erklären, was Ihr Code tun soll. Gehen Sie anschließend detailliert vor und erläutern Sie Ihren Code Zeile für Zeile.

Während des Erklärungsprozesses werden Sie oft feststellen, dass Sie sich vertun oder herausfinden, dass das, was Sie tatsächlich tun, nicht dem entspricht, was Sie zuvor beabsichtigt hatten. Die Ente sitzt still da, zufrieden mit dem Wissen, dass sie Ihnen geholfen hat, den Fehler zu identifizieren.

Hinweis: Wenn nötig, kann ein Kollege die Ente ersetzen, aber oft ist es effektiver, die Ente um Hilfe zu bitten, bevor Sie Kollegen involvieren.

Die Methode des "Rubber Duck Debugging" mag auf den ersten Blick amüsant erscheinen, hat sich jedoch als nützliche Möglichkeit erwiesen, um festgefahrene Gedanken zu klären und Codierfehler zu finden. Das Erklären des Codes laut hilft Entwicklern, die zugrunde liegenden Probleme zu erkennen und Lösungen zu finden, selbst wenn der Gesprächspartner nur aus Kunststoff ist.

[6]

## Time-travel debugging (reverse debugging)
Zeitreise-Debugging, auch als Reverse Debugging bekannt, ermöglicht Entwicklern, die gesamten Aktivitäten eines laufenden Programms aufzuzeichnen und dann rückwärts und vorwärts durch die Aufzeichnung zu navigieren, um den Programmstatus zu überprüfen. Im Vergleich zu herkömmlichen Debuggern, die nur Vorwärts-Debugging unterstützen, eignet sich Zeitreise-Debugging besonders für schwer reproduzierbare Fehler und große Anwendungen.

Mit herkömmlichen Debuggern kann ein Entwickler Schritt für Schritt durch den Code gehen, was bei einfachen Fehlern effektiv sein kann. Bei schwer reproduzierbaren Fehlern, bei denen der Fehlerort unbekannt ist, ist dies jedoch schwierig. Zeitreise-Debugger ermöglichen es, die Ausführung rückwärts zu verfolgen, um die Ursache des Fehlers an verschiedenen Stellen des Programms zu finden.

Das Zeitreise-Debugging erfordert eine Aufzeichnung der Programmausführung, einschließlich Fehler und der Abfolge von Ereignissen, die dazu geführt haben. Dies kann die Leistung beeinträchtigen, wobei die Verlangsamung je nach verwendetem Zeitreise-Debugger variiert.

Die Anwendung von Zeitreise-Debugging ist prinzipiell in allen Programmiersprachen möglich, wobei die Unterstützung in GDB-kompatiblen Sprachen wie C/C++, Go und Fortran am häufigsten ist. Es gibt auch spezielle Zeitreise-Debugging-Tools für andere Sprachen wie Python und JavaScript.

Insgesamt ermöglicht Zeitreise-Debugging Entwicklern, effektiv schwerwiegende Fehler zu beheben, indem sie die Ausführung des Programms rückwärts verfolgen können, um die Wurzel des Problems zu finden. Dies ist besonders nützlich bei komplexen und schwer zu reproduzierenden Fehlern.
[7]

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
[8]

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
[3]
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
[3]

## Debugging Werkzeuge
Trace32 von Lauterbach: Trace32 bietet Hardware- und Software-Tools. Es basiert auf einem modularen Konzept, das universelle Basismodule und architekturspezifische Kabel kombiniert. Entwickler können den "PowerDebug PRO" verwenden, der USB-3.0- und GbE-Anschlüsse bietet und für das Debuggen von verschiedenen Architekturen geeignet ist. Dieses Tool ermöglicht eine umfassende Analyse des Programmablaufs.

ULINKplus von Arm Keil: ULINKplus ist ein Debugger, Leistungsmessgerät und I/O-Schnittstelle in einem Gerät. Es bietet Einblicke in die Funktion, das Timing und die Leistungsaufnahme von Embedded-Anwendungen. Entwickler können es an Arm-Cortex-basierte Geräte anschließen und Funktionen wie SWV-Trace und Multi-Core-Debugging nutzen.

J-Link von Segger: J-Link ist ein Hardware-Debugger, der bis zu 3 Mbyte/s RAM-Download-Geschwindigkeit bietet und eine unbegrenzte Anzahl von Breakpoints im Flash-Speicher von MCUs unterstützt. Es kann mit verschiedenen CPUs und Architekturen verwendet werden und bietet Software-Tools wie Embedded Studio, System View und Ozone.

Universal Debug Engine (UDE) von PLS Programmierbare Logik & Systeme: Die UDE ist ein Software-Tool für die Systemanalyse, Tests und Debugging von High-End-SoCs und eingebetteten Multicore-Systemen. Es ermöglicht das Darstellen von Systemzuständen, das Setzen von Breakpoints und die Laufzeitanalyse. Die UDE unterstützt verschiedene Architekturen und bietet Funktionen wie Trace, Profiling und Code-Coverage-Analyse.

Diese Debugging-Werkzeuge helfen Entwicklern, Softwarefehler zu identifizieren, zu isolieren und zu beheben, um sicherzustellen, dass ihre Software fehlerfrei und leistungsstark ist. Sie bieten eine breite Palette von Funktionen, die von Hardware-Debugging bis hin zu Software-Simulation reichen, je nach den Anforderungen des Entwicklungsprojekts.
[9]

# Agile testing workflows 
Agiles Testen ist eine Testpraxis, die den Regeln und Prinzipien der agilen Softwareentwicklung folgt. Im Gegensatz zur Wasserfallmethode kann Agile Testing bereits zu Beginn des Projekts mit einer kontinuierlichen Integration zwischen Entwicklung und Test beginnen. Die agile Testmethode ist nicht sequentiell (in dem Sinne, dass sie erst nach der Codierungsphase ausgeführt wird), sondern kontinuierlich.

Die Prinzipien des agilen Testens betonen die Zusammenarbeit, kontinuierliche Verbesserung und die Integration von Entwicklung und Test. Der agile Testlebenszyklus umfasst Phasen wie Anforderungsschätzung, Testplanung, Release-Vorbereitung und Übergang. Agile Tests erfolgen in verschiedenen Quadranten, die interne Codequalität, Geschäftsorientierung, Feedback und nicht-funktionale Anforderungen abdecken. Es gibt auch Herausforderungen im agilen Testen, einschließlich hoher Fehlerwahrscheinlichkeit und der Notwendigkeit einer effektiven Testautomatisierung. Insgesamt dient Agile Testing dazu, die Qualität und Anpassungsfähigkeit von Softwareprodukten in agilen Umgebungen sicherzustellen.

[10]
## TDD, BDD, ATDD
Testgetriebene Entwicklung (TDD) ist eine Methode, bei der Entwickler automatisierte Testfälle vor der Codierung schreiben und den Code so anpassen, dass die Tests erfolgreich durchlaufen werden. BDD (Behavioral-Driven Development) ist eine Erweiterung von TDD, die den Schwerpunkt auf das Verhalten eines Systems legt und Testfälle in natürlicher Sprache mit "Given-When-Then" formuliert. ATDD (Acceptance Test-Driven Development) ähnelt BDD, konzentriert sich jedoch mehr auf das Erfassen genauer Anforderungen und verbessert die Zusammenarbeit zwischen Entwicklern, Kunden und Qualitätssicherungskräften.

Die Unterschiede zwischen TDD, BDD und ATDD liegen in den beteiligten Personen, der verwendeten Sprache, dem Hauptaugenmerk und den verwendeten Tools. TDD ist stark auf Entwickler ausgerichtet, verwendet die Programmiersprache des Systems und konzentriert sich auf Unit-Tests. BDD bezieht Kunden und QA-Teams ein, verwendet eine einfache natürliche Sprache und betont das Verhalten des Systems. ATDD ist ähnlich wie BDD, legt jedoch mehr Wert auf die Erfassung genauer Anforderungen und die Verwendung von Abnahmetests. Je nach Projekt und Anforderungen kann eine dieser Methoden oder eine Kombination am effizientesten sein.

[11] https://www.browserstack.com/guide/tdd-vs-bdd-vs-atdd

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
[3]

## Test doubles
Testdoubles sind in agilen Test-Workflows, wie TDD, von entscheidender Bedeutung. Sie werden verwendet, um das Verhalten echter Abhängigkeiten zu simulieren und dienen dazu, die zu testende Codeeinheit von anderen Teilen des Systems zu isolieren. Dies ermöglicht schnellere und zuverlässigere Tests und fördert besseres Design, Feedback und Kommunikation. Testdoubles machen den Einsatz externer Ressourcen, wie Datenbanken oder Webdienste, überflüssig und helfen bei der klaren Definition von Anforderungen.

Der Prozess der Verwendung von Testdoubles in TDD beginnt mit dem Schreiben eines fehlgeschlagenen Tests, in dem das gewünschte Verhalten beschrieben wird. Testdoubles ersetzen alle nicht relevanten oder nicht verfügbaren Abhängigkeiten. Dann wird die minimale Menge an Code geschrieben, damit der Test besteht, und die Testdoubles dienen als Leitfaden für die Interaktionen zwischen dem Code und seinen Abhängigkeiten.

Die Verwendung von Testdoubles sollte in TDD in folgenden Situationen in Betracht gezogen werden:

Wenn Sie eine Codeeinheit isoliert von ihren Abhängigkeiten testen möchten.
Um verschiedene Szenarien oder Grenzfälle zu testen, die mit echten Abhängigkeiten schwer oder gar nicht zu reproduzieren sind.
Um den Testprozess zu beschleunigen oder zu vereinfachen und Zeit und Ressourcen zu sparen.
Die Auswahl des richtigen Testdoubles hängt von Faktoren wie Komplexität, Kontrolle, Abstraktion und Realismus ab. Tools und Frameworks wie Mockito, JUnit, Sinon, Jest und RSpec stehen zur Verfügung, um Testdoubles zu erstellen. Die Wahl des richtigen Testdoubles hängt von den Anforderungen ab und soll eine verbesserte Codierung ermöglichen.

Zusammenfassend unterstützen Testdoubles agile Test-Workflows, indem sie die Isolation von Codeeinheiten erleichtern und bessere Tests, Design-Praktiken und Kommunikation fördern.
[12] https://www.linkedin.com/advice/3/how-do-you-use-test-doubles-mocks-stubs

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
[13]

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
[3]

# Pair programming
Pair Programming oder Programmieren in Paaren ist eine zentrale Technik aus dem Extreme Programming (XP). Beim Pair Programming sitzen zwei Entwickler gleichberechtigt an einem Rechner und arbeiten gemeinsam an einer Aufgabe. Die zwei Entwickler:innen nehmen unterschiedliche Rollen ein, welche oft mit „Pilot“ und „Navigator“ bezeichnet werden.

Der „Pilot“ schreibt den Code, während der „Navigator“ die Korrektheit des Codes und des Lösungsansatzes überwacht und parallel über Verbesserungen am Design nachdenkt. Weil beide Entwickler:innen gleichberechtigt sind, gibt es keine feste Aufgabenteilung. Deshalb wechselt der „Pilot“ alle paar Minuten zum „Navigator“ und der „Navigator“ wird zum „Piloten“. Auch zwischen den Paaren werden die Partner:innen kontinuierlich gewechselt. So wird sichergestellt, dass jedes Teammitglied alle Teile des Projektes kennenlernt. ist das die Definition von Pair programming

[14]

## Ablauf
Der Ablauf beim Pair Programming ist in der Regel recht einfach:

Es gibt zwei Schlüsselrollen: den Driver oder Piloten und den Navigator oder Beobachter. Der Driver ist derjenige, der aktiv am Computer arbeitet und den Code schreibt. Währenddessen erklärt der Driver, was er tut, so dass der Navigator seine Gedanken und Absichten verstehen kann. Der Navigator hingegen beobachtet aufmerksam die Codierung und bietet Feedback zur Implementierung. Gleichzeitig denkt der Navigator darüber nach, wie die Aufgabe möglicherweise optimiert werden kann. Die Idee hinter dieser Rollenteilung besteht darin, zwei verschiedene Perspektiven auf den Code zu haben: Der Driver konzentriert sich auf die unmittelbaren Details und Codezeilen, während der Navigator eine übergeordnete, strategische Sichtweise einnimmt und das Gesamtbild im Auge behält.

Die Rollen zwischen den beiden Entwicklern wechseln regelmäßig ab, wobei jeder abwechselnd die Rolle des Drivers und des Navigators übernimmt.

Die Paarprogrammierer arbeiten idealerweise eng zusammen und fördern eine ständige Kommunikation. Sie klären Unklarheiten oder Fragen bezüglich des Vorgehens, der Programmierung und der Tests so schnell wie möglich.

Es ist nicht ungewöhnlich, dass einer der beiden Entwickler nach einer bestimmten Zeit (z. B. alle paar Tage oder eine Woche) das Paar verlässt und einem anderen Kollegen Platz macht. Dies wird als Paar-Rotation oder Pair Rotation bezeichnet. In einigen Publikationen wird die Person, die im Team bleibt, als "Anker" bezeichnet. Die Absicht dahinter, sofern sie nicht auf Urlaub oder Krankheit zurückzuführen ist, besteht darin, frische Perspektiven und neue Energie ins Team zu bringen und die Bildung von Wissenssilos zu vermeiden. Natürlich sollte jede Organisation individuell entscheiden, ob und wann ein Wechsel sinnvoll ist.

In der Praxis kann die Art und Weise, wie die Entwickler zusammenarbeiten, variieren. Manche teilen sich einen Computer, während andere jeweils ihren eigenen Computer verwenden und auf einem gemeinsamen Code-Stand arbeiten. Die Verwendung von gängigen Versionsverwaltungstools ermöglicht es, selbst mit getrennten Rechnern problemlos zusammenzuarbeiten.
[15]

## Best practices
Best Practices für Pair Programming:

1. Gemeinsam planen: Bevor Sie mit dem Programmieren beginnen, klären Sie Ihre Ziele und Aufgaben, die Dauer der Sitzung und Rollenwechsel. Nehmen Sie sich Zeit, sich über persönliche Vorlieben auszutauschen.

1. Regelmäßiger Rollenwechsel: Wechseln Sie regelmäßig zwischen den Rollen des Piloten und des Navigators, idealerweise alle 30 Minuten. Dies ermöglicht verschiedene Perspektiven und fördert die Zusammenarbeit.

1. Gutes Audio- und Video-Setup: Achten Sie auf eine klare Audio- und Videokommunikation, insbesondere bei Remote-Pair Programming. Verwenden Sie Headsets und schalten Sie die Videokamera ein, um die Kommunikation zu verbessern.

1. Vermeiden Sie Mikromanagement: Vermeiden Sie es, den Partner zu kontrollieren oder zu diktieren. Schaffen Sie eine sichere Umgebung für die Zusammenarbeit und fördern Sie den Wissensaustausch.

1. Seien Sie nett und geduldig: Seien Sie geduldig und respektvoll, insbesondere bei unterschiedlichen Qualifikationsniveaus. Vermeiden Sie es, den Partner zu überwachen oder zu unterbrechen.

1. Vermeiden Sie äußere Ablenkungen: Ignorieren Sie E-Mails und andere Ablenkungen während der Pair-Programming-Sitzung. Planen Sie Pausen und Aktivitäten außerhalb des Programmierens.

1. Ständige Kommunikation: Halten Sie die Kommunikation während der Sitzung aufrecht, um sicherzustellen, dass beide Partner aktiv teilnehmen und zusammenarbeiten.
[16]


# Code reviews
Eine Codeüberprüfung ist eine Peer-Review von Code, die Entwicklern dabei hilft, die Codequalität sicherzustellen oder zu verbessern, bevor sie ihn zusammenführen und versenden.
[17] 
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
[18]
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
[3]

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
[19]

# Refactoring
Refactoring ist eine disziplinierte Technik zur Umstrukturierung eines vorhandenen Codekörpers, bei der seine interne Struktur geändert wird, ohne sein äußeres Verhalten zu ändern.

Sein Herzstück ist eine Reihe kleiner verhaltenserhaltender Transformationen. Jede Transformation (als „Refactoring“ bezeichnet) bewirkt wenig, aber eine Abfolge dieser Transformationen kann zu einer erheblichen Umstrukturierung führen. Da jedes Refactoring klein ist, ist es weniger wahrscheinlich, dass es schiefgeht. Das System bleibt nach jedem Refactoring voll funktionsfähig, wodurch die Wahrscheinlichkeit verringert wird, dass ein System während der Umstrukturierung ernsthaft beschädigt wird.

[20] 


## Ziele des Refactorings
Refactoring verbessert die Lesbarkeit des Codes und macht ihn einfacher zu verstehen und zu warten. Es hilft, die Codequalität zu verbessern, indem es die Komplexität reduziert, die Wartbarkeit erhöht und die Leistung verbessert. Es hilft auch, die Codebasis zu vereinfachen und die technische Schulden zu reduzieren. Refactoring ist ein wichtiger Bestandteil der agilen Softwareentwicklung und wird häufig in Kombination mit Test-Driven Development (TDD) eingesetzt.

[3]
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
[21]


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
[22]
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
[23]
es gibt noch viele weiter Patterns und Methoden wie:
Rename Variable: Die Umbenennung von Variablen in klar verständliche Namen ist entscheidend, um die Lesbarkeit des Codes zu verbessern.

Move Method: Das Verschieben von Methoden in die richtige Klasse kann dazu beitragen, die Struktur des Codes zu verbessern und Abhängigkeiten zu verwalten.

Replace Conditional with Polymorphism: Wenn Sie viele bedingte Anweisungen haben, kann die Umstellung auf polymorphe Strukturen die Wartbarkeit und Lesbarkeit des Codes erheblich verbessern.

Encapsulate Field: Das Einhüllen von Feldern in Methoden, um den Zugriff auf Felder zu steuern und die Flexibilität zu erhöhen.

Introduce Parameter Object: Wenn eine Methode viele Parameter hat, kann das Gruppieren dieser Parameter in einem Objekt die Signatur der Methode vereinfachen.

Encapsulate Collection: Das Einhüllen von Sammlungen in eigene Klassen zur besseren Steuerung und Abstraktion der Daten.

Remove Duplicate Code: Die Entfernung von Duplikaten im Code, um die Wartbarkeit zu erhöhen und Fehler zu reduzieren.

Das sind die in meist genutzten Refactoring Patterns, es gibt noch viele weitere.
[3]

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
[24]

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
[25]
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
[3]

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
[3]


# Quellen

1. [Turing - Start Reading Code the Right Way](https://www.turing.com/kb/start-reading-code-the-right-way)
   - **Autor:** Nicht angegeben
   - **Veröffentlichungsdatum:** Nicht angegeben
   - **Abrufdatum:** 19. Oktober 2023

2. [Testsigma - How to Write a Good Bug Report](https://testsigma.com/blog/how-to-write-a-good-bug-report-some-tips/#How_to_Write_a_Bug_Report)
   - **Autor:** Atif Beg
   - **Veröffentlichungsdatum:** May 23, 2023
   - **Abrufdatum:** 19. Oktober 2023

3. [Chat GPT](https://chat.openai.com/)
   - **Autor:** Nicht angegeben
   - **Veröffentlichungsdatum:** Nicht anwendbar
   - **Abrufdatum:** 19. Oktober 2023

4. [LinkedIn - Root Cause Analysis You Must Know](https://www.linkedin.com/pulse/all-rcaroot-cause-analysis-you-must-know-dhirendra-patel)
   - **Autor:** Dhirendra Patel
   - **Veröffentlichungsdatum:** 30. Dez. 2022
   - **Abrufdatum:** 19. Oktober 2023

5. [Testsigma - Difference Between Testing and Debugging](https://testsigma.com/blog/difference-between-testing-and-debugging/#Difference_Between_Testing_and_Debugging)
   - **Autor:** Kiruthika Devaraj
   - **Veröffentlichungsdatum:** July 15, 2023
   - **Abrufdatum:** 19. Oktober 2023

6. [Rubber Duck Debugging](https://rubberduckdebugging.com/)
   - **Autor:** Nicht angegeben
   - **Veröffentlichungsdatum:** Nicht angegeben
   - **Abrufdatum:** 19. Oktober 2023

7. [Undo - 6 Things About Time-Travel Debugging](https://undo.io/resources/6-things-time-travel-debugging#:~:text=Time%20travel%20debugging%20(aka%20reverse,to%20inspect%20the%20program%20state.)
   - **Autor:** Nicht angegeben
   - **Veröffentlichungsdatum:** Nicht angegeben
   - **Abrufdatum:** 19. Oktober 2023

8. [Coralogix - Tracing vs. Logging: What to Know](https://coralogix.com/blog/tracing-vs-logging-what-to-know/)
   - **Autor:** Tobias Schlichtmeier
   - **Veröffentlichungsdatum:** 14. Mai 2021
   - **Abrufdatum:** 19. Oktober 2023

9. [Elektroniknet - Vier Tools im Check](https://www.elektroniknet.de/embedded/entwicklungstools/vier-tools-im-check.186375.html)
   - **Autor:** Nicht angegeben
   - **Veröffentlichungsdatum:** Nicht angegeben
   - **Abrufdatum:** 19. Oktober 2023

10. [Guru99 - Agile Testing: A Beginner's Guide](https://www.guru99.com/agile-testing-a-beginner-s-guide.html)
    - **Autor:** Thomas Hamilton
    - **Veröffentlichungsdatum:** October 7, 2023
    - **Abrufdatum:** 19. Oktober 2023

11. [BrowserStack - TDD vs. BDD vs. ATDD](https://www.browserstack.com/guide/tdd-vs-bdd-vs-atdd)
    - **Autor:** Jash Unadkat
    - **Veröffentlichungsdatum:** June 15, 2023
    - **Abrufdatum:** 19. Oktober 2023

12. [LinkedIn - How Do You Use Test Doubles, Mocks, Stubs?](https://www.linkedin.com/advice/3/how-do-you-use-test-doubles-mocks-stubs)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

13. [Jesus Valera Reales - Testing With Test Doubles](https://jesusvalerareales.com/testing-with-test-doubles/#:~:text=The%20five%20types%20of%20Test,how%20it%20will%20be%20used.)
    - **Autor:** Jesus Valera Reales
    - **Veröffentlichungsdatum:** June 11, 2020
    - **Abrufdatum:** 19. Oktober 2023

14. [it-agile - Was ist Pair Programming?](https://www.it-agile.de/agiles-wissen/agile-entwicklung/was-ist-pair-programming/)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

15. [T2Informatik - Pair Programming](https://t2informatik.de/wissen-kompakt/pair-programming/)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

16. [Duckly - 7 Tips for Successful Pair Programming](https://duckly.com/blog/7-tips-for-successful-pair-programming/)
    - **Autor:** Jfromtheblock
    - **Veröffentlichungsdatum:** 17 SEPTEMBER 2021
    - **Abrufdatum:** 19. Oktober 2023

17. [GitLab - What Is Code Review?](https://about.gitlab.com/topics/version-control/what-is-code-review/)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

18. [dev.to - Enhancing Code Reviews With Conventional Comments](https://dev.to/tsotsi1/enhancing-code-reviews-with-conventional-comments-2j9i)
    - **Autor:** TSOTSI1
    - **Veröffentlichungsdatum:** 12. Juni .2023
    - **Abrufdatum:** 19. Oktober 2023

19. [Swarmia - A Complete Guide to Code Reviews](https://www.swarmia.com/blog/a-complete-guide-to-code-reviews/?utm_term=code%20review%20best%20practices&utm_campaign=SRH-REVIEW-EU-EN&utm_source=adwords&utm_medium=ppc&hsa_acc=6644081770&hsa_cam=16463390785&hsa_grp=134848023275&hsa_ad=585675515692&hsa_src=g&hsa_tgt=kwd-298072696942&hsa_kw=code%20review%20best%20practices&hsa_mt=p&hsa_net=adwords&hsa_ver=3&gclid=CjwKCAjwp8OpBhAFEiwAG7NaEhy7Gvy4r35tivXyYYrIs0-WQrkUQggqz3NcB2demdyWZ-7DKr0g3RoCY8sQAvD_BwE#best-practices-for-code-reviews
    - **Autor:** Kimmo Brunfeldt
    - **Veröffentlichungsdatum:** Oct 12, 2021
    - **Abrufdatum:** 19. Oktober 2023

20. [Refactoring - refactoring.com](https://refactoring.com/)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

21. [Refactoring Guru - Extract Method](https://refactoring.guru/extract-method)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

22. [Refactoring Guru - Extract Variable](https://refactoring.guru/extract-variable)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

23. [Refactoring Guru - Inline Method](https://refactoring.guru/inline-method)
    - **Autor:** Nicht angegeben
    - **Veröffentlichungsdatum:** Nicht angegeben
    - **Abrufdatum:** 19. Oktober 2023

24. [BrowserStack - Best Test Automation Frameworks](https://www.browserstack.com/guide/best-test-automation-frameworks)
    - **Autor:** GH and Akshay Badkar
    - **Veröffentlichungsdatum:** August 27, 2023
    - **Abrufdatum:** 19. Oktober 2023

25. [BrowserStack - Build Tools](https://www.browserstack.com/guide/build-tools)
    - **Autor:** Somosree Roy
    - **Veröffentlichungsdatum:** July 27, 2023
    - **Abrufdatum:** 19. Oktober 2023

