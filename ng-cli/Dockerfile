FROM node:16-alpine

LABEL authors="Daniel Avila"

#Linux setup
RUN apk update \
  && apk add --update alpine-sdk \
  && apk del alpine-sdk \
  && rm -rf /tmp/* /var/cache/apk/* *.tar.gz ~/.npm \
  && npm cache verify \
  && sed -i -e "s/bin\/ash/bin\/sh/" /etc/passwd

WORKDIR /app

VOLUME ["/app"]

#Angular CLI
RUN npm install -g @angular/cli

EXPOSE 4200

CMD [ "help" ]

ENTRYPOINT [ "ng" ]

USER node
