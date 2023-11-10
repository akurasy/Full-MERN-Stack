# Get node js image to build the frontend application

FROM node:slim AS builder

WORKDIR /app

COPY . /app

RUN npm install

RUN npm run build

# Get nginx image to copy over the files gotten from the build stage and serve the static content in an nginx image

FROM nginx:slim

WORKDIR /app

COPY --from=builder /app/dist /app

EXPOSE 80

ENTRYPOINT [ "nginx", "-g", "daemon off;" ]