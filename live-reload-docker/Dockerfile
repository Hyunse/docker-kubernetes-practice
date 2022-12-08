FROM node:16-alpine

WORKDIR /app

COPY package.json /app

RUN npm install

COPY . /app

EXPOSE 3000

CMD ["npm", "run", "dev"]

# Build
# docker build -t live-app .

# Run

# docker run \
#     --name live-container \
#     -p 3000:3000 \
#     -v `pwd`/nodejs-with-mongodb-api-example:/app \
#     -v nodemodules:/app/node_modules \
#     live-app

# docker run --rm --name live-container -p 3000:3000 -v `pwd`:/app -v live-modules:/app/node_modules live-app