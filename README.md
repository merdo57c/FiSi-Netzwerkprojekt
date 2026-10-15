# FiSi-Netzwerkprojekt

Dieses Repository ist mein eigenständiges IT-Projekt im Rahmen meiner Bewerbung als Fachinformatiker für Systemintegration. Ich plane, simuliere, konfiguriere, teste und dokumentiere klassische Netzwerktopologien mit Cisco Packet Tracer. Ich wollte nicht nur theoretisch über Netzwerke lesen, sondern selbst ausprobieren, wie Geräte zusammenarbeiten und was passiert, wenn etwas nicht funktioniert.

## Motivation

Ich interessiere mich für die Technik hinter dem Internet und dafür, wie Unternehmen ihre Rechner, Server und Standorte miteinander verbinden. Die Ausbildung zum Fachinformatiker für Systemintegration passt zu dieser Neugier, weil sie genau dieses Zusammenspiel aus Planung, Aufbau und Betrieb umfasst.

Mit diesem Projekt möchte ich zeigen, dass ich mich selbstständig in ein technisches Thema einarbeiten kann: von der Theorie über die Planung und Konfiguration bis zur Fehlersuche und sauberen Dokumentation.

## Ziel des Projekts

Am Ende soll ein fiktives Firmennetzwerk mit mehreren Abteilungen und zwei Standorten stehen, das die einzelnen Topologien sinnvoll kombiniert. Dabei geht es mir weniger um die Menge der Geräte als um Verständnis: Jede Topologie soll so dokumentiert sein, dass ich ihren Aufbau, ihre Vor- und Nachteile und ihre Grenzen erklären kann.

## Glossar: Topologien

| Topologie | Kurzbeschreibung | Link |
|-----------|------------------|------|
| Punkt-zu-Punkt | Zwei Geräte sind direkt miteinander verbunden. Einfach, aber jede weitere Verbindung braucht eine eigene Leitung. | [Zum Ordner](Punkt-zu-Punkt-Topologie/) |
| Bus | Alle Geräte hängen an einer gemeinsamen Leitung. Wenig Kabel, aber ein Ausfall der Leitung betrifft das ganze Netz. | [Zum Ordner](Bus-Topologie/) |
| Stern | Alle Geräte sind mit einem zentralen Verteiler verbunden. Fällt ein Endgerät aus, bleibt der Rest erreichbar. Fällt der Verteiler aus, steht das Netz. | [Zum Ordner](Stern-Topologie/) |
| Ring | Die Geräte bilden einen geschlossenen Kreis, über den die Daten weitergereicht werden. Eine unterbrochene Strecke kann den Ring stören. | [Zum Ordner](Ring-Topologie/) |
| Baum | Mehrere Sterne sind hierarchisch verbunden, ähnlich einem Stammbaum. Gut erweiterbar, aber bei einem Ausfall im oberen Bereich sind viele Geräte betroffen. | folgt |
| Mesh | Geräte sind mehrfach untereinander verbunden. Vollständig vermascht bedeutet jeder mit jedem, teilweise vermascht nur einige Verbindungen. Hohe Ausfallsicherheit, aber viel Kabel. | folgt |
| Hybrid | Eine Kombination mehrerer Topologien, zum Beispiel Stern und Ring, um deren Vorteile zu verbinden. | folgt |
| Punkt-zu-Mehrpunkt | Ein zentrales Gerät verbindet sich mit mehreren Teilnehmern, zum Beispiel ein Access Point mit WLAN-Geräten. | folgt |
| Firmennetzwerk | Ein fiktives Unternehmen mit mehreren Abteilungen und zwei Standorten, das die einzelnen Topologien kombiniert. | folgt |
