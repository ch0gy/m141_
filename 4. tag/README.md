# M141 - DB-Systeme in Betrieb nehmen (4. Tag) - Zusammenfassung

## Hackerangriffe
- Systeme wie „PATRAS“ oder öffentliche MySQL-Server können leicht gehackt werden, wenn Standard-Accounts ohne Passwörter existieren.
- XAMPP ist für Entwicklung gedacht, hat deshalb keine sicheren Voreinstellungen (root ohne Passwort!).

## Datenbank-Sicherheit

### Zugangskontrolle
- MySQL prüft beim Verbindungsaufbau (Authentifizierung): Benutzername, Passwort, Host (IP).
- Autorisierung prüft Rechte bei jeder DB-Anfrage.
- Benutzer sind eindeutig definiert durch `'user'@'host'`.

### Benutzerverwaltung
- Benutzer anlegen:  
  ```sql
  CREATE USER 'user'@'host' IDENTIFIED BY 'password';
  ``` 