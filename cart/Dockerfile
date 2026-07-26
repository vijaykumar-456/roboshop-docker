FROM node:20
WORKDIR /app/
COPY *.json .
COPY *.js .
RUN npm install
EXPOSE 8080
CMD ["node", "server.js"]