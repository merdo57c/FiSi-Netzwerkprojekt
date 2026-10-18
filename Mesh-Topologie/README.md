# Mesh-Topologie

![](/Screenshots/01-mesh_aufbau-mit-pcs.png)

## Theorie

Bei der Mesh-Topologie ist jedes Gerät mit mehreren anderen verbunden. Zwischen zwei Geräten gibt es dadurch mehrere Wege.

- **Vollständig vermascht:** Jedes Gerät ist direkt mit jedem anderen verbunden. Bei vier Geräten sind das 6 Verbindungen.
- **Teilweise vermascht:** Nur einige Geräte sind mehrfach verbunden.

**Vorteile:** Hohe Ausfallsicherheit, da oft ein Ersatzweg existiert.
**Nachteile:** Viel Kabel, hoher Aufwand bei Aufbau und Konfiguration.

## Ersatzsimulation

PCs besitzen nur einen Netzwerkanschluss und leiten keine fremden Pakete weiter. Deshalb wird das Mesh mit vier Switches nachgebildet, die vollständig untereinander verbunden sind. Die PCs hängen als Endgeräte an den Switches.

Da die Switches Schleifen bilden, blockiert das Spanning Tree Protocol (STP) einzelne Verbindungen. Dadurch sind nicht alle physischen Wege gleichzeitig aktiv.

## Geräte

- 4 × Switch 2960-24TT (Switch1 bis Switch4)
- 4 × PC-PT (PC1 bis PC4)
- 6 × Verbindungen zwischen den Switches (Copper Straight-Through)
- 4 × Anschlusskabel PC zu Switch (Copper Straight-Through, Fa0/4)

## Verbindungen zwischen den Switches

| Von     | Port  | Nach    | Port  |
|---------|-------|---------|-------|
| Switch1 | Fa0/1 | Switch2 | Fa0/1 |
| Switch1 | Fa0/2 | Switch3 | Fa0/1 |
| Switch1 | Fa0/3 | Switch4 | Fa0/1 |
| Switch2 | Fa0/2 | Switch3 | Fa0/2 |
| Switch2 | Fa0/3 | Switch4 | Fa0/2 |
| Switch3 | Fa0/3 | Switch4 | Fa0/3 |

_Hinweis: Die Portnummern habe ich aus der Planung übernommen. Bitte prüfe sie anhand deines Aufbaus und passe sie bei Abweichung an._

## IP-Adressplan

| Gerät | Angeschlossen an | IP-Adresse   | Subnetzmaske  |
|-------|------------------|--------------|---------------|
| PC1   | Switch1          | 192.168.40.1 | 255.255.255.0 |
| PC2   | Switch2          | 192.168.40.2 | 255.255.255.0 |
| PC3   | Switch3          | 192.168.40.3 | 255.255.255.0 |
| PC4   | Switch4          | 192.168.40.4 | 255.255.255.0 |

## Tests (Ping)

| Test      | Gesendet | Empfangen | Verlust |
|-----------|----------|-----------|---------|
| PC1 → PC2 | 4        | 4         | 0 %     |
| PC1 → PC3 | 4        | 4         | 0 %     |
| PC1 → PC4 | 4        | 4         | 0 %     |

## Spanning Tree

Im Aufbau sind drei der sechs Verbindungen blockiert. Die Blockierung ist im Bild mit orangen Punkten gekennzeichnet.

_Noch offen: Ausgabe von `show spanning-tree` zur Bestätigung._

## Ausfall-Test

_Noch offen: Eine Verbindung entfernen und prüfen, ob PC1 weiterhin PC2 erreicht._

## Fehleranalyse

_Noch offen._

## Meine Lernerkenntnisse

_Hier deine eigenen Erkenntnisse ergänzen._
