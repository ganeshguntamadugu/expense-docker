FROM mysql:8.0

ENV MYSQL_ROOT_PASSWORD=ExpenseApp@1
    # MYSQL_DATABASE=gangs\
    # MYSQL_USER=ganesh \
    # MYSQL_PASSWORD=ganesh@321

ADD scripts/*.sql /docker-entrypoint-initdb.d
    