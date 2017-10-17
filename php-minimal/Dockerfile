FROM evarga/jenkins-slave

# PHP 7
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y wget curl git software-properties-common python-software-properties
RUN add-apt-repository ppa:ondrej/php -y && \
    apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
    php7.0-cli php7.0-dev php7.0-common openssl php-pear

# PHP Extensions
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
    php7.0-xml php7.0-soap php7.0-curl php7.0-mcrypt php7.0-mbstring zip unzip php7.0-zip

# Xdebug
RUN pecl install xdebug
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install \
    php7.0-xdebug

# Phing
RUN wget --no-check-certificate http://www.phing.info/get/phing-2.16.0.phar
RUN mv phing*.phar /usr/bin/phing
RUN chmod a+x /usr/bin/phing
