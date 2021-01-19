FROM node:lts-alpine

RUN apk --no-cache add curl

RUN npm install -g http-server

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

EXPOSE 8080

CMD [ "npm",  "run", "serve" ]
