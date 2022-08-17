FROM node:lts-alpine3.16
RUN set -eux; \
    apk add --no-cache bash

COPY docker-entrypoint.sh /usr/local/bin/

RUN chmod +x /usr/local/bin/docker-entrypoint.sh

ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]

WORKDIR /app
COPY . .
RUN npm i 

EXPOSE 5000
# TODO add wait4it
CMD ["node", "server.js"]
