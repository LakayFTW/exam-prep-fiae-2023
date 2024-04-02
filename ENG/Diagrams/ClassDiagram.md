# Table of Content
- [Table of Content](#table-of-content)
- [Class Diagram](#class-diagram)
  - [Class](#class)
  - [Interface](#interface)
  - [Package](#package)
  - [Relationships](#relationships)
    - [Association](#association)
    - [Inheritance](#inheritance)
    - [Realization / Implementation](#realization--implementation)
    - [Dependency](#dependency)
    - [Aggregation](#aggregation)
    - [Composition](#composition)

# Class Diagram
[^1]<br>
A class diagram is a UML diagram type that describes a system by visualizing the different types of objects within a system and the kinds of static relationships that exist between them. It also illustrates the operations and attributes of the classes.

## Class
<img title="Class Diagram" src="../../img/UML-Klassendiagramm/Class-Notation.png">
<br>
- Classes represent the central objects in a system. They are depicted by a rectangle with up to 3 compartments.
- The first one indicates the name of the class, while the middle one shows the attributes of the class, which are the features of the objects. The bottom one lists the operations of the class, representing the behavior of the class.

## Interface
<img title="Interface" src="../../img/UML-Klassendiagramm/Interface-notation.png">
<br>
- The interface symbol in class diagrams indicates a set of operations that would detail the responsibilities of a class.

## Package
<img title="Package" src="../../img/UML-Klassendiagramm/Package.png">
<br>
- The package symbol is used to group classes or interfaces that are either of similar kind or related. Grouping these design elements using the enclosure symbols enhances the readability of the diagram.

## Relationships
[^2]<br>
<img title="Relations" src="../../img/UML-Klassendiagramm/Class-Diagram-Relations.png">
<br>

### Association
- Association indicates that a property of one class contains a reference to an instance (or instances) of another class.
- There are several types of associations.
    - Binary association
    - Unidirectional association
    - Self-association
    - Multi-role association

__Example:__<br>
Cars and drivers, a car corresponds to a specific driver, and a driver can drive multiple cars.
<br>
<img title="Association" src="../../img/UML-Klassendiagramm/examples-relations/class-diagram-association-example.png" >
<br>
- In UML diagrams, bidirectional associations may have two arrows or no arrows, and unidirectional associations or self-associations have one arrow.
- In a multiplicity relationship, you can directly add a number to the associated line to specify the number of objects in the corresponding class
    - 1..1: Only one
    - 0..*: None or one
    - 1..*: One or more
    - 0..1: None or only one
    - m..n: At least m, at most n (m<=n)

### Inheritance
- __Inheritance__ is also called __Generalization__ and is used to describe the relationship between parent and child classes. A parent class is also referred to as a base class, and a subclass is also referred to as a derived class.
- The subclass inherits all functions of the parent class, and the parent class has all attributes, methods, and subclasses. Subclasses include additional information to the same information as the parent class.

__Example:__<br>
Buses, taxis, and cars are all vehicles, they all have names, and they can all be on the road.
<br>
<img title="Inheritance" src="../../img/UML-Klassendiagramm/examples-relations/class-diagram-inheritance-example.png">
<br>

### Realization / Implementation
- __Implementation__ is mainly used to specify the relationship between interfaces and implementation classes.
- An interface (including an abstract class) is a collection of methods. In an implementation relationship, a class implements an interface, and methods in the class implement all methods of the interface declaration.

__Example:__<br>
Cars and ships are vehicles, and the vehicle is just an abstract concept of a mobile tool, and the ship and the vehicle realize the specific mobile functions.
<br>
<img title="Realization-Implementation" src="../../img/UML-Klassendiagramm/examples-relations/class-diagram-realization-example.png">
<br>

### Dependency
- Assume that a change in class A causes a change in class B, and then say that class B depends on class A.
In most cases, dependencies are reflected in methods of a class that use the object of another class as a parameter. 
- A dependency relationship is a "use" relationship. A change to a specific thing may affect other things that use it, and use a dependency when it is necessary to specify that one thing uses another. <br>

__Example:__<br>
The car depends on gasoline. If there is no gasoline, the car cannot drive.
<br>
<img title="Dependency" src="../../img/UML-Klassendiagramm/examples-relations/class-diagram-dependency-example.png">
<br>

### Aggregation
- The relationship between the whole and a part can be separated.
- Aggregated relationships represent the relationship between the whole and a part of the class.
- A member object represents a part of the whole object, but it can also exist independently of the whole. <br>

__Example:__<br>
Bus driver and work clothes are part of the overall relationship, but they can also exist independently. The given work clothes can be worn by the bus driver, but it can also be worn by something else.
<br>
<img title="Aggregation" src="../../img/UML-Klassendiagramm/examples-relations/class-diagram-aggregation-example.png">
<br>

### Composition
- The relationship between the whole and a part cannot be separated.
- The composition relationship represents the relationship between the whole and a part of the class, and the whole and the part have a consistent lifespan. Once the whole object no longer exists, some of the objects will also cease to exist.

__Example:__<br>
A person consists of a head and a body. Both are inseparable and coexist.
<br>
<img title="Composition" src="../../img/UML-Klassendiagramm/examples-relations/class-diagram-composition-example.png">

[^1]: https://creately.com/blog/de/diagramme/uml-klassendiagramm/
[^2]: https://blog.visual-paradigm.com/de/what-are-the-six-types-of-relationships-in-uml-class-diagrams/
