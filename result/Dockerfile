FROM node:12.18.1-alpine
ENV NODE_ENV=production

WORKDIR /app

COPY ["./", "/app/"]

RUN npm install

CMD npm start

EXPOSE 80
