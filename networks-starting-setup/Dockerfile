FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

CMD ["node", "app.js"]

# build
# docker build -t favorites-node .

# run
# docker run --name favorites -d --rm -p 3000:3000 favorites-node 

# MongoDB
# docker run -d --name mongodb mongo

# Network ( Within a Docker network, all containers can communicate wiht each other and IPs are automatically resolved d)
# docker run --network 

# 1) Create Network
# docker network create favorites-net

# 2) Run docker using Network
# docker run -d --name mongodb --network favorites-net mongo
# docker run --name favorites --network favorites-net -d --rm -p 3000:3000 favorites-node 
