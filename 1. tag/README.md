# M141 – DB-Systeme in Betrieb nehmen (Tag 1)

## Grundlagen

- **Datenbank (DB):** Strukturierte Datensammlung
- **DBMS:** Software zur Verwaltung von Datenbanken (z. B. MySQL, MariaDB)
- **Datenbank-System (DBS):** Kombination aus DBMS + Daten

## Architektur

- **Client/Server-Modell:**  
  - *Client:* GUI oder Tool, sendet SQL-Befehle  
  - *Server:* Verarbeitet SQL-Befehle, speichert Daten zentral

## Datenbanktypen

| Typ                  | Beispiel     | Nutzen                     |
|----------------------|--------------|----------------------------|
| Relational           | MySQL        | Tabellenbasiert, klassisch |
| Dokumentenorientiert | MongoDB      | JSON-ähnliche Strukturen   |
| Key-Value            | Redis        | Caching, Sessions          |
| Graph                | Neo4j        | Beziehungen, Netzwerke     |
| Time Series          | InfluxDB     | Zeitbasierte Daten         |

## Vergleich: MariaDB vs MySQL vs PostgreSQL

| Merkmal     | MariaDB  | MySQL    | PostgreSQL     |
|-------------|----------|----------|----------------|
| Lizenz      | Frei     | Teilweise kommerziell | Frei           |
| Performance | Gut bei OLAP | Gut bei OLTP | Gut bei Analysen |
| JSON-Support| Eingeschränkt | Gut      | Sehr gut       |

## Tools

- **XAMPP:** Lokale Umgebung mit MySQL, Apache, phpMyAdmin
- **phpMyAdmin:** Web-GUI zur Verwaltung von MySQL
- **MySQL Workbench:** GUI-Tool für Datenmodellierung und SQL

## MySQL starten (XAMPP)

- XAMPP öffnen und MySQL starten
- phpMyAdmin öffnen: `http://localhost/phpmyadmin`

## MySQL in der Kommandozeile

```bash
mysql -u root -p

---
