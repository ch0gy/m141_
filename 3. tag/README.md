# M141 – Tag 3: DB-Systeme in Betrieb nehmen

## Tabellentypen in MySQL

| Tabellentyp | Transaktionen | Locking             | Performance       | Geeignet für                          |
|-------------|---------------|---------------------|-------------------|----------------------------------------|
| MyISAM      | Nein          | Table-Level-Locking | Schnell, leicht   | Lese-intensive Anwendungen             |
| Aria        | Eingeschränkt | Table-Level-Locking | Schnell           | Nachfolger von MyISAM, mit Logging     |
| InnoDB      | Ja            | Row-Level-Locking   | Höherer Overhead  | Multi-User, hohe Datenintegrität       |

> Nur InnoDB, BDB und Gemini unterstützen Transaktionen und referenzielle Integrität.

---

## Speicherformate

### MyISAM
- `.frm` – Tabellenstruktur
- `.MYD` – Daten
- `.MYI` – Indexe

### InnoDB
- `.frm` + `.ibd` (wenn `innodb_file_per_table=1`)
- Zentraler Tablespace: `ibdata1`, `ib_logfile0`, `ib_logfile1`, etc.

---

## Transaktionen

### Beispiel

```sql
BEGIN;
  UPDATE konto SET saldo = saldo - 100 WHERE name = 'Von';
  UPDATE konto SET saldo = saldo + 100 WHERE name = 'Nach';
COMMIT;
