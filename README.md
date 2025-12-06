# Squad Dev Environment

This repository provides a development environment for Squad servers and SquadJS. It uses Docker and Docker Compose to easily run a dedicated Squad server, SFTP, MariaDB, and SquadJS locally or on a server.
There are two docker-compose.yml files: one for a Squad server with a SFTP to make the log files accessible and another that includes SquadJS and a MariaDB.

## Requirements

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Hans-Vader/squad-dev-environment.git
   ```
   
    ```bash
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

## License

This project is licensed under the [GNU General Public License v3.0](LICENSE).
