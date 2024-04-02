# Table of Content
- [Table of Content](#table-of-content)
- [Use-Case Diagram](#use-case-diagram)
  - [Keywords](#keywords)
  - [Elements](#elements)
    - [System Context](#system-context)
    - [Actor](#actor)
    - [Use Case](#use-case)
    - [Relationships](#relationships)
      - [Association/Communication](#associationcommunication)
      - [Multiplicity](#multiplicity)
      - [Generalization of Use Cases](#generalization-of-use-cases)
      - [Generalization of Actors](#generalization-of-actors)
      - [Include Relationship](#include-relationship)
      - [Extend Relationship](#extend-relationship)
      - [Extend Relationship with Extension Point](#extend-relationship-with-extension-point)
      - [Use Case](#use-case-1)

# Use-Case Diagram

[^1]

The Use-Case Diagram, also known as an application case diagram, is one of the diagram types of the Unified Modeling Language (UML). It represents use cases and actors with their respective dependencies and relationships.

## Keywords

- **Objective**: To show as simply as possible what one wants to do with the software system to be built, i.e., which application cases exist.
- **Actors**: Represented as "stick figures," which can represent both people like customers or administrators and a system.
- **Use Cases**: Represented in ellipses. They must be described (e.g., in a comment or a separate file).
- **Associations**: Between actors and use cases must be marked by lines.
- **System Boundaries**: Marked by rectangles.
- **Include Relationship**: From the calling use case to the included use case, represented by a dashed arrow with the stereotype `<<include>>`.
- **Extend Relationship**: From the extending use case to the calling use case, represented by a dashed arrow with the stereotype `<<extend>>`. The extending use case can, but does not have to, be activated.

## Elements

### System Context
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/35/Uml-UseCase-Systemkontext.svg/800px-Uml-UseCase-Systemkontext.svg.png" width="200px">

The system context is marked by system boundaries in the form of rectangles.

### Actor
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/dd/Uml-UseCase-Akteur.svg/800px-Uml-UseCase-Akteur.svg.png" width="120px">

Actors are represented as "stick figures," which can represent both people like customers or administrators and a system.

### Use Case

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Uml-UseCase-Anwendungsfall.svg/1920px-Uml-UseCase-Anwendungsfall.svg.png" width="200px">

Use cases are represented in ellipses. They must be described (e.g., in a comment or a separate file).

### Relationships 

#### Association/Communication

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/79/Uml-UseCase-Assoziation.svg/1920px-Uml-UseCase-Assoziation.svg.png" width="300px">

Association/Communication between actor and use case.

#### Multiplicity

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/50/Uml-UseCase-Multiplizitaet.svg/1920px-Uml-UseCase-Multiplizitaet.svg.png" width="300">

Multiplicity between actor and use case, where the default of the actor is 1.

#### Generalization of Use Cases

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4e/Uml-UseCase-Generalisierung.svg/1920px-Uml-UseCase-Generalisierung.svg.png" width="300">

#### Generalization of Actors

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Uml-UseCase-Generalisierung2.svg/800px-Uml-UseCase-Generalisierung2.svg.png" width="300">

#### Include Relationship

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/31/Uml-UseCase-Include.svg/1920px-Uml-UseCase-Include.svg.png" width="300">

Include relationships in the use-case diagram, where use case A includes use case B.

#### Extend Relationship

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d1/Uml-UseCase-Extend.svg/1920px-Uml-UseCase-Extend.svg.png" width="300">

Extend relationships in the use-case diagram, where use case A extends use case B.

#### Extend Relationship with Extension Point

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1c/Uml-UseCase-Extend2.svg/1920px-Uml-UseCase-Extend2.svg.png" width="300">

Extend relationship with extension point, where use case A extends use case B under the specified condition.

#### Use Case

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/f5/Uml-UseCase-Anwendungsfall2.svg/1920px-Uml-UseCase-Anwendungsfall2.svg.png" width="150">

Use case with extension point.

[^1]: https://en.wikipedia.org/wiki/Use_case_diagram
