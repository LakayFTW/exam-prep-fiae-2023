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

[^1]: https://de.wikipedia.org/wiki/HTTP-Statuscode
[^2]: https://de.wikipedia.org/wiki/Hypertext_Transfer_Protocol
[^3]: https://de.wikipedia.org/wiki/Hypertext_Markup_Language
[^4]: https://de.wikipedia.org/wiki/Document_Object_Model