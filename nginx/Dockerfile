FROM daocloud.io/library/nginx:latest


ADD ./nginx.conf /etc/nginx/nginx.conf
ADD ./conf.d/*  /etc/nginx/conf.d/
ADD ./fastcgi_params /etc/nginx/fastcgi_params
RUN  mkdir /code/src && mkdir -p /code/log && mkdir /code/log/nginx
RUN  chown -R www-data.www-data /code/src /code/log

VOLUME ["/code"]
