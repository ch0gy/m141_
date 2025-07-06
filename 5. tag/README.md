# M141 – DB-Systeme in Betrieb nehmen (Tag 5)

## Zugriffsberechtigungen & Autorisierung

Autorisierung kann auf verschiedenen Ebenen erfolgen:
- Global (`*.*`)
- Datenbank (`db.*`)
- Tabelle (`db.tbl`)
- Spalte (`(col1, col2) ON db.tbl`)

###  Wichtige Privilegien

| Privileg         | Bedeutung                                   |
|------------------|---------------------------------------------|
| `SELECT`         | Lesen                                       |
| `INSERT`         | Einfügen                                    |
| `UPDATE`         | Ändern                                      |
| `DELETE`         | Löschen                                     |
| `GRANT OPTION`   | Rechte an andere vergeben                   |
| `FILE`           | Zugriff auf Dateien mit `LOAD DATA INFILE` |
| `ALL`            | Alle Rechte (ausser `GRANT OPTION`)         |
| `USAGE`          | Nur Login, keine Rechte                     |

>  `FILE`-Privileg erlaubt Lesezugriff auf systemweite Dateien → nur mit Vorsicht vergeben.

---

##  Benutzer & Rechte verwalten

###  Benutzer erstellen & Rechte vergeben

```sql
-- Benutzer mit Rechten anlegen
GRANT SELECT, INSERT ON db.tbl TO 'user'@'host' IDENTIFIED BY 'Passwort';

-- Alle Rechte inkl. GRANT
GRANT ALL ON db.* TO 'admin'@'localhost' WITH GRANT OPTION;

-- Dateizugriffsrechte
GRANT FILE ON *.* TO 'user'@'%';

-- Rechte entziehen
REVOKE SELECT ON db.tbl FROM 'user'@'host';

-- Rechte anzeigen
SHOW GRANTS FOR 'user'@'host';

-- Änderungen anwenden
FLUSH PRIVILEGES;
