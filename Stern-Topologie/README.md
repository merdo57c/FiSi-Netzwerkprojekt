# Stern-Topologie

## Aufbau

Alle Geräte hängen mit einem eigenen Kabel an einem zentralen Switch (2960-24TT).
Anders als beim Hub leitet der Switch Pakete nur an den Port weiter, an dem das Zielgerät hängt.
Diese Topologie wird direkt mit Packet Tracer nachgebildet, es ist also keine Ersatzsimulation nötig.

## Geräte

- 1 × Switch 2960-24TT (Switch0)
- 4 × PC-PT (PC0, PC1, PC2, PC3)
- 2 × Printer-PT (Printer0, Printer1)
- Verbindungen: Copper Straight-Through

## IP-Adressplan

| Gerät     | IP-Adresse     | Subnetzmaske  |
|-----------|----------------|---------------|
| PC0       | 192.168.20.1   | 255.255.255.0 |
| PC1       | 192.168.20.2   | 255.255.255.0 |
| PC2       | 192.168.20.3   | 255.255.255.0 |
| PC3       | 192.168.20.4   | 255.255.255.0 |
| Printer0  | 192.168.20.5   | 255.255.255.0 |
| Printer1  | 192.168.20.6   | 255.255.255.0 |

## Tests

| Test                | Gesendet | Empfangen | Verlust |
|---------------------|----------|-----------|---------|
| PC0 → PC1           | 4        | 4         | 0 %     |
| PC0 → PC2           | 4        | 4         | 0 %     |
| PC0 → PC3           | 4        | 4         | 0 %     |
| PC0 → Printer0      | 4        | 4         | 0 %     |
| PC0 → Printer1      | 4        | 4         | 0 %     |

## Ausfall-Test

Das Kabel zu PC1 wurde getrennt.
Ping von PC0 an PC1 im ersten Lauf: 3 × „Request timed out“, danach 1 Antwort, sobald das Kabel wieder verbunden war.
Ergebnis: 1 von 4 Paketen empfangen (75 % Verlust).
Nach dem Wiederverbinden: 4 von 4 Paketen empfangen (0 % Verlust).

## Fehleranalyse

Noch nicht vollständig. Der Ausfall-Test zeigt, dass nur das getrennte Gerät betroffen ist.

## Meine Lernerkenntnisse

_Hier deine eigenen Erkenntnisse ergänzen._
