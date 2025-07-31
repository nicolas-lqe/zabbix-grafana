# Zabbix and Grafana Docker Setup

This project sets up a Docker environment for Zabbix and Grafana using Docker Compose. It includes the necessary services and configurations to run both applications seamlessly.

## Prerequisites

- Docker installed on your Ubuntu Server.
- Docker Compose installed.

## Project Structure

```
zabbix-grafana
├── docker-compose.yml
└── README.md
```

## Setup Instructions

1. **Clone the repository** (if applicable) or navigate to the project directory:

   ```bash
   cd /path/to/zabbix-grafana
   ```

2. **Create a `.env` file** (optional) to store environment variables for sensitive data like passwords. For example:

   ```env
   MYSQL_ROOT_PASSWORD=root_password
   MYSQL_DATABASE=zabbix
   MYSQL_USER=zabbix
   MYSQL_PASSWORD=zabbix_password
   ```

3. **Start the services** using Docker Compose:

   ```bash
   docker-compose up -d
   ```

   This command will start the Zabbix server, MySQL database, and Grafana in detached mode.

4. **Access the applications**:

   - Zabbix: Open your browser and go to `http://<your-server-ip>:10051`
   - Grafana: Open your browser and go to `http://<your-server-ip>:3000`

5. **Default Credentials**:

   - Grafana: 
     - Username: `admin`
     - Password: `admin`

6. **Stopping the services**:

   To stop the running containers, use:

   ```bash
   docker-compose down
   ```

## Notes

- Ensure that the ports `10051` for Zabbix and `3000` for Grafana are not in use by other applications.
- You can customize the environment variables in the `docker-compose.yml` file as needed.

## Troubleshooting

- If you encounter issues, check the logs of the containers using:

  ```bash
  docker-compose logs
  ```
