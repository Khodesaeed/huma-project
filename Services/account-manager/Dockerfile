FROM node:lts-alpine3.16

WORKDIR /app
COPY . .
RUN npm i 

EXPOSE 5000
# TODO add wait4it
CMD ["node", "server.js"]