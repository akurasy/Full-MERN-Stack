# Get node js image to build the frontend application
# this step is using node runtime, because we need to run the build command to get the static content

FROM node:slim AS builder

WORKDIR /app

COPY . /app

RUN npm install

ENV VITE_BACKEND_SERVER=http://35.92.7.67:8888/

RUN npm run build

# Get nginx image to copy over the files gotten from the build stage and serve the static content in an nginx image

FROM nginx:slim

COPY --from=builder /app/dist /usr/share/nginx/html

EXPOSE 80

ENTRYPOINT [ "nginx", "-g", "daemon off;" ]


