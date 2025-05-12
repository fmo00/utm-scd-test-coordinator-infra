FROM node:18-alpine

RUN npm install -g @mockoon/cli@9.1.0
COPY ./uss.json ./uss.json

RUN apk --no-cache add curl tzdata

RUN adduser --shell /bin/sh --disabled-password --gecos "" mockoon
RUN chown -R mockoon ./uss.json
USER mockoon

EXPOSE 3002

ENTRYPOINT ["mockoon-cli","start","--disable-log-to-file","--data","./uss.json","--port","3002"]