FROM node:slim

WORKDIR /backend

COPY . /backend/

RUN npm install

RUN npm run setup

EXPOSE 8888

ENTRYPOINT [ "npm", "run", "dev" ]