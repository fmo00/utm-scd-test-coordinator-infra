FROM node:22-alpine

RUN npm install -g @mockoon/cli@9.1.0
COPY ./auth.json ./auth.json

RUN apk --no-cache add curl tzdata

RUN adduser --shell /bin/sh --disabled-password --gecos "" mockoon
RUN chown -R mockoon ./auth.json
USER mockoon

EXPOSE 3000

ENTRYPOINT ["mockoon-cli","start","--data","./auth.json","--port","3000"]