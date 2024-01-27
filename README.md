# Docker Compose WordPress
This Docker Compose setup simplifies running WordPress with MySQL.

## Configuration

**WordPress:**
- Username: elzoz
- Password: P@ssw0rd
- Database Name: customdb

**MySQL:**
- Username: elzoz
- Password: P@ssw0rd
- Database Name: customdb

## Prerequisites

### Install Docker:

```bash
# Update package list
sudo apt update

# Install dependencies
sudo apt install -y ca-certificates curl gnupg lsb-release

# Add Docker GPG key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# Add Docker repository
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Update package list again
sudo apt-get update

# Install Docker
sudo apt install docker-ce docker-ce-cli containerd.io -y

# Add current user to the docker group
sudo usermod -aG docker $USER

# Activate changes to group membership
newgrp docker
```

### Install Docker Compose:

```bash
sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/ZiadSamehShehawy/docker-compose-wordpress.git
   cd docker-compose-wordpress
   ```

2. Start the containers:

   ```bash
   docker-compose up -d
   ```

3. Access WordPress at http://localhost:8080

4. To login to the MySQL database:

   ```bash
   sudo docker exec -it ubuntu-db-1 mysql -u elzoz -p
   ```
