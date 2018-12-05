FROM node:8-alpine as builder

WORKDIR /var/app

COPY package.json package.json

RUN npm install

COPY . .

RUN npm run build

FROM nginx
EXPOSE 3000
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf
COPY --from=builder /var/app/build /usr/share/nginx/html
