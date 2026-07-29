FROM node:20.20.2-alpine3.22 AS builder
WORKDIR  /app
COPY *.js .
COPY *.json .
RUN npm install


FROM node:20.20.2-alpine3.22
WORKDIR  /app
EXPOSE 8080
RUN addgroup -S roboshop && adduser -S -G roboshop roboshop && \
    chown -R roboshop:roboshop /app
COPY --from=builder /app /app
USER roboshop
CMD ["node", "server.js"]



# FROM node:20
# WORKDIR  /app
# COPY *.js .
# COPY *.json .
# RUN npm install
# EXPOSE 8080
# CMD ["node", "server.js"]
