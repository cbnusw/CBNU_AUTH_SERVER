FROM node:16

WORKDIR /usr/src/app

COPY . .

RUN chown -R node:node /usr/src/

COPY package*.json ./

RUN npm i

RUN npm i -g pm2

EXPOSE 4000

CMD ["pm2-docker", "/usr/src/app/auth/index.js", "-i", "10", "--name", "auth-server"]
