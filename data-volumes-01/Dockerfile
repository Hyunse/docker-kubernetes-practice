FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

# ARGuments
ARG DEFAULT_PORT=80

# ENViroment variable
ENV PORT $DEFAULT_PORT

EXPOSE $PORT

VOLUME [ "/app/feedback" ]

CMD [ "npm", "start"]

# Volume example
# docker run -d --rm -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "/Users/arthur/Dev/docker-kubernetes-practice/data-volumes-01:/app" -v /app/node_modules feedback-node:volumes

# Env example 1
# docker run -d --rm -p 3000:8000 -e PORT=8000 --name feedback-app -v feedback:/app/feedback -v "/Users/arthur/Dev/docker-kubernetes-practice/data-volumes-01:/app" -v /app/node_modules feedback-node:volumes

# Env example 2 ( .env file)
# docker run -d --rm -p 3000:8000 --env-file ./.env --name feedback-app -v feedback:/app/feedback -v "/Users/arthur/Dev/docker-kubernetes-practice/data-volumes-01:/app" -v /app/node_modules feedback-node:volumes

# Arg example
# docker build -t feedback-node:dev --build-arg DEFAULT_PORT=8000 .
