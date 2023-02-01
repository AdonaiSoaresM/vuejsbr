FROM node:10-alpine

WORKDIR /src

COPY . .

RUN npm install

EXPOSE 3000

ENTRYPOINT ["npm" ,"start"]
