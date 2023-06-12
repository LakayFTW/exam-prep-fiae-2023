# Table of Content
- [Table of Content](#table-of-content)
- [Datenschutz](#datenschutz)
  - [Art. 32 der DSGVO - Sicherheit und Verarbeitung](#art-32-der-dsgvo---sicherheit-und-verarbeitung)
  - [3 Aspekte der It-Sicherheit](#3-aspekte-der-it-sicherheit)
  - [Authentifizierung, Authentisierung, Autorisierung](#authentifizierung-authentisierung-autorisierung)
  - [ISMS (Informationssicherheitsmanagementsystem)](#isms-informationssicherheitsmanagementsystem)
- [Schutzbedarfsanalyse](#schutzbedarfsanalyse)
  - [Identifikation der zu schützenden Daten](#identifikation-der-zu-schützenden-daten)
  - [Zusammenfassung der Daten zu Datengruppen](#zusammenfassung-der-daten-zu-datengruppen)
  - [Bestimmen der schlimmsten möglichen Folgen des Verlustes](#bestimmen-der-schlimmsten-möglichen-folgen-des-verlustes)
  - [Einordnung in eine Schutzbedarfskategorie](#einordnung-in-eine-schutzbedarfskategorie)
  - [Verstoß gegen Gesetze, Vorschriften und Verträge](#verstoß-gegen-gesetze-vorschriften-und-verträge)
    - [Datenschutzgesetze](#datenschutzgesetze)
    - [Vorschriften zur Mitbestimmung](#vorschriften-zur-mitbestimmung)
    - [Verträge](#verträge)
- [Symmetrische Verschlüsselung](#symmetrische-verschlüsselung)
  - [Verfahren](#verfahren)
  - [Vorteile](#vorteile)
  - [Nachteile](#nachteile)
- [Asymmetrische Verschlüsselung](#asymmetrische-verschlüsselung)
  - [Vorteile](#vorteile-1)
  - [Nachteile](#nachteile-1)
- [2FA - 2 Faktor Authentifizierung](#2fa---2-faktor-authentifizierung)
  - [Authentifizieren](#authentifizieren)
  - [Authentisieren](#authentisieren)
  - [Autorisieren](#autorisieren)

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

<br>

# Schutzbedarfsanalyse
[^4] [^5]
Bei der Schutzbedarfsanalyse wird anhand der eingesetzten Informationstechnik und der Informationen, deren Schutz bewertet je nach dem wie angemessen dies ist. Der Wert der Daten und Funktionen ist in der Regel um ein Vielfaches höher als der Wert von den IT Geräten selbst. Daher sind angemessene Sicherheitsmaßnahmen aus den Sicherheitsanforderungen der IT-Verfahren abzuleiten.

<br>

<a href="https://tetfolio.fu-berlin.de/web/ii_555094:9">
  <img src="https://tetfolio.fu-berlin.de/IMPAL/659400.gif" width="500" title="Struktur eine Schutzbedarfanalyse">
</a>

<br>

Der Schutzbedarf wird über die Abschätzung der schlimmsten denkbaren Folgen des Verlustes von __Vertraulichkeit__, __Integrität__ und __Verfügbarkeit__ ermittelt. Die Abschätzung hat gesondert für folgende sechs Schadenskategorien zu erfolgen:
- Beeinträchtigung des informationellen Selbstbestimmungsrechts
- Beeinträchtigung der persönlichen Unversehrtheit
- Beeinträchtigung der Aufgabenerfüllung
- Negative Außenwirkung
- Finanzielle Auswirkungen
- Verstoß gegen Gesetze, Vorschriften und Verträge

<br>

Hierzu betrachtet man jede Anwendung und die verarbeiteten Informationen und welche Schäden zu erwarten sind. Meist werden diesen in die Schutzklassen "normal", "hoch", "sehr hoch" kategorisiert. Wird als Ergebnis der Schutzbedarfsanalyse das gewählte IT-Verfahren in die Klasse "normal" eingestuft, reichen die Maßnahmen des IT-Grundschutzes aus. In allen anderen Fällen muss eine verfahrensspezifische Risikoanalyse durchgeführt werden.

<br>

__Bei der Schutzbedarfsanalyse werden folgende Schritte angewendet:__
1. Identifikation der zu schützenden Daten
2. Zusammenfassung der Daten zu Datengruppen (optional)
3. Bestimmen der schlimmsten möglichen Folgen
4. Einordnung in eine Schutzbedarfskategorie

<br>

## Identifikation der zu schützenden Daten
An erster Stelle steht die Identifikation aller Daten, die innerhalb des analysierten IT-Verfahrens verarbeitet bzw. gespeichert werden.
> __Beispiel:__ Vorname, Nachname, Straße, Hausnummer, Postleitzahl und Ort, Forschungsergebnisse, Patentanmeldung

<br>

## Zusammenfassung der Daten zu Datengruppen
Häufig lassen sich mehrere Einzeldaten inhaltlich zu Datengruppen zusammenfassen. Die weiteren Schritte sind dann stets auf diese Datengruppen anzuwenden und nicht mehr auf die dort enthaltenen Einzeldaten.
>__Beispiel:__  
Kontaktdaten 
(Vorname, Nachname, Strasse, Hausnummer, PLZ und Ort)<br> 
Forschungsergebnisse<br> 
Patentanmeldung

<br>

## Bestimmen der schlimmsten möglichen Folgen des Verlustes
Jede Datengruppe ist jeweils bezüglich der genannten sechs Schadenskategorien zu bewerten. Für jede der sechs Schadenskategorien ist zu überlegen, welche Folgen die Beeinträchtigung der Schutzziele __Vertraulichkeit__, __Integrität__, __Verfügbarkeit__ im schlimmsten Fall hätte.

<br>

>Beispiel Vertraulichkeit:<br>
__Vorfall:__ Unbefugte erlangen Kenntnis von Personaldaten.<br>
__Folgen:__ Der Umgang mit Kollegen und Kolleginnen kann beeinträchtigt werden.

<br>

>Beispiel Integrität:<br>
__Vorfall:__ Forschungsdaten werden unbefugt verändert.<br>
__Folgen:__ Es muss von einem überregionalen Ansehensverlust ausgegangen werden.

<br>

>Beispiel Verfügbarkeit:<br>
__Vorfall:__ Personaldaten stehen nicht zur Verfügung.<br>
__Folgen:__ Es kommt zu Verzögerungen bei der Auszahlung der Bezüge.

<br>

## Einordnung in eine Schutzbedarfskategorie
Die in den Abschätzungsüberlegungen festgestellten schlimmsten Folgen müssen anhand der Kategorien in der Bewertungstabelle eingestuft werden.

__Hier ist ein Beispiel für die Einstufung beim Verlust von Vertraulichkeit in einer Tabelle:__

<table cellspacing="2" cellpadding="2">
  <tbody>
    <tr>
      <td colspan="1" rowspan="2"><b>Schadenskategorien</b></td>
      <td colspan="1" rowspan="2">Bedrohung</td>
      <td colspan="3" rowspan="1">Abschätzung des Schadens&nbsp;</td>
    </tr>
    <tr>
      <td>normal</td>
      <td>hoch</td>
      <td>sehr hoch</td>
    </tr>
    <tr>
      <td>
        Beeinträchtigung des informationellen Selbstbestimmungsrechts
      </td>
      <td>Bekannt werden der Daten für Unberechtigte</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td>Beeinträchtigung der persönlichen Unversehrtheit</td>
      <td>Missbrauch der Daten…</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td>Beeinträchtigung der Aufgaben-erfüllung</td>
      <td>Die Kenntnis der Daten durch Unberechtigte…</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td>Negative Außenwirkung</td>
      <td>Missbrauch der Daten…</td>
      <td><br></td>
      <td>X</td>
      <td><br></td>
    </tr>
    <tr>
      <td>Finanzielle Auswirkungen</td>
      <td>Missbrauch der Daten…</td>
      <td>X</td>
      <td><br></td>
      <td><br></td>
    </tr>
    <tr>
      <td colspan="2" rowspan="1">
        <strong>daraus resultierender Schutzbedarf:</strong>
      </td>
      <td colspan="3" rowspan="1"><strong>hoch</strong></td>
    </tr>
  </tbody>
</table>

<br>

## Verstoß gegen Gesetze, Vorschriften und Verträge
Hier müssen alle Regelungen betrachtet werden, die für das betreffende IT-Verfahren relevant sind.

<br>

### Datenschutzgesetze
>__Beispiel:__<br> 
Informationsverarbeitungsgesetz (IVG)<br>
Bundesdatenschutzgesetz (BDSG)<br>
Datenschutz-Grundverordnung (DSGVO)

<br>

### Vorschriften zur Mitbestimmung
>__Beispiel:__ IT-Grundsatzdienstvereinbarung

<br>

### Verträge
>__Beispiel:__ Vertrag über die Zusammenarbeit mit einer externen Firma

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

# 2FA - 2 Faktor Authentifizierung
## Authentifizieren
## Authentisieren
## Autorisieren

[^1]: https://dsgvo-gesetz.de/art-32-dsgvo/
[^2]: https://www.dr-datenschutz.de/authentisierung-authentifizierung-und-autorisierung/
[^3]: https://de.wikipedia.org/wiki/Information_Security_Management_System
[^4]: https://de.wikipedia.org/wiki/IT-Grundschutz#Schutzbedarfsfeststellung
[^5]: https://tetfolio.fu-berlin.de/web/ii_555094:9