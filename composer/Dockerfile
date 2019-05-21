
FROM sockyjam/llxglaravel.artisan:v01

MAINTAINER SockyJam<sockyjam@126.com>


RUN curl -sS https://getcomposer.org/installer | php && \
       mv composer.phar /usr/local/bin/composer && \
       composer self-update && \
       apt-get remove --purge curl -y && \
       apt-get clean





