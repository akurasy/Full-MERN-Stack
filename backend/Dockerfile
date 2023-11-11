FROM node:slim

WORKDIR /backend

COPY . /backend/

RUN npm install

ENV DATABASE=mongodb://mongo-container:27017/

ENV JWT_SECRET=thiscanbechangedlater123654789
ENV KEY=asdasda
ENV NODE_ENV=developement
ENV SECRET=asdasdasd
ENV OPENSSL_CONF=/dev/null


RUN npm run setup

EXPOSE 8888

ENTRYPOINT [ "npm", "run", "dev" ]