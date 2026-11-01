FROM nginx

RUN rm -rf /usr/share/nginx/html/*

RUN rm -rf /etc/nginx/nginx.conf

RUN rm -rf /etc/nginx/conf.d/default.conf

WORKDIR /usr/share/nginx/html/

COPY code .

COPY code/nginx.conf /etc/nginx/nginx.conf

