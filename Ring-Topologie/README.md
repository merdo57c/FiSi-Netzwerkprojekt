# Ring-Topologie

## Status

In Arbeit: Theorie und Planung abgeschlossen, Aufbau noch offen.

## Theorie

Bei der Ring-Topologie ist jedes Gerät mit genau zwei Nachbarn verbunden. Zusammen bilden sie einen geschlossenen Kreis. Daten werden von Gerät zu Gerät weitergereicht, bis sie beim Empfänger ankommen. Jedes Gerät prüft die Zieladresse und gibt das Paket an den nächsten Nachbarn weiter, wenn es nicht für es bestimmt ist.

- **Vorteile:** Kein zentraler Verteiler nötig, klarer Datenfluss.
- **Nachteile:** Fällt eine Verbindung aus, ist der Weg zwischen den Stationen unterbrochen. Jedes Gerät muss Pakete weiterreichen, dadurch können Verzögerungen entstehen.

## Ersatzsimulation

Ein Ring aus PCs ist in Packet Tracer nicht sauber umsetzbar, weil PCs nur einen Netzwerkanschluss haben und nicht als Weiterleitungspunkt dienen. Deshalb wird der Ring mit vier Switches nachgebildet, die im Kreis verbunden sind.

Physisch ist das ein Ring. Da die Switches eine Schleife bilden, blockiert das Spanning Tree Protocol (STP) einen Port, um eine Endlosschleife zu verhindern. Logisch wirkt das Netz dann wie eine Kette.

## Geräte

- 4 × Switch 2960-24TT (Switch0 bis Switch3)
- 4 × PC-PT (PC0 bis PC3), je einer an einem Switch
- Ring-Verbindungen: Copper Straight-Through (Fa0/1 und Fa0/2 der Switches)
- PC-Anschlüsse: Copper Straight-Through (Fa0/3)

## IP-Adressplan

| Gerät | IP-Adresse   | Subnetzmaske  |
|-------|--------------|---------------|
| PC0   | 192.168.30.1 | 255.255.255.0 |
| PC1   | 192.168.30.2 | 255.255.255.0 |
| PC2   | 192.168.30.3 | 255.255.255.0 |
| PC3   | 192.168.30.4 | 255.255.255.0 |

## Tests

_Noch nicht durchgeführt._ Geplant sind Ping-Tests zwischen allen PCs sowie ein Test mit einem unterbrochenen Ring-Kabel.

## Fehleranalyse

_Noch offen._

## Meine Lernerkenntnisse

_Hier deine eigenen Erkenntnisse ergänzen._
