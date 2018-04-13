FROM node:8-alpine

RUN apk add --no-cache curl

ENV WORKDIR="/app"
RUN mkdir -p ${WORKDIR}
WORKDIR ${WORKDIR}

COPY . ${WORKDIR}
RUN npm install --quiet  && npm cache clean --force && rm -rf ~/.npm

CMD [ "npm", "start" ]