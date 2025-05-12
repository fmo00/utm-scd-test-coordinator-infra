FROM node:18-alpine

RUN npm install -g @mockoon/cli@9.1.0
COPY ./dss.json ./dss.json

RUN apk --no-cache add curl tzdata

RUN adduser --shell /bin/sh --disabled-password --gecos "" mockoon
RUN chown -R mockoon ./dss.json
USER mockoon

EXPOSE 3001

ENTRYPOINT ["mockoon-cli","start","--disable-log-to-file","--data","./dss.json","--port","3001"]
