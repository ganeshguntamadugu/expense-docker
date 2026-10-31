FROM node:20

EXPOSE 8080

ENV DB_HOST=expense_mysql \
    DB_USER=expense \
    DB_PWD=ExpenseApp@1 \
    DB_DATABASE=transactions

RUN useradd -m expense \
    mkdir /opt/server

WORKDIR /opt/server

COPY code/package.json .

COPY code/*.js .

RUN npm install \
    chown -R expense:expense /opt/server

USER expense

CMD [ "node", "index.js" ]

