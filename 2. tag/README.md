# M141 – DB-Systeme in Betrieb nehmen (Tag 2)




| Tätigkeit                                     | SQL-Befehl                                                                                      | Gruppe | Gefährlich                |
|----------------------------------------------|--------------------------------------------------------------------------------------------------|--------|---------------------------|
| 1) Alle Daten einer Tabelle anzeigen         | `SELECT * FROM tabellenname;`                                                                   | DML    | nein                      |
| 2) Datenbank auswählen                       | `USE datenbankname;`                                                                            | DDL    | nein                      |
| 3) Eine neue Datenbank erstellen             | `CREATE DATABASE datenbankname;`                                                                | DDL    | nein                      |
| 4) Eine neue Tabelle erstellen               | `CREATE TABLE tabellenname (spalte1 Datentyp, spalte2 Datentyp, ...);`                          | DDL    | nein                      |
| 5) Eine Tabelle löschen                      | `DROP TABLE tabellenname;`                                                                      | DDL    | **ja**                    |
| 6) Tabellenstruktur kontrollieren            | `DESCRIBE tabellenname;` oder `SHOW COLUMNS FROM tabellenname;`                                | DDL    | nein                      |
| 7) Datenbanken anzeigen                      | `SHOW DATABASES;`                                                                               | DDL    | nein                      |
| 8) Tabellen einer DB anzeigen                | `SHOW TABLES;`                                                                                  | DDL    | nein                      |
| 9) Daten in eine Tabelle eintragen           | `INSERT INTO tabellenname (spalte1, spalte2) VALUES (wert1, wert2);`                            | DML    | nein                      |
| 10) Daten in einer Tabelle ändern            | `UPDATE tabellenname SET spalte1 = wert1 WHERE bedingung;`                                     | DML    | **ja** *(ohne WHERE)*     |
| 11) Daten in einer Tabelle löschen           | `DELETE FROM tabellenname WHERE bedingung;`                                                     | DML    | **ja** *(ohne WHERE)*     |
| 12) Spalte in einer Tabelle löschen          | `ALTER TABLE tabellenname DROP COLUMN spaltenname;`                                             | DDL    | **ja**                    |
