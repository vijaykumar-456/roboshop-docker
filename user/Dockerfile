FROM node:20
WORKDIR  /app
COPY *.js .
COPY *.json .
RUN npm install
EXPOSE 8080
CMD ["node", "server.js"]
