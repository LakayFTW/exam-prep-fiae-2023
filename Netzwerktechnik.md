# Table of Content
- [Table of Content](#table-of-content)
- [Netzwerk und Hardware](#netzwerk-und-hardware)
  - [Software und Hardware Raid](#software-und-hardware-raid)
    - [Hardware Raid Vorteile](#hardware-raid-vorteile)
    - [Hardware Raid Nachteile](#hardware-raid-nachteile)
    - [Software Raid Vorteile](#software-raid-vorteile)
    - [Software Raid Nachteile](#software-raid-nachteile)
  - [Verschiedene Raid Stufen](#verschiedene-raid-stufen)
    - [Raid 0: Striping - Beschleunigung ohne Redundanz](#raid-0-striping---beschleunigung-ohne-redundanz)
    - [Raid 1: Mirroring - Spiegelung](#raid-1-mirroring---spiegelung)
    - [Raid 5: Leistung + Parität, Block-Level Striping mit verteilter Paritätsinformation](#raid-5-leistung--parität-block-level-striping-mit-verteilter-paritätsinformation)
    - [Raid 01: Verbundsraid (Raid 1 über mehrere Raid 0)](#raid-01-verbundsraid-raid-1-über-mehrere-raid-0)
    - [Raid 10: Verbundsraid (Raid 0 über mehrere Raid 1)](#raid-10-verbundsraid-raid-0-über-mehrere-raid-1)
  - [Speichersysteme](#speichersysteme)
    - [SAN (Storage Area Network)](#san-storage-area-network)
    - [NAS (Network Attached Storaged)](#nas-network-attached-storaged)
  - [Ethernet und MAC-Adressen](#ethernet-und-mac-adressen)
    - [Ethernet-Frame (In Reihenfolge links rechts)](#ethernet-frame-in-reihenfolge-links-rechts)
    - [MAC-Adressen](#mac-adressen)
    - [IPv4](#ipv4)

---
<br>

# Netzwerk und Hardware
## Software und Hardware Raid
[^1]
### Hardware Raid Vorteile
- Der Datenzugriff bei Hardware Raids ist meist schneller
- Der Controller verwaltet die Festplatten unabhängig vom zugehörigen Computer und muss keine Rechenleistung in Anspruch nehmen.
- Es ist einfach eine kaputte Platte zu tauschen

### Hardware Raid Nachteile
- Teurer als Software Raid
- Kompatibilitätsprobleme mit einigen Betriebssystemen
- Bei der Verwendung anderer Technologien wie z.B. SSDs können Leistungsprobleme auftreten

### Software Raid Vorteile
- Billiger als Hardware Raid weil kein Controller benötigt wird
- Der (Software)Controller verwaltet Festplatten als Teil des zugehörigen Controllers
- Software Raids können in einem Betriebssystem implementiert werden und auf mehreren Geräten verwendet werden.

### Software Raid Nachteile
- Datenzugriff kann im Vergleich zu Hardware Raid langsamer sein
- Angeschlossene Geräte müssen mit dem Betriebssystem kompatible sein
- Eine Platte zu tauschen ist aufwändiger da der Software erst gesagt werden muss den Raid Controller auszuschalten

## Verschiedene Raid Stufen
[^2]
### Raid 0: Striping - Beschleunigung ohne Redundanz

### Raid 1: Mirroring - Spiegelung

### Raid 5: Leistung + Parität, Block-Level Striping mit verteilter Paritätsinformation

### Raid 01: Verbundsraid (Raid 1 über mehrere Raid 0)
### Raid 10: Verbundsraid (Raid 0 über mehrere Raid 1)
---
## Speichersysteme
### SAN (Storage Area Network)
- Ein SAN ist ein Netzwerkspeicher mit dem man über mehrere Clients zugreifen kann

### NAS (Network Attached Storaged)
- Ein NAS ist ein Speichermedium welches im Lokalen Netzwerk liegt und man mit berechtigten Geräten Daten über das Lokale Netzwerk legen kann.

---
## Ethernet und MAC-Adressen
### Ethernet-Frame (In Reihenfolge links rechts)
[^3]
- Preamble: 7 Bytes
- Start Frame Delimiter (SFD): 1 Byte
- Destination Address (DA): 6 Bytes [MAC]
- Source Address (SA): 6 Bytes [MAC]
- Type/Length: 2 Bytes
- Payload: 46 - 1.500 Bytes
- Frame Check Sequence: 4 Bytes

### MAC-Adressen
[^4]<br>
Eine MAC-Adresse (Media Access Control Address) ist ein eindeutiger Identifier welcher zu einem Netzwerk Controller (Network Interface Controller [NIC]) zugewiesen wird. Eine MAC Adresse ist 48-bit lang

### IPv4
[^5]<br>
IP-Adressen können in dezimal, binär, oktal und hexadezimal sowohl in der Punkt-, als auch in der Nichtpunktnotation dargestellt werden

IPv4 benutzt 32-Bit-Adressen. IPv4-Adressen werden üblicherweise dezimal in vier Blöcken geschrieben, zum Beispiel 207.142.131.235. Ein Block darf nicht mit einer 0 führen. Jedes Oktett representiert 8 Bit und somit ist eine Reichweite von 0 bis 255 möglich.

[^1]: https://www.techtarget.com/searchstorage/tip/Key-differences-in-software-RAID-vs-hardware-RAID
[^2]: https://de.wikipedia.org/wiki/RAID
[^3]: https://en.wikipedia.org/wiki/Ethernet_frame
[^4]: https://en.wikipedia.org/wiki/MAC_address
[^5]: https://de.wikipedia.org/wiki/IPv4