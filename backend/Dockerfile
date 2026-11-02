FROM node:20 AS builder
WORKDIR /opt/server
COPY code/package.json .
COPY code/*.js .
RUN npm install

FROM node:20.18.0-alpine3.20
EXPOSE 8080
ENV DB_HOST=expense_mysql \
    DB_USER=expense \
    DB_PWD=ExpenseApp@1 \
    DB_DATABASE=transactions
RUN addgroup -S expense && adduser -S expense -G expense && \
    mkdir /opt/server && \
    chown -R expense:expense /opt/server
WORKDIR /opt/server
COPY --from=builder /opt/server /opt/server/
USER expense
CMD [ "node", "index.js" ]




#Before best practices implemented
# FROM node:20

# EXPOSE 8080

# ENV DB_HOST=expense_mysql \
#     DB_USER=expense \
#     DB_PWD=ExpenseApp@1 \
#     DB_DATABASE=transactions
    
# RUN mkdir /opt/server

# WORKDIR /opt/server

# COPY code/package.json .

# COPY code/*.js .

# RUN npm install 

# CMD [ "node", "index.js" ]

