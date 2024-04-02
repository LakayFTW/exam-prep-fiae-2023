# Table of Content
- [Table of Content](#table-of-content)
- [Cloud-Computing](#cloud-computing)
  - [Wesentliche Eigenschaften (NIST - National Institute of Standards and Technology)](#wesentliche-eigenschaften-nist---national-institute-of-standards-and-technology)
- [Schichten](#schichten)
  - [IaaS - Infrastructure as a Service](#iaas---infrastructure-as-a-service)
    - [Vorteile](#vorteile)
    - [Beispiele](#beispiele)
  - [PaaS - Platform as a Service](#paas---platform-as-a-service)
    - [Vorteile](#vorteile-1)
    - [Beispiele](#beispiele-1)
  - [SaaS - Software as a Service](#saas---software-as-a-service)
    - [Organisationsformen der Cloud](#organisationsformen-der-cloud)
      - [Private Cloud](#private-cloud)
      - [Public Cloud](#public-cloud)
        - [Exclusive Cloud](#exclusive-cloud)
        - [Open Cloud](#open-cloud)
      - [Hybrid Cloud](#hybrid-cloud)
    - [Vorteile](#vorteile-2)
    - [Nachteile](#nachteile)
- [SaaS - Software as a Service -- Allgemein](#saas---software-as-a-service----allgemein)
  - [Vergleich Lizentmodelle](#vergleich-lizentmodelle)
    - [Tranditionellse Software-Lizenzmodell](#tranditionellse-software-lizenzmodell)
    - [SaaS](#saas)
    - [Zusammenfassung](#zusammenfassung)
  - [Ziel](#ziel)
  - [Preismodelle](#preismodelle)
  - [Vorteile für den Servicenehmer](#vorteile-für-den-servicenehmer)
  - [Nachteile für den Servicenehmer](#nachteile-für-den-servicenehmer)
  - [Vorteile für den Servicegeber](#vorteile-für-den-servicegeber)
  - [Nachteile für Servicegeber](#nachteile-für-servicegeber)
  - [Datenschutz](#datenschutz)
  - [Saas-Unternehmen](#saas-unternehmen)

# Cloud-Computing
Cloud Computing ist die Datenverarbeitung in einer "Wolke".
Es beschreibt die Bereitstellung der IT-Infrastuktur und IT-Leistungen als Service über das Internet, dabei werden die Cloud Dienste bedarfsgerecht und dynamisch abgerufen, die Berechnung erfolgt über ein nutzungsabhängiges Abrechnungsmodell. Angebot und Nutzung erfolgen ausschließlich über technische Schnittstellen und Protokolle. Es umfasst das ganze Spektrum der Informationstechnik und beinhaltet u.a. Infrastuktur, Plattformen und Software. Es entbindet den Nutzer von der kostenintensiven Bereitstellung, Installation und Betreuung eigener Rechensysteme.

## Wesentliche Eigenschaften (NIST - National Institute of Standards and Technology)
- On-Demand Self Service
  - Automatische Selbstbedienbarkeit für die Nutzer ohne zutun des Anbieters.
- Broad Network Access
  - Zugang von Desktops, Laptops und Mobilfunk über das Breitband, ohne Anbindung an einen bestimmten Client
- Resource Pooling
  - Zusammenlegung von Ressourcen für mehrere Benutzer
- Rapid Elasticity
  - Flexible Ressourcen, die im Bedarfsfall schnell umdisponiert werden können.
- Measured Services
  - Mess- und Überwachbare Services
  - Können den  Nutzer bei Bedarf zur Verfügung gestellt werden.

# Schichten 
- Infrastruktur
- Plattform
- Anwendung

## IaaS - Infrastructure as a Service
Das IaaS bildet die unterste Schicht im Cloud-Computing, es wird auch die Cloud-Foundation genannt. Hier werden IT-Leistungen wie Rechenleistung, Speicherplatz und Netzwerke angeboten, es umfasst quasi die Basisinfrastruktur. Nutzer gestalten sich frei ihre eigenen virtuellen PC-Cluster, sie sind aber für die Auwahl, Installation, Betrieb und Funktionen der Software selbst verantwortlich.

### Vorteile
- Skalierbarkeit, d.H. die Cloud Dienste können je nach Nutzungsgrad und Bedarf dynamisch angepasst werden.
- Beispiel -> Speicherplatz kann jederzeit erweitert oder verkleinert werden.

### Beispiele
- GoGrid
- Linode

## PaaS - Platform as a Service
PaaS liegt eine Schicht über der Infrastruktur, hier werden IT-Leistungen angeboten mit denen sich Anwendungssoftware und Kommponenten entwickeln und integrieren lassen. Dabei stellt der Cloud Service eine Programmschnittstelle bzw. einen Zugang zu einer Softwareumgebung zur Verfügung. Darin kann der Entwickler Anwendungssoftware erstellen und über Cloud Dienste anbieten. Der Kunde hat aber keine Zugriffe auf die darunterliegenden Schichten (BS, Hardware)

### Vorteile
- Keinen Administrationsaufwand
- Automatische Skalierung
- Verbrauchsgenaue Abrechnung

### Beispiele
- Windows Azure von MS
- App Engine von Google
- force.com von Salesforce.com

## SaaS - Software as a Service
SaaS stellt die oberste Schicht dar.

### Organisationsformen der Cloud

#### Private Cloud
Hier werden die Cloud Dienste aus einem unternehmenseigenen Rechenzentrum  bereitgestellt. Anbieter und Nutzer kennen sich und befinden sich meist auch im selben Unternehmen, außerdem wird die Cloud im Unternehmen selbst kontrolliert und betrieben. Die Dienste sind nur für eine beschränkte Anzahl an Personen, wie Mitarbeiter und autorisierte Geschäftspartner zugänglich, dabei erfolgt der Zugriff innerhalb meist über Intranet und von außen über VPN. Probleme aus dem Bereich der Datensicherheit sind dabei fast hinfällig.

#### Public Cloud
Hier werden Cloud Dienste aus einem öffentlich zugänglichen System bereitgestellt, sie werden von einem externen Dienstleister betrieben, da sie öffentlich sind, können sie von beliebigen Personen und Unternehmen über das Internet genutzt werden. Dabei ist das ganze nicht mehr auf interne Anwendungen eines einzelnen Unernehmens beschränkt. Allerdings muss sich der Nutzer selbst überlegen, wie viele und welche Daten er außerhalb seiner unmittelbaren Kontrolle halten möchte, denn wegen dem öffentlichen Zugriff kommt es häufiger zu Problemen mit der Datensicherheit.

Es wird hierbei zwischen Zwei Formen unterschieden:

##### Exclusive Cloud
- Setzt voraus, dass Anbieter und Nutzer sich kennen.
- Es werden feste Konditionen ausgehandelt und ein Vertrag darüber geschlossen.
- Es gibt keine Unbekannten Parteien
  
##### Open Cloud
- Anbieter und Nutzter kennen sich vorher nicht.
- Der Anbieter muss sein Angebot ohne direkten Input von Kunden entwickeln und in Form von SLAs festlegen.
- Wegen der Vielzahl an potentiellen Nutzern muss der gesamte Geschäftsabschluss und die Nutzung von Instanzen anbieterseitig vollautomatisch ablaufen.
- Beispiel -> Amazon Web Serivces

#### Hybrid Cloud
Darunter versteht man, dass ein Unternehmen eine eigene Private Cloud betreibt und zusätzlich als Falloverstrategie oder für Belastungsspitzen eine Public Cloud verwendet.

### Vorteile 
- Geringe Kosten, da nur die Nutzung und nicht die Hardware/Software gezahlt werden muss
- Skalierbarkeit
- Zukunftssicherheit
- Verfügbarkeit
- Ortsunabhängigkeit
- Einfachkeit

### Nachteile
- Zwingender Nutzzugang, da die Daten nur Online verfügbar sind.
- Sicherheit der Daten
- Zuverlässigkeit
- Abhängigkeit vom Anbieter
- Unzureichende Bandbreite
- Kontrollverlust über die eignen Daten

# SaaS - Software as a Service -- Allgemein
- Teilbereich des Cloud-Computings.
- Bedeutet das Software als Dienstleistung angeboten und an Kunden "vermietet" wird.
- Hierbei wird die Software (und IT-Infrastruktur) bei einem externen IT-Dienstleister betrieben und vom Kunden als Service genutzt.
- Dazu braucht der Kunde nur einen Internet fähigen PC.
- Der Zugriff wird meist über einen Webbrowser realisiert.
- Bei diesen Applikationen handelt es sich um Collaborations- oder Branchensoftware, die ein Unternehmen für den Betrieb seines Geschäftes oder temporärer Projekte benötigt.

## Vergleich Lizentmodelle
### Tranditionellse Software-Lizenzmodell
- Hier erhält der Kunde mit Kauf der Software die Lizenz und das Recht zur Nutzung.
- Dazu wird ein Installationspaket vom Anbieter bereitgestellt.
- Die Installation benötigt eine komplette IT-Infrastruktur (Hardware, BS, Datenbank etc.)
- Nach der Installation wird die Software entsprechend den Geschäftsanforderungen konfiguriert.
- Mit Abschluss der Softwareeinführung übernimmt das Unternehmen den kompletten Betrieb der IT-Infrastruktur und die IT-Aufgaben, wie Administration, Wartung etc.
- Unkalkulierbare Folgekosten fallen meist durch einen Wartungsvertrag an, der mit dem Lizenzkauf verbunden ist.
- Dies beinhaltet die Installation neuer Releases und die Behebung von Fehlern in der Software.

### SaaS
- Hier stellt ein Servicegeber die betriebswirtschaftliche oder redaktionelle Software in einem Rechenzentrum bereit.
- Er betreibt diese und leistet technische Unterstützung
- Dabei übernimmt er alle notwendingen Komponenten eines Rechenzentrums (Netzwerke, Speicher, Datenbanken, Anwendungssserver, Webserver, Disaster-Recovery und Backup-Services).
- Außerdem werden weitere operative Dienstleistungen wie Authentifizierung, Verfügbarkeit, Identitätsmanagement, Fertigungssteuerung, Patchverwaltung, Aktivitätsüberwachung, Softwareupgrades und Anpassungen durchgeführt..
- Der Servicenehmer hingegen braucht nur einen internetfähigen PC und muss keine eigene Software installieren.
- Der Zugriff erfolgt über den Webbrowser.
- Für diese Nutzung und Betrieb zahlt der Servicenehmer eine nutzerabhängige Gebühr.

### Zusammenfassung
- Hier kann man sagen, dass die IT-Infrastruktur und die IT-Aufgaben nicht mehr durch den Servicenehmer, sondern durch den Servicegeber betrieben werden.
- Der Softwarenehmer zahlt keine Softwarelizenz, sondern eine monatliche nutzerabhängige Gebühr.

## Ziel
- Einsparung der Investitionskosten für die IT-Infrastruktur (Hardware, Speicher etc) und die IT-Aufgaben (Softwarewartung, Updates etc.)

## Preismodelle
- Pro Nutzer und pro Monat (pro Benutzer/Monat)
  - Zahlung einer monatlichen, gleichbleibenden Gebühr für jeden angemeldeten Benutzer der mit der Software arbeitet.
  - Ist unabhängig von der Anzahl der Transaktionen und der Zeit, quasi wie eine Art Flatrate.
- Abhängiges vom Funktionsumfang
  - Erweiterung des ersten Modells
  - Auch hier wird eine monatliche gleichbleibende Gebühr gezahlt.
  - Diese ist aber abhängig vom genutzen Funktionsumfang.
  - Beispiel -> Gibt es SRM, CRM, PM etc. und der Servicenehmer möchte nur das CRM nutzen, so braucht er auch nur dafür eine monatliche gleichbleibende Gebühr pro Nutzer zahlen.
- Abhängigkeit von derAnzahl der Transaktionen
  - Abrechnung pro getätigter Transaktion
  - Beispiel -> Der Servicegeber eine E-Commerce-Plattform, bei der der Servicenehmer Produkte verkaufen kann. Bei jeder generierten Bestellung im Shop bezahlt der Servicenehmer einen prozentuellen Anteil vom Verkaufspreis
- Freemium
  - Hier stellt der Servicegeber eine kostenlose Basis-Version zur Verfügung
  - Diese wird dann durch konstenpflichtige Services ergänzt.
- Sonstige
  - Abrechnung durch Datenmenge
  - Abrechnung nach genutzer CPU-Stunde
  - Konstanter Preis über bestimmte Vertragslaufzeit

## Vorteile für den Servicenehmer
- Geringes Investitionsrisiko
- Transparente IT-Kosten
- Beschleunigte Implementierung
- Verringerung der IT-Prozesskomplexität
- Mobilität
- Konzentation auf das Kerngeschäft

## Nachteile für den Servicenehmer
- Abhängigkeit vom Servicegeber
- Langsame Datenübertragungsgechwindigkeit
- Geringere Anpassungsmöglichkeiten
- Daten- und Transaktionssicherheit

## Vorteile für den Servicegeber
- Erweiterung des IT-Leistungsangebots
- Erzielung zusätzlicher Umsatzerlöse
- Längerfristig gesicherte Einnahmen
- Bessere Liquidätsplanungsoption
- Geringere Wahrscheinlichkeit des Auftretens von Softwarepiraterie

## Nachteile für Servicegeber
- Investitionsrisiko
- Akzeptansprobleme auf dem IT-Markt
- Möglicher Imagesschaden und Umsatzverluste

## Datenschutz
- Die Daten der Kunden und Mitarbeiter liegen nicht auf den eigenen Rechnern, sondern beim Servivegeber.
- Der Kunde ist nach dem §11 des Bundesdatenschutzgesetzes  (Auftragsdatenverarbeitung) zu folgendem verpflichtet:
  - Sorgfältige Auswahl des Anbieters
  - Regelmäßige Kontrollen
  - Dokumentation der Ergebnisse der Kontrollen
- Außerdem bleibt der Kunde für die Rechtmäßigkeit der Datenverarbeitung verantwortlich.
- SaaS-Verträge müssen zudem den 10-Punkte-Katalog des $11 BDSG umsetzen, da dem Kunden ansonsten Bußgelder in der höhe von bis zu 50.000 Euro drohen (§43 Absatz 1 Nr. 2b BDSG)

## Saas-Unternehmen
- Salesforce.com
- NetSuite
- Kenexa
- RightNow Technologies
- Taleo
- Paglo
- athenahealth
- Bazaarvoice
- Jive Software
- Scorpevisio AG
- weclapp GmbH
- salesdoc
- SuccessFactors