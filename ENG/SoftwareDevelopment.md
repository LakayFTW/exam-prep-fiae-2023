# Table of Content
- [Table of Content](#table-of-content)
- [Web Development](#web-development)
	- [Markup Languages](#markup-languages)
		- [HTML - Hypertext Markup Language](#html---hypertext-markup-language)
			- [DOM - Document Object Model](#dom---document-object-model)
	- [Protocols](#protocols)
		- [HTTP/S](#https)
			- [HTTP-400](#http-400)
				- [Types of HTTP-400](#types-of-http-400)
			- [HTTP-500](#http-500)
				- [Types of HTTP-500](#types-of-http-500)
- [Object Orientation](#object-orientation)
	- [Interfaces](#interfaces)
		- [Declaration](#declaration)
		- [Example](#example)
		- [Naming Conventions](#naming-conventions)
	- [Abstraction](#abstraction)
		- [Programming Languages](#programming-languages)
		- [Abstraction in Object-Oriented Programming](#abstraction-in-object-oriented-programming)

# Web Development

## Markup Languages

### HTML - Hypertext Markup Language
[^3]
HTML is a text-based markup language for structuring electronic documents such as texts with hyperlinks, images, and other content. HTML documents are the foundation of the World Wide Web (WWW) and are displayed by web browsers.

Contrary to some people's claims, HTML is **NOT** a programming language.
HTML cannot exhibit characteristics of a programming language like **variables** and **control structures**.

#### DOM - Document Object Model
[^4]
Document Object Model

- mainly HTML
- but can also be XML or XHTML
- The DOM represents a tree structure in which each element of the document is represented as a node in the tree.

## Protocols

### HTTP/S
[^1] [^2]
- Hyper Text Transport Protocol
- Secure Hyper Text Transport Protocol

#### HTTP-400
HTTP Response Code 400 refers to client errors.

##### Types of HTTP-400
- 400 Bad Request
    - The server cannot or will not process the request due to an apparent client error (incorrect request, syntax incorrect, content too large, etc.).
- 403 Forbidden
    - The request contained data that was understood by the server but not processed (entry duplicate).
- 404 Not Found
    - The requested resource could not be found.

#### HTTP-500
HTTP Response Code 500 refers to server errors.

##### Types of HTTP-500
- 500 Internal Server Error
    - A generic error message given when an unexpected condition was encountered.
- 502 Bad Gateway
    - The server acted as a gateway or proxy and received an invalid response.
- 503 Service Unavailable
    - The server cannot handle the request (too many requests, down for maintenance).

# Object Orientation

## Interfaces
An interface in object-oriented programming defines which methods exist or must exist in different classes or similar.  
An interface specifies which methods exist or must exist.  
Interfaces provide a guarantee about the methods present in a class. They indicate that all objects possessing these interfaces can be treated equally.

In programming languages that do not support multiple inheritance like Java, interfaces can be used to define compatibilities between classes that do not inherit from each other.

### Declaration
Other programming languages that support multiple inheritance, such as C++, know the concept of interfaces but treat them like ordinary classes. This is also called abstract classes. Sometimes, a separate language (a so-called Interface Description Language, IDL) is used to declare the interface - this is often the case with middleware systems like CORBA or DCOM. Object-based languages without strict typing usually do not have interfaces.

### Example
**C#**
```c#
public interface IFace
{
    void Move(float x, float y);
    void Turn(float x, float y, double angle);
    void Scale(float factor);
    double GetArea();
    void SetColor(Color color);
    Color GetColor();
}

public class Polygon : IFace
{
    private List<PointF> points;
    private Color color;

    public Polygon(List<PointF> points, Color color)
    {
        this.points = points;
        this.color = color;
    }

public void Move(float x, float y)
    {
        for (int i = 0; i < points.Count; i++)
        {
            PointF point = points[i];
            points[i] = new PointF(point.X + x, point.Y + y);
        }
    }

    public void Turn(float x, float y, double angleInDegrees)
    {
        double angleInRadians = angleInDegrees * (Math.PI / 180);
        double cosine = Math.Cos(angleInRadians);
        double sine = Math.Sin(angleInRadians);
        for (int i = 0; i < points.Count; i++)
        {
            PointF point = points[i];
            points[i] = new PointF((float)(cosine * (point.X - x) - sine * (point.Y - y) + x), (float)(sine * (point.X - x) + cosine * (point.Y - y) + y));
        }
    }

    public void Scale(float factor)
    {
        for (int i = 0; i < points.Count; i++)
        {
            PointF point = points[i];
            points[i] = new PointF(factor * point.X, factor * point.Y);
        }
    }

    public double GetArea()
    {
        double area = 0.0;
        for (int i = 0; i < points.Count; i++)
        {
            PointF point1 = points[i];
            PointF point2 = points[(i + 1) % points.Count];
            area += (point1.Y + point2.Y) * (point1.X - point2.X);
        }
        return Math.Abs(area / 2.0);
    }

    public void SetColor(Color color)
    {
        this.color = color;
    }

    public Color GetColor()
    {
        return color;
    }
}
```

### Naming Conventions
In some programming languages, it is customary to make interfaces recognizable by special prefixes or suffixes. For example, an "I" or "IF" is often appended.
In the example above, this would be an "I" for "IFace", which is typically applied in C#.

## Abstraction
[^6]
The term abstraction is frequently used in computer science and describes the separation between **concept** and **implementation**.

### Programming Languages
Different programming languages offer different ways of abstraction, such as:
- In object-oriented languages like C++, Object Pascal, or Java, the concept of abstraction has been implemented in the form of a separate declarative statement. After such a declaration, it is the programmer's task to implement a class to create an instance of an object from it.

### Abstraction in Object-Oriented Programming
- Needs elaboration


[^1]: https://de.wikipedia.org/wiki/HTTP-Statuscode
[^2]: https://de.wikipedia.org/wiki/Hypertext_Transfer_Protocol
[^3]: https://de.wikipedia.org/wiki/Hypertext_Markup_Language
[^4]: https://de.wikipedia.org/wiki/Document_Object_Model
[^5]: https://de.wikipedia.org/wiki/Schnittstelle_(Objektorientierung)
[^6]: https://de.wikipedia.org/wiki/Abstraktion_(Informatik)