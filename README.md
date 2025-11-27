# Squad Dev Environment

Dieses Repository stellt eine Entwicklungsumgebung für Squad-Server und SquadJS bereit. Es nutzt Docker und Docker Compose, um einen dedizierten Squad-Server, SFTP, MariaDB und SquadJS einfach lokal oder auf einem Server zu betreiben.

## Features

- Squad Dedicated Server als Docker-Container
- SquadJS-Integration für Server-Management und Automatisierung
- SFTP-Zugang für Logdateien
- MariaDB für persistente Datenhaltung
- Beispiel-Konfigurationsdateien für schnellen Einstieg

## Voraussetzungen

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Einrichtung

1. **Repository klonen**
   ```bash
   git clone https://github.com/dein-benutzername/sqaud-dev-environment.git
   cd sqaud-dev-environment
   ```

2. **Konfigurationsdateien anpassen**
   - Kopiere `.env.dist` zu `.env` und passe die Werte an deine Umgebung an:
     ```bash
     cp .env.dist .env
     ```
   - Passe ggf. `squadjs-config.json.dist` an und kopiere sie zu `squadjs-config.json`:
     ```bash
     cp squadjs-config.json.dist squadjs-config.json
     ```

3. **Docker-Container starten**
   ```bash
   docker compose up -d
   ```

4. **Server-Status prüfen**
   ```bash
   docker compose ps
   ```

## Verzeichnisstruktur

- `squad-data/` – Persistente Daten des Squad-Servers
- `squadjs-config.json` – Konfiguration für SquadJS
- `.env` – Umgebungsvariablen für alle Container
- `docker-compose.yml` – Docker Compose Setup

## Nützliche Kommandos

- Logs anzeigen:  
  `docker compose logs -f squad`
- Container stoppen:  
  `docker compose down`

## Hinweise

- Die Standard-Konfiguration ist für Entwicklungs- und Testzwecke gedacht.
- Passe Passwörter und Ports vor Produktivbetrieb an.
- Weitere SquadJS-Plugins können in der Konfiguration aktiviert werden.

## Lizenz

Dieses Projekt steht unter der [GNU General Public License v3.0](LICENSE).

