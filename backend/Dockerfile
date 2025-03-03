#FROM node:20
# Try to use light weight OS to save space and booting time.
FROM node:20.18.3-alpine3.21
RUN addgroup -S expense && adduser -S expense -G expense
RUN mkdir /opt/backend
RUN chown -R expense:expense /opt/backend
WORKDIR /opt/backend
COPY package.json .
COPY *.js .
RUN npm install
ENV DB_HOST="mysql"
# ENV DB_HOST="localhost"

CMD ["node", "index.js"]