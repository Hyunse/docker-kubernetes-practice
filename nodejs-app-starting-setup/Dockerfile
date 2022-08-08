FROM  node

# All command in the app folder
WORKDIR /app

# first . : same folder 
# second . : where copy 
COPY . /app

RUN npm install

EXPOSE 80

CMD ["node", "server.js"]`