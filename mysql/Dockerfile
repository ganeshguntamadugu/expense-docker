FROM mysql:8.0

ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1
    # MYSQL_DATABASE=gangs\
    # MYSQL_USER=ganesh \
    # MYSQL_PASSWORD=ganesh@321

RUN groupadd expense && \
    useradd -g expense expense && \
    chown -R expense:expense /var/lib/mysql /var/lib/mysqld /docker-entrypoint-initdb.d

ADD scripts/*.sql /docker-entrypoint-initdb.d

USER expense
    