# Table of Content
- [Table of Content](#table-of-content)
- [Normalformen](#normalformen)
  - [1. Normalform](#1-normalform)
    - [Erläuterung](#erläuterung)
    - [Beispiel](#beispiel)
    - [Mögliche Fehler](#mögliche-fehler)
      - [Einfüge-Anomalie](#einfüge-anomalie)
      - [Änderungs-Anomalie](#änderungs-anomalie)
      - [Lösch-Anomalie](#lösch-anomalie)
  - [2. Normalform](#2-normalform)
    - [Erläuterung](#erläuterung-1)
    - [Beispiel](#beispiel-1)
    - [Mögliche Fehler](#mögliche-fehler-1)
      - [Änderungs-Anomalie](#änderungs-anomalie-1)
  - [3. Normalform](#3-normalform)
    - [Erläuterung](#erläuterung-2)
    - [Beispiel](#beispiel-2)
    - [Mögliche Fehler](#mögliche-fehler-2)

---
<br>

# Normalformen
[^2] [^1]<br>
Zurzeit gebräuchliche Normalformen sind:
- 1. Normalform (1NF)
- 2. Nromalform (2NF)
- 3. Normalform (3NF)
- Boyce-Codd-Normalform (BCNF) [Wird hier nicht besprochen]
- 4. Normalform (4NF) [Wird hier nicht besprochen]
- 5. Normalform (5NF) [Wird hier nicht besprochen]

## 1. Normalform
### Erläuterung
Jedes __Attribut__ der __Relation__ muss einen atomaren Wertebereich haben, und die Relation muss frei von Wiederholungen sein.<br>
Das heißt, dass pro Datenfeld nur maximal ein Wert enthalten sein darf.

### Beispiel
__0. Normalform__
<br>
<img title="0 Normalform" src="./img/Normalformen/normalisierung_0nf_bsp.png">
<br>
Im oberen Beispiel werden mehrere Daten in einem Datenfeld gespeichert. Dies wird auch die 0. Normalform oder NF² (Non-First-Normal-Form) genannt.<br>
Datensätze aus dieser Tabelle können hier nicht einzelnd entnommen werden. Möchte man z.B. PrüfFachNr von Meier bekommen, bekommt man "10", "12" und "16".
In der Definition heißt es: "...maximal einen Wert...", was einem in der 1. Normalform erlaubt Null-Werte einzutragen, wenn man z.B. noch nicht vergeben Punkte in einem Kurs.
<br>

Es gibt zwei Arten Mehrfachattribute zu beseitigen:
1. Das Mehrfachattribut wird innerhalb des Datensatzes in mehrere Einfachattribute zerlegt, d.h. der Datensatz erhält mehr Attribute.
2. Wenn das Mehrfachattribut eine Liste von typgleichen Daten enthält, wird jedem Wert der Liste einen eigenem Datensatz zugeordnet.

Das Ergebnis könnte so aussehen:
<br>
<img title="1. Normalform" src="./img/Normalformen/normalisierung_1nf_bsp.png">
<br>

### Mögliche Fehler
#### Einfüge-Anomalie
1. Zur bestehenden Prüfungsnummer erfolgt ein weiterer Eintrag mit anderer Prüffachbezeichnung.
2. Zur selben Matrikelnummer erfolgt ein Eintrag mit anderem Studentennamen.
3. Der Eintrag eines Studenten, der noch kein Prüfungsfach gewählt hat, liefert Nullwerte in der Prüfungsfachnummer, da dies aber Teil des Primärschlüssels ist, darf dies nicht sein. Es verletzt die Integrität.

#### Änderungs-Anomalie
4. Wenn der Name des Professors sich ändert, muss dies in allen Zeilen geschehen.
5. Den einzelnen Prüfungsfächern werde neue Prüfer zugeordnet. Überall.

#### Lösch-Anomalie
- Einige Daten könnten verloren gehen wenn ein Tupel gelöscht wird.

## 2. Normalform
### Erläuterung
Eine Relation ist dann in der zweiten Normalform wenn die erste Normalform erreicht wurde und kein Nichtprimärattribut funktionial von einer echten Teilmenge eines Schlüsselkandidaten abhängt.

### Beispiel
Wir müssen die Tabelle aus dem Beispiel der ersten Normalform aufteilen, da weder der Name des Studenten noch die Bezeichnung des Prüfungsfach voll vom Pirmärschlüssel abhängig sind. Das Attribut Note ist voll vom Primäschlüssel abhängig und bleibt in der Relation.<br>
So ergibt sich folgende Realtionen in der zweiten Normalform.

<br>
<img title="2. Normalform" src="./img/Normalformen/normalisierung_2nf_bsp.png">
<br>

In allen entstandenen Relationen sind alle Nicht-Primärschlüssel-Attribute voll funktional abhängig von den jeweiligen Primärschlüsseln.

### Mögliche Fehler
#### Änderungs-Anomalie
4. Wenn der Name des Professors sich ändert, muss dies in allen Zeilen geschehen.

## 3. Normalform
### Erläuterung
Eine Relation befindet sich in der dritten Normalform, wenn die zweite Normalform erfüllt ist und keine Abhängigkeiten der Nichtschlüssel-Attribute untereinander bestehen. Solche Abhängigkeiten bezeichnet man auch als __transitive__ Abhängigkeiten. Weiterhin müssen alle Nichtschlüssel voll funktional abhängig vom Schlüsselattribut sein.
<br>

### Beispiel
Durch die Überführung in die zweite Normalform haben wir Redundanzen weitgehend beseitigt, jedoch fällt auf, dass das Attribut "ProfName" mehrmals vorkommt. obwohl mit ProfNr der Name des Professors schon gegeben wäre. Dies können wir mit der Überführung in die dritte Normalform beseitigen.

<br>
<img title="3. Normalform" src="./img/Normalformen/normalisierung_3nf_bsp.png">
<br>

### Mögliche Fehler
Nun sind alle Anomalien / Redundanzen beseitigt.

[^1]: https://de.wikipedia.org/wiki/Normalisierung_(Datenbank)#Normalformen
[^2]: https://info-wsf.de/Normalformen/