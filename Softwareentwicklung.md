# Table of Content
- [Table of Content](#table-of-content)
- [Web Entwicklung](#web-entwicklung)
	- [Auszeichnungssprachen](#auszeichnungssprachen)
		- [HTML - Hypertext Markup Language](#html---hypertext-markup-language)
			- [DOM - Document Object Model](#dom---document-object-model)
	- [Protokolle](#protokolle)
		- [HTTP/S](#https)
			- [HTTP-400](#http-400)
				- [Arten von HTTP-400](#arten-von-http-400)
			- [HTTP-500](#http-500)
				- [Arten von HTTP-500](#arten-von-http-500)
- [Objektorientierung](#objektorientierung)
	- [Interfaces](#interfaces)
		- [Deklaration](#deklaration)
		- [Beispiel](#beispiel)
		- [Namenskonventionen](#namenskonventionen)
	- [Abstraktion](#abstraktion)
		- [Programmiersprachen](#programmiersprachen)
		- [Abstraktion in der objektorientierten Programmierung](#abstraktion-in-der-objektorientierten-programmierung)
		- [Abstraktion Beispiel (Java)](#abstraktion-beispiel-java)
	- [Polymorphie](#polymorphie)
		- [Polymorphie von Operatoren](#polymorphie-von-operatoren)
		- [Polymorphie in der Objektorientierten Programmierung](#polymorphie-in-der-objektorientierten-programmierung)
		- [Beispiel Polymorphie](#beispiel-polymorphie)

# Web Entwicklung

## Auszeichnungssprachen

### HTML - Hypertext Markup Language
[^3]
HTML ist eine textbasierte Auszeichnungssprache zur Strukturierung elektronischer Dokumente wie Texte mit Hyperlinks, Bilder und anderen Inhalten. HTML-Dokumente sind die Grundlage des WWW (World-Wide-Web) und werden von Webbrowsern dargestellt. 

Anders als einige Leute behaupten ist HTML **KEINE** Programmmiersprache.
HTML kann Merkmale einer Programmiersprache wie **Variablen** und **Kontrollstukturen** nicht auweisen.

#### DOM - Document Object Model
[^4]
Document Object Model

- meist HTML
- kann aber auch XML oder XHTML sein
- Das DOM stellt eine Baumstruktur dar, in der jedes Element des Dokumentes als Knoten im Baum repräsentiert wird.

## Protokolle

### HTTP/S
[^1] [^2]
- Hyper Text Transport Protocol
- Secure Hyper Text Transport Protocol

#### HTTP-400
HTTP Response Code 400 bezieht sich auf Client fehler

##### Arten von HTTP-400
- 400 Bad Request
    - Der Server kann oder will die Anfrage nicht bearbeiten wegen eines vermeidlichen Client Errors (Request falsch, Syntax falsch, Inhalt zu groß etc.)
- 403 Forbidden
    - Die Anfrage hat Daten enthalten die vom Server zwar verstanden wurde aber nicht verarbeitet wird (Eintrag doppelt)
- 404 Not Found
    - Die Angefragte Resource konnte nicht gefunden werden

#### HTTP-500
HTTP Response Code 500 bezieht sich auf Server fehler

##### Arten von HTTP-500
- 500 Internal Server Error
    - Eine generische Fehlermeldung welche gegeben wird wenn etwas unerwartetes passiert ist
- 502 Bad Gateway
    - Der Server fungierte als Gateway oder Proxy und erhielt eine ungültige Antwort
- 503 Service Unavailable
    - Der Server kann die Anfrage nicht verarbeiten (zu viele Anfragen, down for maintanance)

# Objektorientierung

## Interfaces
Ein Interface oder auch Schnittstelle definiert in der objektorientierte Programmierung, welche Methoden in den unterschiedlichen Klassen u. Ä vorhanden sind oder sein müssen.  
Eine Schnittstelle gibt an, welche Methoden vorhanden sind oder vorhanden sein müssen.  
Schnittstellen stellen eine Garantie über die in einer Klasse vorhandenen Methoden dar. Sie geben an, dass alle Objekte, die diese Schnittstellen besitzen, gleich behandelt werden können.

In Programmiersprachen die keine Mehrfachvererbung untestützen wie z.B. Java, können Schnittstellen verwendet werden, um Kompatibilitäten zwischen Klassen zu definieren, die nicht voneinander erben.

### Deklaration
Andere Programmiersprachen, die Mehrfachvererbung unterstützen, zum Beispiel C++, kennen zwar das Konzept von Schnittstellen, behandeln diese aber wie gewöhnliche Klassen. Man spricht dann auch von abstrakten Klassen. Manchmal wird auch eine eigene Sprache (eine sogenannte Schnittstellenbeschreibungssprache, IDL) zur Deklaration der Schnittstelle verwendet – meist ist das bei Middleware-Systemen wie CORBA oder DCOM der Fall. Objektbasierte Sprachen ohne strenge Typisierung kennen meist keine Schnittstellen.

### Beispiel
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
			points[i] = new PointF((float) (cosine * (point.X - x) - sine * (point.Y - y) + x), (float) (sine * (point.X - x) + cosine * (point.Y - y) + y));
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

### Namenskonventionen
In einigen Programmiersprachen ist es üblich, Schnittstellen durch besondere Präfixe oder Suffixe erkennbar zu machen. So wird häufig ein "I" oder ein "IF" angehängt.  
Im oben aufgeführtem Beispiel wäre dies ein "I" für "IFace". Dies wird normalerweise bei C# angewandt.

## Abstraktion
[^6]
Der Begriff Abstraktion wird in der Informatik häufig eingesetzt und beschreibt die Trennung zwischen **Konzept** und **Umsetzung**.  

### Programmiersprachen
Unterschiedliche Programmiersprachen bieten unterschiedliche Möglichkeiten von Abstraktion, wie zum Beispiel:
- In Objektorientierten Sprachen wie C++, Object Pascal oder Java, wurde das Konzept der Abstraktion in Form einer eigenen deklarativen Anweisung umgesetzt. Nach einer derartigen Deklaration ist es die Aufgabe des Programmierers, eine Klasse zu implementieren, um eine Instanz eines Objektes davon erzeugen zu können.

### Abstraktion in der objektorientierten Programmierung
In der objektorientierten Programmierung repräsentieren Objekte die abstrakten „Akteure“, die Arbeiten verrichten, ihren Zustand verändern und mit anderen Objekten im System kommunizieren können. Dabei werden die detaillierten Informationen über den genauen Zustand des Objektes oft verborgen, was auch als Information Hiding oder Kapselung bezeichnet wird. Hier werden Details verborgen, um das Problem nicht zu komplex zu gestalten. 

Eine weiter Form der Abstraktion ist die Polymorphie. Diese Vielgestaltigkeit erlaubt es, Objekte unterschiedlicher Typen miteinander auszutauschen. Auch die Vererbung von Klassen ist in einer Form eine Abstraktion, die es ermöglicht, ein komplexes Gebilde von Realationen abzubilden.

Verschiedene Programmiersprachen bieten vergleichbaren Konzepte der Abstraktion. Das Ziel bei allen ist es die Vielgestaltigkeit in der Objektorientierten Programmierung zu unterstützen.

### Abstraktion Beispiel (Java)
```java
public class Tier
{
     private double energieReserven;

     public boolean istHungrig() {
         return energieReserven < 2.5;
     }
     public void essen(Futter futter) {
         // Futter essen
         energieReserven += futter.getKalorien();
     }
}
```

Mit diesem Code können Objekte vom Typen "Tier" erstellt werden.
```java
schwein = new Tier();
if(schwein.istHungrig()){
	schwein.essen(essensreste);
}

kuh = new Tier();
if(kuh.istHungrig()){
	kuh.essen(gras);
}
```

In diesem Beispiel stellt die Klasse Tier eine Abstraktion dar und wird an Stelle von tatsächlichen Tieren verwendet. 

## Polymorphie
[^7]
Polymorphie oder Polymorphismus (griechisch für Vielgestaltigkeit | Poly = Viel, Morph = Form) ist ein Konzept in der Objektorientierten Programmierung, welches es uns ermöglicht einen Bezeichner abhängig von seiner Verwendung Objekte unterschiedlichen Datentyps annimmt. 

### Polymorphie von Operatoren
Ein Operator wie z.B. ein + oder - kann mehrmals mit anderen bedeutungen verwendet werden. Einersatz lassen sich hiermit Integer addieren oder subtrahieren, jedoch lassen sich auch Strings hiermit einander verketten.

### Polymorphie in der Objektorientierten Programmierung
Polymorphie tritt in der Objektorientierten Programmierung immer in Zusammenhang mit Vererbung und [Schnittstellen](#interfaces) auf.

Gibt es mehrere Methoden auf unterschiedlicher Hierarchischen Ebenen mit gleicher Signatur, wird zur Laufzeit bestimmt welche der Methoden für ein gegebenes Objekt verwendet wird (**Dynamisches Binden**). 

### Beispiel Polymorphie
```c#
class Fahrzeug
{
    public virtual void Beschleunigen()
    {
        Console.WriteLine("Das Fahrzeug beschleunigt.");
    }
}

// Abgeleitete Klasse 1
class Auto : Fahrzeug
{
    public override void Beschleunigen()
    {
        Console.WriteLine("Das Auto beschleunigt schnell.");
    }
}

// Abgeleitete Klasse 2
class Fahrrad : Fahrzeug
{
    public override void Beschleunigen()
    {
        Console.WriteLine("Das Fahrrad beschleunigt langsam.");
    }
}

class Program
{
    static void Main(string[] args)
    {
        Fahrzeug fahrzeug1 = new Auto();
        Fahrzeug fahrzeug2 = new Fahrrad();

        fahrzeug1.Beschleunigen(); // Aufruf der überschriebenen Methode in der Auto-Klasse
        fahrzeug2.Beschleunigen(); // Aufruf der überschriebenen Methode in der Fahrrad-Klasse
    }
}
```

[^1]: https://de.wikipedia.org/wiki/HTTP-Statuscode
[^2]: https://de.wikipedia.org/wiki/Hypertext_Transfer_Protocol
[^3]: https://de.wikipedia.org/wiki/Hypertext_Markup_Language
[^4]: https://de.wikipedia.org/wiki/Document_Object_Model
[^5]: https://de.wikipedia.org/wiki/Schnittstelle_(Objektorientierung)
[^6]: https://de.wikipedia.org/wiki/Abstraktion_(Informatik)
[^7]: https://de.wikipedia.org/wiki/Polymorphie_(Programmierung)