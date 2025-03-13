# PHP + MySQL + phpMyAdmin Docker Setup

## Prerequisites
Ensure Docker and Docker Compose are installed on your system.

## Stopping System Services (If Needed)
If Apache2 and MySQL are running on your local machine, stop them to free up the required ports:

```sh
sudo systemctl stop mysql
sudo systemctl stop apache2
```

## Setup Instructions
1. Clone this repository or navigate to your project directory.
2. Ensure your `docker-compose.yml` file is properly configured.
3. Build and start the containers:

```sh
docker compose up -d --build
```

## Accessing the Services
- **PHP Application:** [http://localhost:8080](http://localhost:8080)
- **phpMyAdmin:** [http://localhost:8081](http://localhost:8081)

## Stopping the Containers
To stop and remove the containers, run:

```sh
docker compose down
```

## Troubleshooting
- Ensure ports `8080` and `8081` are free before starting the containers.
- If permissions cause issues, run:

```sh
sudo chmod -R 777 .
```
- If database errors occur, restart the MySQL container:

```sh
docker restart mysql-db
```

