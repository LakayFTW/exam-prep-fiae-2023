# Table of Content
- [Table of Content](#table-of-content)
- [Use-Case Diagramm](#use-case-diagramm)
  - [Keywords](#keywords)
  - [Elemente](#elemente)
    - [Systemkontext](#systemkontext)
    - [Akteur](#akteur)
    - [Anwendungsfall](#anwendungsfall)
    - [Beziehungen](#beziehungen)
      - [Assoziation/Kommunikation](#assoziationkommunikation)
      - [Mulizplizität](#mulizplizität)
      - [Generalisierung von Anwendungsfällen](#generalisierung-von-anwendungsfällen)
      - [Generalisierung von Akteuren](#generalisierung-von-akteuren)
      - [Include-Beziehung](#include-beziehung)
      - [Extend-Beziehung](#extend-beziehung)
      - [Extend-Beziehung mit extension point](#extend-beziehung-mit-extension-point)
      - [Anwendungsfall](#anwendungsfall-1)

# Use-Case Diagramm

[^1]

Das Use-Case DIagramm wird auch Anwendungsfalldiagramm bezeichnet und ist eine der Diagrammarten der Unified Modelling Language (UML). Es stellt Anwendungsfälle und Akteure mit ihren jeweiligen Abhängigkeiten und Beziehungen dar.

## Keywords

- **Ziel** ist es, möglichst einfach zu zeigen, was man mit dem zu bauenden Softwaresystem machen will, welche Fälle der Anwendung es also gibt.
- **Akteure** werden als "Strichmännchen" dargestellt, welche sowohl Personen wie Kunden oder Administratoren als auch ein System darstellen können.
- **Anwendungsfälle** werden in Ellipsen dargestellt. Sie müssen beschrieben werden (z.B. in einem Kommentar oder einer eigenen Datei).
- **Assoziationen** zwischen Akteuren und Anwendungsfällen müssen durch Linien gekennzeichnet werden.
- **Systemgrenzen** werden durch Rechtecke gekennzeichnet.
- **include-Beziehung** vom aufrufenden Anwendungsfall zum inkludierten Anwendungsfall werden als gestrichelter Pfeil mit dem Stereotyp ``<<include>>`` dargestellt.
- **extend-Beziehung** vom erweiternden Anwendungsfall zum aufrufenden Anwendungsfall werden als gestrichelter Pfeil mit dem Stereotyp ``<<extend>>`` dargestellt. Der erweiternde Anwendungsfall kann, muss aber nicht aktiviert werden.

## Elemente

### Systemkontext
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Uml-UseCase-Systemkontext.svg/800px-Uml-UseCase-Systemkontext.svg.png" width="200px">

Der Systemkontext wurd durch Systemgrenzen in Form von Rechtecken gekennzeichnet.

### Akteur
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/dd/Uml-UseCase-Akteur.svg/800px-Uml-UseCase-Akteur.svg.png" width="120px">

Akteure werden als "Strichmännchen" dargestellt, welche sowohl Personen wie Kunden oder Administratoren als auch ein System darstellen können.

### Anwendungsfall

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Uml-UseCase-Anwendungsfall.svg/1920px-Uml-UseCase-Anwendungsfall.svg.png" width="200px">

Anwendungsfälle werden in Ellipsen dargestellt. Sie müssen (z.B. in einem Kommentar oder einer eigenen Datei) beschrieben werden.

### Beziehungen 

#### Assoziation/Kommunikation

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/79/Uml-UseCase-Assoziation.svg/1920px-Uml-UseCase-Assoziation.svg.png" width="300px">

Assoziation / Kommunikation von Akteur und Anwendungsfall

#### Mulizplizität

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Uml-UseCase-Multiplizitaet.svg/1920px-Uml-UseCase-Multiplizitaet.svg.png" width="300">

Multiplizität von Akteur und Anwendungsfall, wobei die Voreinstellung des Akteurs 1 ist.

#### Generalisierung von Anwendungsfällen

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Uml-UseCase-Generalisierung.svg/1920px-Uml-UseCase-Generalisierung.svg.png" width="300">

#### Generalisierung von Akteuren

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Uml-UseCase-Generalisierung2.svg/800px-Uml-UseCase-Generalisierung2.svg.png" width="300">

#### Include-Beziehung

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Uml-UseCase-Include.svg/1920px-Uml-UseCase-Include.svg.png" width="300">

Include-Beziehungen im Anwendungsfalldiagramm, wobei Anwendungsfall A den Anwendungsfall B beinhaltet

#### Extend-Beziehung

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Uml-UseCase-Extend.svg/1920px-Uml-UseCase-Extend.svg.png" width="300">

Extend-Beziehung im Anwendungsfalldiagramm, wobei Anwendungsfall A den Anwendungsfall B erweitert.

#### Extend-Beziehung mit extension point

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1c/Uml-UseCase-Extend2.svg/1920px-Uml-UseCase-Extend2.svg.png" width="300">

Extend-Beziehung mit extension point, wobei Anwendungsfall A den Anwendungsfall B unter der angegebenen Bedingung erweitert.

#### Anwendungsfall

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Uml-UseCase-Anwendungsfall2.svg/1920px-Uml-UseCase-Anwendungsfall2.svg.png" width="150">

Anwendungsfall mit extension point.

[^1]: https://de.wikipedia.org/wiki/Anwendungsfalldiagramm