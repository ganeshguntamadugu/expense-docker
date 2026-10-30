FROM mysql:latest

ENV MYSQL_ROOT_PASSWORD=gana@123
    # MYSQL_DATABASE=gangs\
    # MYSQL_USER=ganesh \
    # MYSQL_PASSWORD=ganesh@321

ADD scripts/*.sql /docker-entrypoint-initdb.d
    