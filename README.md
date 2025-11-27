# Squad Dev Environment

This repository provides a development environment for Squad servers and SquadJS. It uses Docker and Docker Compose to easily run a dedicated Squad server, SFTP, MariaDB, and SquadJS locally or on a server.

## Features

- Squad Dedicated Server as a Docker container
- SquadJS integration for server management and automation
- SFTP access for log files
- MariaDB for persistent data storage
- Example configuration files for quick setup

## Requirements

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/sqaud-dev-environment.git
   cd sqaud-dev-environment
   ```

2. **Adjust configuration files**
   - Copy `.env.dist` to `.env` and adjust the values for your environment:
     ```bash
     cp .env.dist .env
     ```
   - Optionally adjust `squadjs-config.json.dist` and copy it to `squadjs-config.json`:
     ```bash
     cp squadjs-config.json.dist squadjs-config.json
     ```

3. **Start Docker containers**
   ```bash
   docker compose up -d
   ```

4. **Check server status**
   ```bash
   docker compose ps
   ```

## Directory Structure

- `squad-data/` – Persistent data for the Squad server
- `squadjs-config.json` – Configuration for SquadJS
- `.env` – Environment variables for all containers
- `docker-compose.yml` – Docker Compose setup

## Useful Commands

- Show logs:  
  `docker compose logs -f squad`
- Stop containers:  
  `docker compose down`

## Notes

- The default configuration is intended for development and testing purposes.
- Change passwords and ports before using in production.
- Additional SquadJS plugins can be enabled in the configuration.

## License

This project is licensed under the [GNU General Public License v3.0](LICENSE).
