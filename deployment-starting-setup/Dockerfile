FROM node:14-alpine

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

CMD ["node", "app.js"]

# build
# docker build -t node-dep-example .

# Run
# docker run -d --rm --name node-dep -p 80:80 node-dep-example

# Bind Mounts, Volume?
# In Development
# Use "Bind Mounts" to provide your local host project files to the running container
# Allows for instant updates without restarting the container

# In Production
# A container should really work standalone, you should NOT have source code on your remote machine
# Use COPY to copy a code snapshot into the image
# Ensures that every image runs without any extra, surrounding configuration or code

# Docker Engine Install
# https://docs.docker.com/engine/install/

# docker push kimhyunse/node-example-1:tagname