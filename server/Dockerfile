FROM node:8-alpine

WORKDIR /var/app

EXPOSE 5000

COPY package.json package.json

RUN npm install

COPY . .

CMD ["npm", "run", "start"]