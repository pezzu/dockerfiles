FROM node:8-alpine

RUN apk add --no-cache --virtual .build-deps \
        binutils-gold \
        curl \
        g++ \
        gcc \
        gnupg \
        libgcc \
        linux-headers \
        make \
        python \ 
        yarn \
        && \
    yarn global add pouchdb-server && \
    apk del .build-deps


RUN mkdir /pouchdb

WORKDIR /pouchdb

CMD ["pouchdb-server", "-p", "5984", "-o", "0.0.0.0"]
	