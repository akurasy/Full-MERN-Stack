FROM node:slim

WORKDIR /backend

COPY . /backend/

RUN npm install

RUN npm run setup

ENTRYPOINT [ "npm", "run", "dev" ]