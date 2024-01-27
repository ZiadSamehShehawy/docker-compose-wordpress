# Docker Compose WordPress
This is a simple Docker Compose setup for running WordPress with MySQL.

# Configuration.

    WordPress:
        Username: elzoz
        Password: P@ssw0rd
        Database Name: customdb

    MySQL:
        Username: elzoz
        Password: P@ssw0rd
        Database Name: customdb

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/ZiadSamehShehawy/docker-compose-wordpress.git
   cd docker-compose-wordpress
Start the containers:

1- docker-compose up -d

2- Access WordPress at http://localhost:8080

3- Login DB:
sudo docker exec -it ubuntu-db-1 mysql -u elzoz -p

