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

# NOTE

In env files is CI/CD implemented just change the urls from localhost to what you mentioned in your build script files
In git hub actions place your secret keys and values
