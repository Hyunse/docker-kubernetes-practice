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