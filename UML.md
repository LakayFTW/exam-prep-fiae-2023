# Table of Content
- [Programmablaufplan(PAP)](#programmablaufplan-pap)
- [Klassendagramm:](#klassendiagramm)
  - [Beziehungen](#beziehungen)

---

# Programmablaufplan (PAP) [^1]
- Wird auch als Flussdiagramm (Flowchart) oder Programmsturkturplan bezeichnet
Die Grafische Darstellung eines Algorithmus in einem Programm und beschreibt die
- Folge von Operationen zur Lösung einer Aufgabe
- DIN 66001 für Datenflusspläne

## Elemente
- Kreis; Oval/Rechtek abgerundet: Terminator
- Pfeil, Linie: Verbindung zum nächsten Element
- Rechteck: Operation (Tätigkeit)
- Rechteck mit doppelten, vertikalen Linien: Unterpogramm ausführen
- Raute: Verzweigung / Entscheidung
- Parallelogramm: Ein- und Ausgabe
---
<br></br>
# Klassendiagramm [^2]
Ein Klassendiagramm ist ein UML-Diagrammtyp, der ein System beschreibt, indem er die verschiedene Objekttypen innerhalb eines Systems und die Arten der statischen Beziehungen, die zwischen ihnen bestehen, visualisiert. Sie veranschaulicht auch die Operation und Attribute der Klassen.

## Klasse
<img title="Klassendiagramm" src="./img/UML-Klassendiagramm/Class-Notation.png"></img>
<br/>
- Klassen stellen die zentralen Objekte in einem System dar. Sie wird durch ein Rechteck mit bis zu 3 Fächern dargestellt.
- Die erste zeigt den Namen der Klasse, während die mittlere die Attribute der Klasse zeigt, die die Merkmale der Objekte sind. Die untere listet die Operationen der Klasse auf, die das Verhalten der Klasse darstellt.

## Schnittstelle
<img title="Interface" src="./img/UML-Klassendiagramm/Interface-notation.png"></img>
<br/>
- Das Schnittstellensymbol in Klassendiagrammen zeigt eine Reihe von Operationen an, die die Verantwortung einer Klasse detailliert beschreiben würde.

## Paket
<img title="Package" src="./img/UML-Klassendiagramm/Package.png"></img>
<br/>
- Das Paketsymbol wird verwendet, um Klassen oder Schnittstellen zu gruppieren, die entweder von ähnlicher Art oder verwandt sind. Die Gruppierung dieser Entwurfselemente mit Hilfe der Gehäusesymbole verbessert die Lesbarkeit des Diagramms.

## Beziehungen [^3]
<img title="Relations" src="./img/UML-Klassendiagramm/Class-Diagram-Relations.png"></img>
<br/>

### Assoziation - Association
- Die Assoziation gibt an, dass eine Eigenschaft einer Klasse einen Verweis auf eine Instanz (oder Instanzen) einer anderen Klasse enthält.
- Es gibt mehrere Arten der Assoziation.
    - Zweigassoziation
    - Einwegassoziation
    - Selbstassoziation
    - Merfachnummernassoziation

__BSP:__<br/>
Autos und Fahrer, ein Auto entspricht einem bestimmten Fahrer und ein Fahrer kann mehrere Autos fahren.
<br/>
<img src="./img/UML-Klassendiagramm/examples-relations/class-diagram-association-example.png" ></img>
<br/>
- In UML-Diagrammen können bidirektionale Assoziationen zwei Pfeile oder keine Pfeile haben und unidirektionale Assoziationen oder Selbstassoziationen haben einen Pfeil.
- In einer Multiplizitätsbeziehung können Sie der zugehörigen Zeile direkt eine Zahl hinzufügen, um die Anzahl der Objekte in der entpsrechenden Klasse anzugeben
    - 1..1: Nur eine
    - 0..*: Null oder eine
    - 1..*: ein oder mehr
    - 0..1: Nein oder nur eins
    - m..n: mindestens m, höchstens n (m<=n)

### Vererbung - Inheritance
- __Vererbung__ wird auch __Generalisierung__ genannt und wird verwendet, um die Beziehung zwischen Eltern- und Kindklassen zu beschreiben. Eine übergeordnete Klasse wird auch als Basisklasse bezeichnet und eine Unterklasse wird auch als abgeleitete Klasse bezeichnet.
- Die Unterklasse erbt alle Funktionen der Elternklasse, und die Elternklasse hat alle Attribute, Methoden und Unterklassen. Unterklassen enthalten zusätzliche Informationen zu den gleichen Informationen wie die übergeordnete Klasse.

__BSP:__<br/>
Busse, Taxen und Autos sind Autos, sie alle haben Namen und sie können alle auf der Straße sein.
<br/>
<img src="./img/UML-Klassendiagramm/examples-relations/class-diagram-inheritance-example.png"></img>
<br/>

### Realisierung / Umsetzung - Realization / Implementation
- __Implementierung__ (Implementation) wird hauptsächlich verwendet, um die Beziehung zwischen Schnittstellen und Implementierungsklassen zu spezifizieren.
- Eine Schnittstelle (einschließlich einer abstrakten Klasse) ist eine Sammlung von Methoden. In einer Implementierungsbeziehung implementiert eine Klasse eine Schnittstelle, und Methoden in der Klasse implementieren alle Methoden der Schnittstellendeklaration.

__BSP:__<br/>
Autos und Schiffe sind Fahrzeuge, und das Fahrzeug ist nur ein abstraktes Konzept eines mobilen Werkzeugs, und das Schiff und das Fahrzeug realisieren die spezifischen mobilen Funktionen.
<br/>
<img src="./img/UML-Klassendiagramm/examples-relations/class-diagram-realization-example.png"></img>
<br/>

### Abhängigkeit - Dependency


[^1]: https://de.wikipedia.org/wiki/Programmablaufplan
[^2]: https://creately.com/blog/de/diagramme/uml-klassendiagramm/
[^3]: https://blog.visual-paradigm.com/de/what-are-the-six-types-of-relationships-in-uml-class-diagrams/