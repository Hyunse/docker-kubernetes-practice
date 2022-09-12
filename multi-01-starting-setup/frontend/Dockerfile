FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD ["npm", "start"]

# Frontend Container
# Without Network
# docker build -t goals-react .
# docker run --name goals-frontend --rm -p 3000:3000 -it goals-react

# With Network
# docker build -t goals-react .
# docker run --name goals-frontend --rm -p 3000:3000 -it goals-react

# Live Source Code Update ( Bind mount )
# docker run -v /Users/arthur/Dev/docker-kubernetes-practice/multi-01-starting-setup/frontend/src:/app/src --name goals-frontend --rm -p 3000:3000 -it goals-react