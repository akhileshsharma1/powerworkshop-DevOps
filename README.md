# php-hello-world
A simple hello-world for composer

# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

Installation using Dockerfile
------------

Build Docker Image
``` bash
docker build -t workshop .
```

Run Docker Image
``` bash
docker run -dp 0.0.0.0:8081:80 workshop
```

Installation using docker-compose.yml
------------

Build and run Docker Image
``` bash
docker-compose up -d
```

Access the Application
------------

Access the application using <ip-address>:8081

![Site Demo](https://github.com/akhileshsharma1/powerworkshop-DevOps/blob/main/images/browser.png)

Configure GitHub Actions
------------

![GitHub Actions](https://github.com/akhileshsharma1/powerworkshop-DevOps/blob/main/images/actions.png)

Pushing Image to DockerHub
------------

Build Docker Image
``` bash
docker build -t your_username/devops-workshop:php-hello-world .
```

Login to DockerHub
``` bash
docker login
```

Push the Docker Image
``` bash
docker push your_username/devops-workshop:php-hello-world
```

![DockerHub](https://github.com/akhileshsharma1/powerworkshop-DevOps/blob/main/images/dockerhub.png)

docker ps
![Docker Ps](https://github.com/akhileshsharma1/powerworkshop-DevOps/blob/main/images/docker%20ps.png)

