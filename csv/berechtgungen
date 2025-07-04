USE m141_lb3_db
-- Rollen erstellen
CREATE ROLE 'User';
CREATE ROLE 'Admin';

-- Berechtigungen für Rolle 'User'
GRANT SELECT, UPDATE ON m141_lb3_db.tbl_personen TO 'User';

GRANT
  SELECT (deaktiviert, Benutzername, Vorname, Name, Benutzergruppe, aktiv, erfasst),
  INSERT (Benutzername, Vorname, Name, Benutzergruppe, aktiv, erfasst),
  UPDATE (Benutzername, Vorname, Name, Benutzergruppe, aktiv, erfasst)
ON m141_lb3_db.tbl_benutzer TO 'User';

GRANT SELECT, INSERT, UPDATE ON m141_lb3_db.tbl_buchung TO 'User';
GRANT SELECT, INSERT, UPDATE ON m141_lb3_db.tbl_positionen TO 'User';

GRANT SELECT ON m141_lb3_db.tbl_land TO 'User';
GRANT SELECT ON m141_lb3_db.tbl_leistung TO 'User';

-- Berechtigungen für Rolle 'Admin'
GRANT SELECT ON m141_lb3_db.tbl_positionen TO 'Admin';
GRANT SELECT ON m141_lb3_db.tbl_buchung TO 'Admin';

GRANT SELECT, INSERT, UPDATE, DELETE ON m141_lb3_db.tbl_personen TO 'Admin';
GRANT SELECT, INSERT, UPDATE, DELETE ON m141_lb3_db.tbl_land TO 'Admin';
GRANT SELECT, INSERT, UPDATE, DELETE ON m141_lb3_db.tbl_leistung TO 'Admin';
GRANT SELECT, INSERT, UPDATE, DELETE ON m141_lb3_db.tbl_benutzer TO 'Admin';

-- Benutzer erstellen
CREATE USER 'koichiro'@'%' IDENTIFIED BY 'koichiro';
CREATE USER 'tristan'@'%' IDENTIFIED BY 'tristan';

-- Rollen zuweisen
GRANT USAGE ON m141_lb3_db.* TO 'koichiro'@'%';
GRANT USAGE ON m141_lb3_db.* TO 'tristan'@'%';

GRANT User TO 'koichiro'@'%';
GRANT Admin TO 'tristan'@'%';

SET DEFAULT ROLE 'User' TO 'koichiro'@'%';
SET DEFAULT ROLE 'Admin' TO 'tristan'@'%';
