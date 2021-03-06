# How run 3 apps on the same server in diferent port using Docker 
```
                  +--- host --------> node.js on localhost:8080
                  |
users --> nginx --|--- host/odoo13 ---> odoo on localhost:8013
                  |
                  +--- host/odoo14 ---> odoo on localhost:8014
```

# Step 1 - Install Docker
```
apt-get update && apt-get upgrade -y
apt  install docker.io docker-compose -y

sudo apt install curl
sudo curl -L "https://github.com/docker/compose/releases/download/1.26.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo docker–compose --version
```

# Step 2 - Install Odoo 13 in port 8013
```
git clone https://github.com/falconsoft3d/run-docker-nginx-app-by-port
cd run-docker-nginx-app-by-port
cd odoo13
docker-compose up -d
```

# Step 3 - Install Odoo 14 in port 8014
```
cd ..
cd odoo14
docker-compose up -d
```

# Step 4 - Run App Home
```
cd ..
cd homeapp
docker-compose up -d
```

# Step 5 - nginx
```
shell docker run -d -p 80:80 -v /var/run/docker.sock:/tmp/docker.sock jwilder/nginx-proxy
```

# Oher command
```
docker build -t nginx .
docker run -p 80:80 nginx
docker exec -it nginx  bash
```