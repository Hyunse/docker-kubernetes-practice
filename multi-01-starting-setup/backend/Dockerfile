FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

# Default ENV
ENV MONGODB_USERNAME=arthur
ENV MONGODB_PASSWORD=secret
ENV MONGODB_URL=mongodb

CMD ["npm", "start"]

# 1. Without Network

# 1) MongoDB Container
# docker run --name mongodb --rm -d -p 27017:27017 mongo

# 2) Backend Container ( Node )
# docker build -t goals-node .
# docker run --name goals-backend --rm -d -p 80:80 goals-node


# 2. With Network

# 1) Network ( Name: goals-net )
# docker network create goals-net

# 2) MongoDB Container
# docker run --name mongodb --rm -d --network goals-net mongo

# 3) Backend Container ( Node )
# docker build -t goals-node .
# docker run --name goals-backend --rm -d -p 80:80 --network goals-net goals-node

# 3. With Volume
# MongoDB With Volume
# docker run --name mongodb -v data:/data/db --rm -d --network goals-net mongo

# MongoDB authentication with -e
# docker run --name mongodb -v data:/data/db --rm -d --network goals-net -e MONGO_INITDB_ROOT_USERNAME=arthur -e MONGO_INITDB_ROOT_PASSWORD=secret mongo

# Volume for log files & Bind mount
# docker run --name goals-backend -v /Users/arthur/Dev/docker-kubernetes-practice/multi-01-starting-setup/backend:/app -v logs:/app/logs -v /app/node_modules --rm -d -p 80:80 --network goals-net goals-node
