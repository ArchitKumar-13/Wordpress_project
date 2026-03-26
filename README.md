# Wordpress_project
### Prerequisites: 
- Ubuntu Instance
  - Instance Type: ***t2.medium***
- Install <ins>**Docker**</ins>, <ins>**Docker-Compose**</ins> & <ins>**Git**</ins>

### ***Step*** 1 : Install Docker
```
sudo apt update
sudo apt install -y docker.io
sudo usermod -aG docker ubuntu
newgrp docker
docker --version
```

### ***Step*** 2 : Install Docker-Compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

### ***Step*** 3 : Check the version of git.
```
git --version | cut -d ' ' -f3
```

### ***Step*** 4 : Clone this repository.
```
git clone https://github.com/ArchitKumar-13/Wordpress_project
```

### ***Step*** 5 : Change the directory.
```
cd wordpress
```

### ***Step*** 6 : Create environment variable file.
```
mv .env.example .env
```
### ***Step*** 7 : Start docker containers in detached mode.
```
docker-compose up -d
```

### ***Step*** 8 : Check the containers are up and running.
```
docker ps
```

### ***Step*** 9 : Access Application.
### Go to your browser, and access this <ins>**Wordpress Application**</ins> on port <ins>**80**</ins> via the ubuntu instance public IPv4 or IPv6.

#### ***Allow the inbound port 80 in the security group.***
