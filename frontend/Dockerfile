FROM nginx

RUN rm -rf /usr/share/nginx/html/*

WORKDIR /usr/share/nginx/html/

COPY code .

COPY code/nginx.conf /etc/nginx/default.d/expense.conf

