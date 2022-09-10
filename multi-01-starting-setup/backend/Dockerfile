FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD ["node", "app.js"]

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