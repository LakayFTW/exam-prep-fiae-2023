# Table of Content
- [Verwendung des ITSM's](#verwendung-des-itsms)
- [Bedeutung eines Prozesses](#bedeutung-eines-prozesses)
- [Umterscheidung von Prozessketten](#unterscheidung-von-prozessketten)
- [Bedeutung von IT Services](#bedeutung-von-it-services)
- [Unterscheidung von Services](#unterscheidung-von-services)
  - [Statusmeldung](#statusmeldung)
  - [Kundenanfrage](#kundenanfrage)
  - [Störungsfall](#störungsfall)
- [Einsatz von ITSM Frameworks](#einsatz-von-itsm-frameworks)
  - [ITIL](#itil)
  - [ISO 20000](#iso-20000)
  - [COBIT](#cobit)
  - [FitSM](#fitsm)
  - [DevOps](#devops)
  - [SAFe](#safe)
- [IT Service Managementarten](#it-service-managementarten)
- [Service Lebenszyklus nach ITILv4](#service-lebenszyklus-nach-itilv4)
  - [Strategy](#strategy)
  - [Design](#design)
  - [Transition](#transition)
  - [Operation](#operation)
  - [Improvement](#improvement)
- [Service Lebenszyklus nach IMAC/R/D](#service-lebenszyklus-imacrd)
  - [Install](#install)
  - [Move](#move)
  - [Change](#change)
  - [Add](#add)
  - [Remove](#remove)
  - [Dispose](#dispose)
- [Incident Management](#incident-management)

&nbsp;

[^1]
# Verwendung des ITSM's

Das IT-Servicemanagement, oft auch ITSM genannt, beschreibt die Art und Weise, wie IT-Teams bei der gesamten Bereitstellung von IT-Services für ihre Kunden und Mitarbeiter vorgehen. Dazu gehören alle Prozesse und Aktivitäten rund um die Planung, Zusammenstellung, Lieferung und den Support von IT-Services.
Die Bereitstellung und Kontrolle von Services unterliegt nicht nur der IT Branche und kann auch bei anderen Branchen erfolgen in Form des allgemeinen Service Managements.

&nbsp;

[^2]
[^3]
# Bedeutung eines Prozesses
Ein Prozess ist eine geregelter Ablauf von folgenden Aktivitäten.
Es besitzt immer ein definiertes Ende und auch einen definierten Startpunkt. Es folgte nach dem EVA Prinzip, dass durch das Einbringen gewünschter Anforderungen eine Folge an geregelten Schritten eintritt, um einen erhofftes Ergebnis zu erhalten.

<a href="https://qualitaetsmanagement.me/prozessmanagement/prozess/">
  <img src="https://qualitaetsmanagement.me/wp-content/uploads/2022/11/071122_Der-Prozess-einfach-erklaert_Logo.jpg" width="500" title="Einfacher Prozessablauf" />
</a>

&nbsp;

[^4]
Ein Prozess muss und kann auch nicht das gewünschte Endresult erbringen.
Somit können sich mehrere zusammengehängte Prozesse ergeben, welche das letzte Ergebnis eines Prozesses als Eingabe für das nächste weiterbringt bis zum Ende.
Eine Reihung an Prozessen wird Prozesskette bezeichnet.

&nbsp;

<a href="https://qualitaetsmanagement.me/prozessmanagement/prozess/">
  <img src="https://prozessoptimierung-sprung.de/wp-content/uploads/2019/10/Prozesslandkarte-mit-Prozesskette-Supportprozess.jpg" width="500" title="Einfache Prozesskette">
</a>

&nbsp;

Der Verlauf von mehreren Prozessen und deren Bedingungen, welche Wege eingeschlagen werden können, lassen sich in einer Ereignisgesteuerten Prozesskettenmodell(EPK Modell) darstellen.

<a href="http://de.processorientation.com/?p=668">
  <img src="https://imgs.search.brave.com/cWfLjTeeyPGmUGqsetbAOSxnWbtjExyPyiHlccT1uLw/rs:fit:766:1024:1/g:ce/aHR0cDovL2RlLnBy/b2Nlc3NvcmllbnRh/dGlvbi5jb20vd3At/Y29udGVudC91cGxv/YWRzLzIwMTIvMDEv/RVBLX0JlaXNwaWVs/LTc2NngxMDI0LnBu/Zw" width="400" title="Einfache Ereignisprozesskette">
</a>

&nbsp;

# Unterscheidung von Prozessketten

&nbsp;

__Die Prozessketten werden in folgende Arten unterteilt:__
- Wertschöpfungsprozesse
- Supportprozesse
- Managementprozesse

&nbsp;

## Wertschöpfungsprozesse
Wertschöpfungsprozesse sind Prozesse, die direkt an der Erstellung eines verkaufbaren Produktes oder Dienstleistung mitwirken.

&nbsp;

## Supportprozesse
Supportprozesse sind notwendig, um die Wertschöpfungs- und Managementprozesse durchführen zu können.

&nbsp;

## Managementprozesse
Managementprozesse dienen der Planung, Diagnose und Steuerung von Wertschöpfungs- oder Supportprozessen. Das sind meist nicht so viele Prozesse. Und sie laufen typischerweise auf der obersten Managementebene ab. Sie beziehen sich auf das Gesamtunternehmen.

&nbsp;

[^5]
# Bedeutung von IT Services

Ein IT Service bezieht sich auf die Dienstleistung, die mit der Anwendung von technischem und betriebswirtschaftlichem Fachwissen entwickelt wurden, um die Nutzung der Technologie für Unternehmen und Endbenutzer zu erleichtern.

Die IT Services können im eigenen Unternehmen, als auch von Drittanbietern in Anspruch genommen werden.

&nbsp;

# Unterscheidung von Services
__Services können in folgende Kategorien unterschieden werden:__
- Statusmeldung
- Kundenanfrage
- Störungsfall

&nbsp;

## Statusmeldung
Diese Statusmeldungen werden hier aus als Events bezeichnet.
Diese werden nicht von einem Anwender verfasst, sondern über ein integriertes Überwachungssystem, auch als __Monitoring__ bezeichnet, automatisch bei Vorfällen erstellt.

&nbsp;

__Die Meldungen unterteilen sich in weitere folgende Kategorien:__
- Information: Meldung ohne Handlungsbedarf
> Beispiel: Netzwerkauslastung von 45%.
- Warnung / Warning: Meldung mit Notwendigkeit näherer Beobachtung.
> Beispiel: RAID Datenverbund meldet eine Restkapazität von 20%.
- Ausnahme / Exception: Meldung mit sofortigen Handlungsbedarf
> Beispiel: Netzwerkport 48 ist ausgefallen am Switch.

&nbsp;

## Kundenanfrage
Eine formale Anfrage eines Kundens für die Verbesserung oder die Erzeugung eines neuen Services.
Wenn Informationen oder Zugriff angefragt wird handelt es sich um einen Service Request und ist im Service-Katalog meistens hinterlegt. Diese werden über die bestehenden Prozesse durchgeführt.

&nbsp;

Wenn Anforderungen gestellt werden zur Aufrüstung der aktuellen Hard- und Software als Beispiel, handelt es sich um einen Request for Change, wo professionell der Aufwand betrieben und koordiniert werden muss.
Hier werden Änderungen ausgelöst, welche bestehdende Prozesse umstruktuerieren und diese verständlich den anderen zur Verfügung gestellt werden muss.

&nbsp;

## Störungsfall
Eine Meldung von einer nicht geplanten Unterbrechung eines Services.
Dies wird auch als Incident bezeichnet.
Im Bereich der IT können Störungen im Netzwerk, an Computersystemen oder an einer Software vorliegen, welches den laufenden Betrieb entweder verlangsamt oder sogar komplett pausieren kann. Hier soll der laufende Betrieb damit sichergestellt werden. 


&nbsp;

[^6] 
# Einsatz von ITSM Frameworks
Damit eine Organisation in allen Abteilung effizient miteinander arbeiten kann, wie auch mit dem Kunden selbst, muss eine gute Struktur gegeben sein an die sich die Organisation halten kann für den Einsatz derer Services.
Hierzu existieren einige Frameworks, wo jedes seine eigene Bandbreite an Möglichkeiten bietet sowie einen eigenen Ansatz, die alle dazu beitragen können, die speziellen Anforderungen einer Organisation zu erfüllen

__Beliebte Frameworks darunter sind:__
- ITIL
- ISO 20000
- COBIT
- FitSM
- DevOps
- SAFe

&nbsp;

## ITIL
Das ITIL Framework zielt darauf ab, die Lieferung an IT-Prozessen zu verbessern, um mehrere geschäftliche Ziele zu unterstützen.

&nbsp;

## ISO 20000
Bedient sich an den Prinzipien vom ITIL Framework, hat aber keine öffentliche Beziehung zu dessen.

&nbsp;

## COBIT
Das COBIT IT Governance Framework legt ihren Fokus auf kontinuierlicher IT-Sicherheit und ist das Gegenteil von ITIL.

&nbsp;

## FitSM
FitSM ist ein Standard für Leichtgewicht-Servicemanagement und zusätzlich das Service-Portfolio-Management.

&nbsp;

## DevOps
DevOps nutzt die Methodologie kreuzfunktionaler Teams, die von offener Kommunikation angeregt werden. Das DevOps Framework vereint einen nicht zusammenhängenden Satz an Prinzipien, die je nach den geschäftlichen Anforderungen des Unternehmens verbunden werden.

&nbsp;

## SAFe
Das Scaled Agile Framework wendet die Agile-Struktur, die von Softwareentwicklungsteams verwendet wird, an, indem Agile auf größere Applikationen skaliert wird.

&nbsp;

# IT Service Managementarten

Beim Anbieten und Verfolgen der Services im Unternehmen gibt es verschiedene spezielle Bereiche wie diese koordiniert werden. Einige von diesen Arten sind:
- Incident Mangement: Behebungen von eintretenden Zwischenfällen bei laufenden Services
- Service-Level Management: Bereitstellung und Kontrolle von SLA's
- Problem Management: Behebungen von schwerwiegenden Zwischenfällen bei laufenden Services
- Change Management: Vorbereitung und Umsetzung von Ändernungen an Arbeitsprozessen im Unternehmen

&nbsp;

# Service Lebenszyklus nach ITILv4

<a href="https://de.education-wiki.com/9403688-itil-service-lifecycle">
  <img src="https://cdn.education-wiki.com/img/project-management-basics/9403688/itil-service-lifecycle-2.png.webp" width="300" title="Phasenaufbau nach ITILv4">
</a>

&nbsp;

[^7]
Das ITSM besteht nach dem ITIL Lebenszyklus aus fünf festgelegten Phasen:
- Strategy
- Design
- Transition
- Operation
- Improvement


&nbsp;
## Strategy:
- DevOps Einsatz
- Business Relationship Management

&nbsp;

## Design:
- Service Level Managemnt
- Service Capacity Management
- Service Availability Management
- Service Continuity Management
- Service Catalog Management
- Information Security Management
- Requirements Engineering
- Data Management

&nbsp;

## Transition:
- Release- / Configuration Management
- Knowledge Management
- Change Management

&nbsp;

## Operation:
- Incident Management
- Request Fullfillment
- Problem Management
- Access Management

&nbsp;

## Improvement:
- PDCA, KVP (Kontinuierlicher Verbesserungsprozess)
- DevOps Einsatz

&nbsp;

[^8]
# Service Lebenszyklus nach IMAC/R/D
International verbreitet veranschaulichen Unternehem die Durchführung iheres Service Lebenszyklus nach der IMAC/R/D Darstellung.
Hier können Kunden ihre Probleme und oder Anfragen direkt in einer der Phasen einordnen wenn sie den Kontakt mit dem Unternehmen aufnehmen.
Die Darstellung wird allgemein für alle Services verwendet und bietet Kunden eine bessere Findung in das bestehdende Unternehmenssystem durch die konkrete Unterscheidung aller Services.

&nbsp;

<a href="https://www.i-doit.com/blog/imac-r-d-serviceorientiertes-it-lifecycle-management/">
  <img src="https://www.i-doit.com/hs-fs/hubfs/imac-r-d-1600x900-1.jpg?width=550&height=309&name=imac-r-d-1600x900-1.jpg" title="IMAC/R/D Lifecycle" width="500">
</a>

&nbsp;

## Install
Installation und Konfiguration eines Systems oder Gegenstands.
>Beispiel: Einrichten eines IT Arbeitsplatzes mit funktionierenden Rechner, passender Peripherie, Monitoren, Netzwerkanschluss und den Office Softwareprodukten.

&nbsp;

## Move
Bereitstellung, Verpackung, Neukonfiguration existierender Geräte mit folgendem Transport zur neuen Umgebung.
>Beispiel: Umzug eines Entwicklungsteams samt benötigten Geräten von der Grundetage in die erste Etage.

&nbsp;

## Add
Hinzufügen und Konfiguration zusätzlicher Komponenten.
>Beispiel: Einabu einer externen Grafikeinheit in einem Rechner mit abhängigen Grafiktreibern.  

&nbsp;

## Change
Aktualisierung oder Wechsel von existierenden Komponenten.
>Beispiel: Umtausch einer Festplatte mit allen gespeicherten Daten auf eine größerer mit mehr Speicherkapazität.

&nbsp;

## Remove
Vorbereitung und Sichern von zu entfernenden Komponenten in einem eingesetzten System.
>Beispiel: Abbau eines Arbeitsplatzes mit allen Geräten.

&nbsp;

## Dispose
Entsorgung oder Neuaufbereitung von ungebrauchten oder defekten Geräten.
>Beispiel: Sachgerechte Entsorgung einer defekten Netzwerkkarte.

&nbsp;

[^9]
# Incident Management
Das Kernstück des Incident Managements ist die Behebung von jeglichen Zwischenfällen, welche auf unterschiedlichster Weise den Ablauf der Unternehmensprozesse negativ beeinflussen kann.

<a href="https://advisera.com/20000academy/knowledgebase/itil-incident-management-separate-roles-different-support-levels/">
  <img src="https://imgs.search.brave.com/2OIwiEv6-3r--ZBh5UE3uFIUlgPMcGRYAW1dzkGeJ9w/rs:fit:600:401:1/g:ce/aHR0cHM6Ly9hZHZp/c2VyYS5jb20vd3At/Y29udGVudC91cGxv/YWRzL3NpdGVzLzYv/MjAxNS8wNy9JVElM/X3JvbGVfc2VwYXJh/dGlvbi5wbmc" width="500" title="Incident Management">
</A>

&nbsp;

Wenn ein Vorfall vorliegt wird die Umgebung als erstes mit einem Track-System kategorisiert, ob es im Bereich Software, Hardware oder Netzwerk vorliegt. Danach erfolgt die Priorisierung des Vorfalls nach Dringlichkeit und Auswirkung. Dies geschieht beim Helpdesk oder allgemein dem Single Point of Contact (auch SPOC genannt) und leistet hier für die meldende Person den First-Level-Support.

Hier wird in der Known-Error-Database nach einem ähnlichen Sachzusammenhang geguckt und eine Lösung hierzu angeboten. Wenn diese Lösung die Behebung der Störung erzielt hat wird somit der Prozess erfolgreich beendet und protokolliert.

Wenn das Problem mangels an Fachwissen und hinterlegten Einträgen nicht zur Zufriedenheit soweit behoben wird, werden die Anforderungen der definierten SLA's nicht erfüllt und der Incident wird eskaliert.

Der Vorfall wird nun zu einem Problem und es erfolgt eine speziellere Behandlung von Fachpersonen mit mehr Kenntnissen in Second-Level-Support.
Nicht jeder Incident wird automatisch zu einem Problem, da es von der Priorisierung und dem Umfeld abhängig ist,
Wenn hier auch nach den verfassten SLA's keine Zufriedenheit geschaffen werden kann, dann erfolgt eine letzere Eskalation zum Third-Level-Support bei Fachkräften, die bei jdem Detailaspekt Einfluss besitzen das System auf jede Art und Weise zu verändern.

Wenn eine Lösung gefunden wurde im aktuellen Level wird jeweils dem vorherigen ein Bericht erstattet bis nichts mehr weitergetragen werden kann.
Alle Schritte werden auf dem Weg protokolliert und in der Know-Error-Database hintergelgt bei ähnlichen und gleichen Vorfällen.


[^1]: https://www.atlassian.com/de/itsm
[^2]: https://www.itsmprocesses.com/Wiki/Deutsch/ITIL%20Prozesse.htm
[^3]: https://qualitaetsmanagement.me/prozessmanagement/prozess/
[^4]: https://prozessoptimierung-sprung.de/
[^5]: https://www.hagel-it.de/it-service/was-sind-it-services.htmlwas-sind-prozessketten-welche-prozessarten-gibt-es/
[^6]: https://www.freshworks.com/de/freshservice/itsm/itsm-framework/
[^7]: https://de.education-wiki.com/9403688-itil-service-lifecycle
[^8]: https://www.i-doit.com/blog/imac-r-d-serviceorientiertes-it-lifecycle-management/
[^9]: https://advisera.com/20000academy/knowledgebase/itil-incident-management-separate-roles-different-support-levels/