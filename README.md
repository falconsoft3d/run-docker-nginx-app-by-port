# How run 3 apps on the same server in diferent port using Docker 
```
                  +--- host --------> node.js on localhost:8080
                  |
users --> nginx --|--- host/odoo13 ---> odoo on localhost:8181
                  |
                  +--- host/odoo14 ---> odoo on localhost:7272
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

# Step 2 - Install Odoo 13 in port 8181
```
```

# Step 3 - Install Odoo 14 in port 7272
```
```
