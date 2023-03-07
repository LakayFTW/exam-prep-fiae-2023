# Netzwerk und Hardware
## Software und Hardware Raid
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
- Preamble: 7 Bytes
- Start Frame Delimiter (SFD): 1 Byte
- Destination Address (DA): 6 Bytes [MAC]
- Source Address (SA): 6 Bytes [MAC]
- Type/Length: 2 Bytes
- Payload: 46 - 1.500 Bytes
- Frame Check Sequence: 4 Bytes

### MAC-Adressen
Eine MAC-Adresse (Media Access Control Address) ist ein eindeutiger Identifier welcher zu einem Netzwerk Controller (Network Interface Controller [NIC]) zugewiesen wird. Eine MAC Adresse ist 48-bit lang

### IPv4
IP-Adressen können in dezimal, binär, oktal und hexadezimal sowohl in der Punkt-, als auch in der Nichtpunktnotation dargestellt werden

IPv4 benutzt 32-Bit-Adressen. IPv4-Adressen werden üblicherweise dezimal in vier Blöcken geschrieben, zum Beispiel 207.142.131.235. Ein Block darf nicht mit einer 0 führen. Jedes Oktett representiert 8 Bit und somit ist eine Reichweite von 0 bis 255 möglich.