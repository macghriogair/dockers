FROM evarga/jenkins-slave

RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y software-properties-common python-software-properties
RUN add-apt-repository ppa:ondrej/php -y && \
    apt-get update

RUN DEBIAN_FRONTEND=noninteractive apt-get -y install php7.0-cli php7.0-common php7.0-soap php7.0-curl php7.0-mcrypt
