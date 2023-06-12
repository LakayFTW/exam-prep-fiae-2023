# Table of Content
- [Table of Content](#table-of-content)
- [Software und Hardware Raid](#software-und-hardware-raid)
  - [Hardware Raid Vorteile](#hardware-raid-vorteile)
  - [Hardware Raid Nachteile](#hardware-raid-nachteile)
  - [Software Raid Vorteile](#software-raid-vorteile)
  - [Software Raid Nachteile](#software-raid-nachteile)
  - [Host Raid](#host-raid)
  - [Verschiedene Raid Stufen](#verschiedene-raid-stufen)
    - [RAID 0: Striping - Beschleunigung ohne Redundanz](#raid-0-striping---beschleunigung-ohne-redundanz)
      - [Vorteile](#vorteile)
      - [Nachteile](#nachteile)
      - [Anwendung](#anwendung)
    - [RAID 1: Mirroring - Spiegelung](#raid-1-mirroring---spiegelung)
      - [Vorteile](#vorteile-1)
      - [Nachteile](#nachteile-1)
      - [Anwendung](#anwendung-1)
    - [RAID 5: Leistung + Parität, Block-Level Striping mit verteilter Paritätsinformation](#raid-5-leistung--parität-block-level-striping-mit-verteilter-paritätsinformation)
      - [Vorteile](#vorteile-2)
      - [Nachteile](#nachteile-2)
      - [Anwendung](#anwendung-2)
    - [RAID 01: Verbundsraid (Raid 1 über mehrere Raid 0)](#raid-01-verbundsraid-raid-1-über-mehrere-raid-0)
    - [RAID 10: Verbundsraid (Raid 0 über mehrere Raid 1)](#raid-10-verbundsraid-raid-0-über-mehrere-raid-1)
- [Speichersysteme](#speichersysteme)
  - [SAN (Storage Area Network)](#san-storage-area-network)
  - [NAS (Network Attached Storaged)](#nas-network-attached-storaged)
- [Ethernet und MAC-Adressen](#ethernet-und-mac-adressen)
  - [Ethernet-Frame (In Reihenfolge links rechts)](#ethernet-frame-in-reihenfolge-links-rechts)
  - [MAC-Adressen](#mac-adressen)
    - [Syntax](#syntax)
  - [IPv4](#ipv4)
    - [Adressformat](#adressformat)
    - [Private IP-Adressen](#private-ip-adressen)
      - [Adressbereiche:](#adressbereiche)
    - [Funktionsweise](#funktionsweise)
- [DHCP](#dhcp)
  - [Konzept](#konzept)
  - [DHCP-Server](#dhcp-server)
    - [Statische Zuordnung](#statische-zuordnung)
      - [Vorteil](#vorteil)
      - [Nachteil](#nachteil)
    - [Automatische Zuordnung](#automatische-zuordnung)
      - [Vorteil](#vorteil-1)
      - [Nachteil](#nachteil-1)
    - [Dynamische Zuordnung](#dynamische-zuordnung)
  - [DHCP-Nachrichten](#dhcp-nachrichten)
  - [Mögliche Zuweisung / Einstellung die ein DHCP dem Client zuweisen kann](#mögliche-zuweisung--einstellung-die-ein-dhcp-dem-client-zuweisen-kann)
  - [Einsatzbereiche](#einsatzbereiche)
- [Firewall](#firewall)
- [VPN (Virtual Private Network)](#vpn-virtual-private-network)
  - [Eigentschaften von VPN](#eigentschaften-von-vpn)
  - [OSI-Layer, auf dem die Kommunikation des VPN realisiert ist](#osi-layer-auf-dem-die-kommunikation-des-vpn-realisiert-ist)
  - [Anwendungsbereiche für VPN](#anwendungsbereiche-für-vpn)
  - [Ist ein VPN sicher? Nein! Welche Maßnahmen können den VPN-Tunnel sicher machen?](#ist-ein-vpn-sicher-nein-welche-maßnahmen-können-den-vpn-tunnel-sicher-machen)

---
<br>

# Software und Hardware Raid
[^1]
## Hardware Raid Vorteile
- Der Datenzugriff bei Hardware Raids ist meist schneller
- Der Controller verwaltet die Festplatten unabhängig vom zugehörigen Computer und muss keine Rechenleistung in Anspruch nehmen.
- Es ist einfach eine kaputte Platte zu tauschen

## Hardware Raid Nachteile
- Teurer als Software Raid
- Kompatibilitätsprobleme mit einigen Betriebssystemen
- Bei der Verwendung anderer Technologien wie z.B. SSDs können Leistungsprobleme auftreten

## Software Raid Vorteile
- Billiger als Hardware Raid weil kein Controller benötigt wird
- Der (Software)Controller verwaltet Festplatten als Teil des zugehörigen Controllers
- Software Raids können in einem Betriebssystem implementiert werden und auf mehreren Geräten verwendet werden.

## Software Raid Nachteile
- Datenzugriff kann im Vergleich zu Hardware Raid langsamer sein
- Angeschlossene Geräte müssen mit dem Betriebssystem kompatible sein
- Eine Platte zu tauschen ist aufwändiger da der Software erst gesagt werden muss den Raid Controller auszuschalten

## Host Raid
Host Raid ist eine Zwischenstufe von Hard- und Software-RAID.
Hier werden Chipsätze, die sich auf dem Mainboard befinden oder günstige RAID-Adapter verwendet.
Mainbords mit RAID-Funktion beherrschen meist nur RAID 0, 1 und teurere Varianten möglicherweise noch RAID 5.
Man spricht von Host-RAID, da die RAID-Funktionen von der Firmware bzw. den Treibern erledigt werden.

## Verschiedene Raid Stufen
[^2]
### RAID 0: Striping - Beschleunigung ohne Redundanz
Die Null in RAID 0 steht für die Null-Daten-Redundanz. Daher gehört RAID 0 eigentlich nicht zu den RAID-Systemen, da es eher ein schnelles Array of Independent Disks ist. Hier bei werden zwei oder mehrere Platten zu einem großen logischen Laufwerk zusammengeschaltet. Hier werden die Daten meist in Blöcke der Größe 64 oder 128 kB (Stripe = Streifen) unterteilt, daher kommt auch die Bezeichnung Striping.
Bei RAID 0 empfielt es sich zwei gleich große Platten zu verwenden, da sich die Gesamtgröße des RAID nach der kleinsten Platte mal Anzahl der Platten richtet.

#### Vorteile
- Steigerung des Datendurchsatzes, da die Platten-Zugriffe in höherem Maße parallel ablaufen.
- Gilt aber nur bei sequenziellem Datentransfer.

#### Nachteile
- Fällt eine Platte aus, so sind die Daten nutzlos, denn von jeder gespeicherten Datei ist nur noch die Hälfte lesbar.
- Fehlt ein Teil einer Datei, so kann der Rest nicht wiederhergestellt werden, somit wird in RAID 0 keine Datensicherung gewährleistet.
- Die Ausfallsicherheit liegt höher als bei einer einzelnen Platte, d.H. sie steigt mit jeder zusätzlichen Platte.
- Für den Klassischen Server-Betrieb ungeeignet.

#### Anwendung
- Wenn besonders große Datenmengen in kurzer Zeit gelesen werden soll und die Datensicherheit irrelevant ist.
- Für temporäre Dateien, wie die Windows-Auslagerungsdatei oder Swap-Funktion von Linux.

Darstellung Raid 0:<br>
<a href="https://de.wikipedia.org/wiki/RAID">
  <img title="RAID 0" src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/RAID_0.svg/220px-RAID_0.svg.png" width="200">
</a>

### RAID 1: Mirroring - Spiegelung
RAID 1 ist der Verbund von zwei Platte, wobei auf allen Festplatten die gleichen Daten gespeichert werden (Spiegelung). Somit ist volle Redundanz geboten.
Die Platten müssen paarweise vorhanden sein und die Kapazität richtet sich auch hier nach der kleinsten Platte. Beim Bescheiben ist das RAID nur so schnell wie die langsamste Platte.

#### Vorteile
- Bei Ausfall einer Platte kann ohne Daten- und mit geringen Geschwindigkeitsverlust weiter gearbeitet werden.
- Das bietet eine hohe Ausfall- und Datensicherheit.
- Ein RAID 1-System kann beim Lesen auf mehr als einer Platte zugreifen und gleichzeitig verschiedene Sektoren von verschiedenen Platten einlesen, was die Leseleistung erhöht.

#### Nachteile
- Keine richtige Steigerung des Datendurchsatzes.
- Es entsteht keine Datensicherung, da z.B. versehentliche oder fehlerhafte Schreiboperationen auf allen Platten genutzt werden.
- Das Setup ist teuer, da immer der doppelte Preis gezahlt werden muss bei einfacher Speicherung.
- Zwei Platten mit 500GB ergeben zwar 1TB aber da RAID 1 die Daten spiegelt, steht nur die Hälfte zur Verfügung.

#### Anwendung
- Eher für kleine Server, da man große Datenmengen besser mit höheren RAID-Leveln speichert.

Darstellung RAID 1:<br>
<a href="https://de.wikipedia.org/wiki/RAID">
  <img title="RAID 1" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b7/RAID_1.svg/220px-RAID_1.svg.png" width="200">
</a>

### RAID 5: Leistung + Parität, Block-Level Striping mit verteilter Paritätsinformation
Wie bei RAID 0 werden die Daten in Blöcke (Stripesets) zerlegt. Zusätzlich wird ein Bereich auf jeder Platte für Prüfnummern (Parity) verwendet, damit nachträglich Fehler beseitigt werden können. Die Parity wird mithilfe einer XOR-Operation bitweise berechnet. Dabei werden Datenblöcke von 64kB geteilt und aus diesen beiden Blöcken wird die Parity-Info gebildet, also einem dritten Block von 64kB. Für diese Art von RAID werden 3 Festplatten benötigt.
RAID 5 anders als bei RAID 4 speichert die Parity-Bits und die Teil-Infos auf allen drei Platten verteilt.

#### Vorteile
- Steigerung des Datendurchsatzes
- Datensicherheit
- Relativ geringe Kosten (Dennoch: Es werden mindestens 3 Platten benötigt)
- Bei Ausfall einer Platte können die Daten während des Betriebes dank der Paritätsinfo wiederhergestellt werden.

#### Nachteile
- Es darf nicht mehr als eine Platte ausfallen, da die Daten sonst verloren sind.
- Schreibgeschwindigkeit ist geringer, da vor jedem Schreibzugriff erst die Paritätsinfo ausgelesen und danach neu erstellt werden müssen.
- Kapazitätsverlust durch die Speicherung von Paritätsinfos. Bei einer Plattengröße von 500GB und drei Platten, hätte man 1,5TB - 500GB = 1TB Speicher.

#### Anwendung
- Für große Datenmengen mit kleinen Dateien, wegen der geringeren Schreibgeschwindigkeit.

Darstellung RAID 5:<br>
<a href="https://de.wikipedia.org/wiki/RAID">
  <img title="RAID 5" src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/RAID_5.svg/220px-RAID_5.svg.png" width="200">
</a>

### RAID 01: Verbundsraid (Raid 1 über mehrere Raid 0)
RAID 01 ist eine Kombination aus RAID 0 und 1, also Striping und Mirroring. Es sind mindestens drei Festplatten erforderlich. Die Daten werden in Blöcke (Stripesets) zerlegt und dann auf mehrere RAID 0 verteilt, somit werden die Eigenschaften Sicherheit und höherer Datendurchsatz kombiniert.

Darstellung RAID 01<br>
<a href="https://de.wikipedia.org/wiki/RAID">
  <img title="RAOD 01" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/RAID_01.svg/220px-RAID_01.svg.png" width="200">
</a>

### RAID 10: Verbundsraid (Raid 0 über mehrere Raid 1)
RAID 10 ist eine kombination aus RAID 1 und 0. Hier sind mindestens 4 Platten erforderlich. Es werden die Daten vom RAID-Controller zuerst gespiegelt und danach auf zwei RAID 1 gespeichert. Diese werden dann auf ein RAID 0 zusammengefasst. Das erhöht die Sicherheit der Daten (höher als bei RAID 01) und die Sicherheit des Datendurchsatzes.
RAID 10 ist besonders geeignet um größere Datenmengen redundant zu speichern.

Darstellung RAID 10:<br>
<a href="https://de.wikipedia.org/wiki/RAID">
  <img title="RAID 10" src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/bb/RAID_10.svg/170px-RAID_10.svg.png" width="200">
</a>

---
# Speichersysteme
## SAN (Storage Area Network)
- Ein SAN ist ein Netzwerkspeicher mit dem man über mehrere Clients zugreifen kann

## NAS (Network Attached Storaged)
- Ein NAS ist ein Speichermedium welches im Lokalen Netzwerk liegt und man mit berechtigten Geräten Daten über das Lokale Netzwerk legen kann.

---
# Ethernet und MAC-Adressen
## Ethernet-Frame (In Reihenfolge links rechts)
[^3]
- Preamble: 7 Bytes
- Start Frame Delimiter (SFD): 1 Byte
- Destination Address (DA): 6 Bytes [MAC]
- Source Address (SA): 6 Bytes [MAC]
- Type/Length: 2 Bytes
- Payload: 46 - 1.500 Bytes
- Frame Check Sequence: 4 Bytes

## MAC-Adressen
[^4]<br>
Eine MAC-Adresse (Media Access Control Address) ist ein eindeutiger Identifier welcher zu einem Netzwerk Controller (Network Interface Controller [NIC]) zugewiesen wird. Eine MAC Adresse ist 48-bit lang. Die MAC-Adresse wird auch als physische Adresse bezeichnet, weil er teilweise vom Hersteller in ein Gerät fest und nicht veränderbar einprogrammiert wird.

### Syntax
Im Falle von Ethernet-Netzen besteht die MAC-Adresse aus 48 Bit bzw. sechs Bytes. Die Adresse wird in hexadezimal geschrieben. Üblich ist eine byteweise schreibweise, wobei die einzelnen Bytes durch Bindestriche oder Doppelpunkte getrennt werden. z.B.<br>
- `00-80-41-ae-fd-7e`
- `008041-aefd7e` oder
- `00:80:41:ae:fd:7e`

## IPv4
[^5]<br>
IP-Adressen können in dezimal, binär, oktal und hexadezimal sowohl in der Punkt-, als auch in der Nichtpunktnotation dargestellt werden

IPv4 benutzt 32-Bit-Adressen. IPv4-Adressen werden üblicherweise dezimal in vier Blöcken geschrieben, zum Beispiel 207.142.131.235. Ein Block darf nicht mit einer 0 führen. Jedes Oktett representiert 8 Bit und somit ist eine Reichweite von 0 bis 255 möglich.

### Adressformat
IP-Adressen bestehen aus einem Netzanteil und einem Hostanteil. Der Netzteil definiert ein Teilnetz, der Hostteil definiert ein Gerät (Host) innerhalb eines Teilnetzes.

Beispiel:
||dezimal|||binär||
|---|---|---|---|---|---|
|IP-Adresse|192.168.0|.23| -> |11000000.10101000.00000000 |.00010111|
|Subnetzmaske|255.255.255|.0| -> |11111111.11111111.11111111|.00000000|
||Netzanteil|Hostanteil||Netzanteil|Hostanteil|

Die Subnetzmaske sorgt für die genaue Aufteilung zwischen Netzanteil und Hostanteil. Eine Subnetzmaske definiert z.B. `255.255.255.0`. Bei Verwendung dieser Maske würde die IP-Adresse in der CIDR-Notation dann als `192.168.0.23/24` geschrieben, wobei die "24" bedeutet, dass die ersten 24 Bits der Subnetzmaske gleich "1" sind. Die Bits der Maske, die auf "1" sind, legen die Stellen der IP-Adresse fest, die zum Netzanteil gehören. Alle restlichen stellen, die dann auf "0" stehen, gehören dann zum Hostanteil.

Merke: Die Adressen `192.168.0.0` und `192.168.0.255` sind reserviert.<br>
`192.168.0.0`: Das Netzwerk selbst<br>
`192.168.0.255`: Die Broadcast Adresse<br>

### Private IP-Adressen
Private IP-Adressen gehören zu bestimmten IP-Bereichen, die im Internet nicht groutet werden. Sie können von jedem innerhalb privater Netze (z.B. LANs) genutzt werden.
Folgende Adressbereiche wurden aus dem öffentlichen Adressraum ausgespart für die private Nutzung.

#### Adressbereiche:
- Netzadressenbereich:
  - 10.0.0.0 bis 10.255.255.255
  - 172.16.0.0 bis 172.16.255.255
  - 192.168.0.0 bis 192.168.255.255
- Netzklassen:
  - Klasse A -> 1 privates Netz mit 16.777.216 Adressen (10.0.0.0/8)
  - Klasse B -> 16 private Netze mit jeweils 65.536 Adressen (172.16.0.0/16 bis 172.31.0.0/16)
  - Klasse C -> 256 private Netze mit jeweils 256 Adressen (192.168.0.0/24 bis 192.168.255.0/24)
- Anzahl Adressen:
  - $2^{24} = 16.777.216$
  - $2^{20} = 1.048.576$
  - $2^{16} = 65.536$

Somit hat man keinen unnützen administrativen Mehraufwand bei der Pflege lokaler Netzwerke.

### Funktionsweise
- PCs in einem Rechnernet, denen private IP-Adressen zugewiesen wurden, bilden ein Intranet und können nur untereinander kommunizieren. 
- Aus dem Internet heraus kann nicht auf das Intranet zugegriffen werden
- Internet-Router ignorieren die privaten Adressbereiche. 
- Um einen Internetzugang herzustellen muss ein Gateway oder Router im privaten Netz plaziert werden, der sowohl eine private als auch eine öffentliche IP-Adresse besitzt.
- Der genutzte private Adressbereich ist immer nur innerhalb des privaten Netzes sichtbar, womit die Adressen auch in anderen privaten Netzen vergeben werden können.

---
<br>

# DHCP
[^10]<br>
Das Dynamic Host Protocol (DHCP) ist ein Kommunikationsprotokoll. Durch einen Server können Clients die richtige Netzwerkkonfiguration erhalten.
DHCP ist eine Erweiterung des Bootstrap-Protokols (BOOTP)

Die Länge eines DHCP-Pakets beträgt 32 Bit.

DHCP ist in RFC 2131 und 2132 definiert.

## Konzept

Mit DHCP können Clients ohne manuelle Konfiguration der Netzwerkschnittstelle in ein bestehendes Netz aufgenommen werden. Informationen wie IP-Adresse, Subnetzmaske, Gateway und Name Server (DNS) sowie mögliche weitere Einstellungen werden automatisch vergeben.

## DHCP-Server
Der DHCP-Server wird wie alle gängigen Netzwerkdienste als Hintergrundprozess (Dienst oder Daemon) gestartet und wartet über UDP-Port 67 auf Anfragen von Clients.

Es gibt drei verschiedene Betriebsmodi eines DHCP-Servers:

### Statische Zuordnung
In diesem Modi lassen sich IP-Adressen einer bestimmten MAC-Adresse zuordnen. Die Adressen werden den MAC-Adressen auf unbestimmte Zeit zugeteilt. 

#### Vorteil
Eine statische Zuordnung kann dann von Vorteil sein, wenn Netzwerkdienste über eine bestimmte Adresse erreichbar sein sollen. Auch Portfreigaben von einem Router zu einem Client benötigen in der Regel eine feste IP-Adresse.

#### Nachteil
Dabei kann das Problem aufteten, dass keine weiteren Clients dem Netzwerk zugeteilt werden können, da alle Adressen fest vergeben sind. Das kann unter manchen Sicherheitsaspekten problematisch sein.

### Automatische Zuordnung
Bei der Automatischen Zuordnung werden am DHCP-Server Bereiche von IP-Adressen (range) definiert. Neue Cleints erhalten dabei IP-Adressen welche den MAC-Adressen zugeordnet werden, das wird in einer Tabelle festgehalten. Im Unterschied zur dynamischen Zuordung werden automatische Adressen fest vergeben und nicht entfernt. 

#### Vorteil
Der Vorteil darin liegt, dass IP-Adressen immer dem gleichen Host zugeordnet sind und keinem anderem Host zugeordnet werden können.

#### Nachteil
Der Nachteil darin besteht, dass neue Clients keine IP-Adresse erhalten wenn der gesamte Adressbereich bereits vergeben ist, auch wenn IP-Adressen nicht mehr aktiv genutzt werden.

### Dynamische Zuordnung
Die dynamische Zuordnung gleicht der automatischen Zuordnung, allerdings wird in der dynamischen Konfiguration festgelegt wie lange eine bestimmte IP-Adresse an einem Client vergeben werden darf. Nach dem Ablauf meldet sich der Client beim Server und beantragt eine "Verlängerung". Sollte sich der Client nicht melden, dann wird eine IP-Adresse frei und kann einem anderen (oder auch wieder dem selben) Client neu vergeben werden. Diese Zeit nennt man "Lease-Time" (Leihdauer).

Manche Konfigurationen vergeben IP-Adressen abhängig von der MAC-Adresse, das heißt auch nach langer Abstinenz kann eine IP-Adresse wieder an den gleichen Client vergeben werden, solange diese Adresse noch nicht neu vergeben wurde.

## DHCP-Nachrichten

- DHCP**DISCOVER**:
  - EIn Client ohne IP-Adresse sendet eine Broadcast-Anfrage nach Adress-Angeboten an alle DHCP-Server im lokalen Netz.
- DHCP**OFFER**:
  - Die DHCP-Server antworten mit entsprechenden Werten auf eine DHCP**DISCOVER**-Anfrage.
- DHCP**REQUEST**:
  - Der Client fordert eine der angebotenen IP-Adressen, weitere Daten sowie Verlängerung der Lease-Zeit von einem der antwortenden DHCP-Server.
- DHCP**ACK**:
  - Bestätigung des DHCP-Servers zu einer DHCP**REQUEST**-Anforderung durch den DHCP-Server.
- DHCP**NAK**:
  - Ablehnung einer DHCP**REQUEST**-Anforderung durch den DHCP-Server.
- DHCP**DECLINE**:
  - Ablehnung durch den Client, da die IP-Adresse schon verwendet wird.
- DHCP**RELEASE**:
  - Der Client gibt die eigene Konfiguration frei, damit die Parameter wieder für andere Clients zur Verfügung stehen.
- DHCP**INFORM**:
  - Anfrage eines Clients nach weiteren Konfigurationsparametern, z.B. weil der Client eine statische IP-Adresse benutzt.

## Mögliche Zuweisung / Einstellung die ein DHCP dem Client zuweisen kann
- IP-Adresse
- Subnetzmaske/Netzwerkmaske
- Default-Gateway
- Nameserver
- Proxy-Konfig via [WPAD](/Begriffe.md/#wpad-web-proxy-audodiscovery-protocol)
- Time- und NTP-Server
- DNS-Server, DNS Context und [DNS](/Begriffe.md/#dns-domain-name-system) Tree
- Sekundärer DNS-Server
- WINS-Server (für MS Windows Clients)

## Einsatzbereiche
- große Netzwerke mit häufigen Änderungen
- normale Anwender, die einfach nur eine Netzwerkverbindung haben wollen, ohne sich großartig mit Netzwerkkonfig auskennen zu müssen.

---
<br>

# Firewall
- Sicherheitsprobleme, wo gegen die Firewall keinen Schutz bietet?
- Filtertechnologien
  - Paketfilter
  - Stateful Packet Inspection
  - Proxyfilter
  - Contentfilter
- Firewallarten
  - Person Firewall (Desktop Firewall)
  - Externe Firewall (Netzwerk- oder Hardware Firewall)
- Firewalltechnologien
  - Paketfilter-Firewall
  - Stateful Inspection Firewall (SIF)
  - Firewall Router
  - Application Layer Firewall
  - Proxy-Firewall (Application Layer Firewall)

---
<br>

# VPN (Virtual Private Network)
VPNs sind Punkt-zu-Punkt verbindungen über ein privates oder ein öffentliches Netzwerk, z.B. über das Internet. Dabei werden die Verbindungen durch einen öffentlichen ISP (Internet Service Provider) bereitgestellt. Zur Übertragung im Internet wird ein sogenannter Tunnel erzeugt. Um einen virtuellen Anruf bei einem virtuellen Port auf einem VPN-Server zu tätigen, werden spezielle TCP/IP-basierte Protokolle, so genannte Tunnelprodukte verwendet.

## Eigentschaften von VPN
- Hohe flexibilität
- Niedrige Kosten für die Übertragung
- Kapselung
- Reines Softwareprodukt

## OSI-Layer, auf dem die Kommunikation des VPN realisiert ist
- VPN Tunneling kann man auf OSI-Schicht 2 oder OSI-Schicht 3 realisieren.
  - OSI-Schicht 2 (Sicherrungsschicht, Data Link Layer)
    - Vertreter des Layer-2-Tunneling sind die Protokolle PPTP (Point to Pont Tunneling Protocoll), L2F (Layer 2 Forwarding) und L2TP (Layer 2 Tunneling Protocol)
  - OSI-Schicht 3 (Vermittlungsschicht, Network Layer)
    - IPSec

## Anwendungsbereiche für VPN
- Remotezugriff
- Verbindung von Netzwerken
- Verbindung von PCs über ein Intranet zum Aufbau geschlossener Gruppen
- Firmennetzwerk

## Ist ein VPN sicher? Nein! Welche Maßnahmen können den VPN-Tunnel sicher machen?
- Identifikation
- Authentifikation
- Verschlüsselung der Daten zum Schutz vor unbefugten
- Firewall
- Verwendung von Tunneling Protokollen:
  - PPTP
  - L2TP
  - IPSec
  - SSTP


[^1]: https://www.techtarget.com/searchstorage/tip/Key-differences-in-software-RAID-vs-hardware-RAID
[^2]: https://de.wikipedia.org/wiki/RAID
[^3]: https://en.wikipedia.org/wiki/Ethernet_frame
[^4]: https://en.wikipedia.org/wiki/MAC_address
[^5]: https://de.wikipedia.org/wiki/IPv4
[^10]: https://de.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol