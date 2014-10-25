FROM erjohnso/php-redis

RUN apt-get update && apt-get upgrade -y && apt-get install unzip -y

COPY index.php /var/www/index.php
COPY controllers.js /var/www/controllers.js
COPY index.html /var/www/index.html
COPY ~/appdynamics-php-agent-x64-linux-tar-self-service-3.9.3.0.zip /

RUN  unzip appdynamics-php-agent-x64-linux-tar-self-service-3.9.3.0.zip \
     && cd appdynamics-php-agent \
     && sh runme.sh

CMD /run.sh
