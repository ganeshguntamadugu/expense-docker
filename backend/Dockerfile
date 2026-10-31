FROM node:20

EXPOSE 8080

RUN mkdir /opt/server

USER expense

WORKDIR /opt/server

COPY code/package.json .

COPY code/*.js .

RUN npm install

CMD [ "node", "index.js" ]

ENV DB_HOST=expense_mysql \
    DB_USER=expense \
    DB_PWD=ExpenseApp@1 \
    DB_DATABASE=transactions