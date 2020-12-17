FROM djfarrelly/maildev
RUN apk add --update \
    gcc \
    make \
    g++ \
    python \
  && rm -rf /var/cache/apk/
WORKDIR /usr/src/app
ENV NODE_ENV production
RUN apk add --no-cache curl \
  && npm install \
  && npm install node-gyp -g \
  && npm install iconv --save \
  && npm prune \
  && npm cache clean --force \
  && rm -rf /tmp/*

EXPOSE 80 25 
