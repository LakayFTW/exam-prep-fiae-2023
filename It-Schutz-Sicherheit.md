# Table of Content
- [Table of Content](#table-of-content)
- [Datenschutz](#datenschutz)
  - [Art. 32 der DSGVO - Sicherheit und Verarbeitung](#art-32-der-dsgvo---sicherheit-und-verarbeitung)
  - [3 Aspekte der It-Sicherheit](#3-aspekte-der-it-sicherheit)
  - [Authentifizierung, Authentisierung, Autorisierung](#authentifizierung-authentisierung-autorisierung)
  - [ISMS (Informationssicherheitsmanagementsystem)](#isms-informationssicherheitsmanagementsystem)
  - [Schutzbedarfsanalyse](#schutzbedarfsanalyse)
- [Symmetrische Verschlüsselung](#symmetrische-verschlüsselung)
  - [Verfahren](#verfahren)
  - [Vorteile](#vorteile)
  - [Nachteile](#nachteile)
- [Asymmetrische Verschlüsselung](#asymmetrische-verschlüsselung)
  - [Vorteile](#vorteile-1)
  - [Nachteile](#nachteile-1)

---
<br>

# Datenschutz
- DSGVO - Datenschutz-Grundverordnung
- BDSG - Bundesdatenschutzgesetz

## Art. 32 der DSGVO - Sicherheit und Verarbeitung
[^1]
1. Pseudonymisierung und Verschlüsselung personbezogener Daten
2. die Fähigkeit, die Vertraulichkeit, die Integrität und Belastbarkeit der Systeme und Dienste im Zusammenhang mit der Verarbeitung auf Dauer sicherzustellen
3. die Fähigkeit, die Verfügbarkeit der personenbezogener Daten und den Zugang zu ihnen bei einem physischen oder technischen Zwischenfall rasch wiederherzustellen
4. ein Verfahren zur regelmäßigen Überprüfung, Bewertung und Evaluierung der Wirksamkeit der technischen und organisatorischen Maßnahmen zur Gewährleistung der Sicherheit der Verarbeitung

Zusätzlich muss man bei der Einhaltung und Beurteilung dieser Vorgaben an die Risiken denken und einhalten, die mit der Verarbeitung verbunden sind.

## 3 Aspekte der It-Sicherheit
- Vertraulichkeit
- Integrität
- Verfügbarkeit

## Authentifizierung, Authentisierung, Autorisierung
[^2]
- Authentifizierung = Prüfung der angegebenen Daten
- Authentisierung = Eine Person legt Informationen vor um sich zu identifizieren
- Autorisierung = Wenn Informationen richtig sind gibt Gegenseite Zugang frei

## ISMS (Informationssicherheitsmanagementsystem)
[^3]
Die Aufstellung von Verfahren und Regeln innerhalb einer Organisation, die dazu dienen, die Informationssicherheit dauerhaft zu definieren, zu steuern, zu kontrollieren, aufrechtzuerhalten und fortlaufend zu verbessern

## Schutzbedarfsanalyse
[^4]
Bei der Schutzbedarfsanalyse wird anhand der eingesetzten Informationstechnik und der Informationen, deren Schutz bewertet je nach dem wie angemessen dies ist. Hierzu betrachtet man jede Anwendung und die verarbeiteten Informationen und welche Schäden zu erwarten sind. Meist wird hier dann in "Normal", "Hoch", "Sehr Hoch" kategorisiert. Bei der Vertraulichtkeit meist in "öffentlich", "intern", "geheim".

---
<br>

# Symmetrische Verschlüsselung
In der Symmetrischen Verschlüsselung verwenden beide Teilnehmer den gleichen Schlüssel, dieser ist für die Verschlüsselung wie auch für die Entschlüsselung Zuständig.

## Verfahren
- AES
- DES
- Triple-DES
- IDEA
- Blowfish
- QUISCI
- Twofish

Diese Verfahren sind auch bei großen Datenmengen sehr schnell.

## Vorteile
- Einfaches Schlüsselmanagement da nur ein Schlüssel für Ent- und Verschlüsselung gebraucht wird.
- Hohe Geschwindigkeit für Ent- und Verschlüsselung.

## Nachteile
- Nur ein Schlüssel für Ver- und Entschlüsselung, Schlüssel darf nicht in unbefugte Hände gelange.
- Schlüssel muss über einen sicheren Weg übermittelt werden.
- Anzahl der Schlüssel bezogen auf die Anzahl der Teilnehmer wächst quadratisch.

# Asymmetrische Verschlüsselung
Die Asymmetrische Verschlüsselung wird auch Public-Key-Verfahren genannt. Hier gibt es nicht nur einen Schlüssel sondern gleich zwei, dieses sogenannte Schlüsselpaar setzt sich aus einem privaten Schlüssel (Private Key) und einem öffentlichen Schlüssel (Public Key) zusammen. Mit dem Private Key, werden Daten Entschlüsselt oder eine digitale Signatur erzeugt. Mit dem Public Key kann man Daten verschlüsseln und erzeugte Signaturen auf ihren Authentizität überprüfen. Dieses Verfahren ist sehr langsam und eignen sich daher nur für kleine Datenmengen.

## Vorteile
- Relativ hohe Sicherheit.
- Es werden nicht so viele Schlüssel benötigt, wie bei einem symmetrischen Verschüsselungsverfahren, somit weniger Aufwand der Geheimhaltung des Schlüssels.
- Kein Schlüsselverteilungsproblem, da Public Key für jeden ohne Probleme zu erreichen ist.
- Möglichkeit der Authentifikation durch elektronische Unterschriften (digitale Signaturen).

## Nachteile
- Arbeiten sehr langsam ca. 10000 Mal langsamer als symmetrische.
- Große benötigte Schlüssellänge.
- Probleme bei mehreren Empfänger einer verschlüsselten Nachricht, da jedes Mal die Nachricht extra verschlüsselt werden muss.
- Sicherheitsrisiko durch für jeden zugänglichen Public Key -> Man in the Middle.

[^1]: https://dsgvo-gesetz.de/art-32-dsgvo/
[^2]: https://www.dr-datenschutz.de/authentisierung-authentifizierung-und-autorisierung/
[^3]: https://de.wikipedia.org/wiki/Information_Security_Management_System
[^4]: https://de.wikipedia.org/wiki/IT-Grundschutz#Schutzbedarfsfeststellung
