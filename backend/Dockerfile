FROM node:20

EXPOSE 8080

ENV DB_HOST=expense_mysql \
    DB_USER=expense \
    DB_PWD=ExpenseApp@1 \
    DB_DATABASE=transactions

RUN mkdir /opt/server

WORKDIR /opt/server

COPY code/package.json .

COPY code/*.js .

RUN npm install

USER expense

CMD [ "node", "index.js" ]

