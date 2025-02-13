# NetworkNexus

# docker setup in server:

sudo usermod -aG docker $USER -> Add Your User to the Docker Group
newgrp docker -> Apply the Changes
sudo systemctl restart docker -> Restart Docker Service
docker ps -> Check If Docker Works Without sudo (If it lists running containers without errors, your user now has permission)
docker-compose build (or) sudo docker-compose build

# Install Redis:

sudo apt update
sudo apt install -y redis-server
sudo systemctl start redis
sudo systemctl enable redis
sudo systemctl status redis

# Install MongoDB:

Import the MongoDB GPG Key:
curl -fsSL https://pgp.mongodb.com/server-7.0.asc | sudo tee /usr/share/keyrings/mongodb-server-7.0.gpg > /dev/null
Add the MongoDB Repository:
echo "deb [signed-by=/usr/share/keyrings/mongodb-server-7.0.gpg] https://repo.mongodb.org/apt/ubuntu $(lsb_release -cs)/mongodb-org/7.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-7.0.list
Update the Package List:
sudo apt update
Install MongoDB:
sudo apt install -y mongodb-org
Start and Enable MongoDB:
sudo systemctl start mongod
sudo systemctl enable mongod
Verify MongoDB Is Running:
sudo systemctl status mongod

# Redis:

Google - redis windows git install (https://github.com/tporadowski/redis/releases)
Redis-x64-5.0.14.1.msi - download

# Packages:

cors (allow requests from frontend)
Dotenv
Express
express-http-proxy
helmet
ioredis
jsonwebtoken
winston
argon2
express express-rate-limit (Useful for limiting API requests, user actions, or any other operations)
joi
mongoose
Rate-limit-redis
multer
Cloudinary
Amqplib

# Rabbitmq installation steps:

https://www.erlang.org/downloads -> install
https://www.rabbitmq.com/docs/install-windows(supported operating system->windows->direct downloads->click link to download) -> install
c:->program files -> RabbitMQ Server -> rabbitmq_server-4.0.5 -> sbin (open in cmd)
rabbitmq-plugins enable rabbitmq_management-> enter(rabbitmq installation complete)

https://amqp-node.github.io/amqplib/channel_api.html

# docker

docker-compose build
docker-compose up
docker ps
docker-compose logs api-gateway

# git bash comments to connect server
Your identification has been saved in /home/ubuntu/.ssh/id_rsa
Your public key has been saved in /home/ubuntu/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:1fMa+3bESs3EXBBV9EwIbIDa+Nw/BofX3WPb7znZlyU jeniferworkspace2025@gmail.com

git bash cmds:
Verify the .pem File Path (Run the following command in Git Bash (MINGW64))
ls -l /c/Users/jenif/.ssh/Network-Nexus.pem

Fix File Permissions(Once you've confirmed the .pem file exists, set the correct permissions:)
chmod 400 /c/Users/jenif/.ssh/Network-Nexus.pem

SSH Into EC2(Now, try connecting to your server with git bash)
ssh -i "/c/Users/jenif/.ssh/Network-Nexus.pem" ubuntu@13.53.131.57


ls -l ~/.ssh/
cat ~/.ssh/authorized_keys
priority

sudo apt install



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
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
jeniferworkspace
https://github.com/jeniferworkspace/NetworkNexus.git



git clone https://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@github.com/jeniferworkspace/NetworkNexus.git




# NOTE

In env files is CI/CD implemented just change the urls from localhost to what you mentioned in your build script files
In git hub actions place your secret keys and values
