FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

VOLUME [ "/app/feedback" ]

CMD [ "npm", "start"]

# docker run -d --rm -p 3000:80 --name feedback-app -v feedback:/app/feedback -v "/Users/arthur/Dev/docker-kubernetes-practice/data-volumes-01:/app" -v /app/node_module
# s feedback-node:volumes