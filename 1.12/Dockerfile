FROM node:14

WORKDIR /usr/src/myapp

COPY . .

RUN npm install

RUN npm run build

RUN npm install -g serve

EXPOSE 5000

ENTRYPOINT [ "serve -s -l 5000 build" ]

