FROM lip17/base-debian:0.2@sha256:6e372623dd5851ae8f0cd5c36caa363b9ffce49f96ebbf2e84f6e37192c59a80

RUN apt-get update && \ 
apt-get -qq -y --no-install-recommends install \
    gnupg2 \
    software-properties-common && \
apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0x219BD9C9 && \
apt-add-repository 'deb http://repos.azulsystems.com/debian stable main' && \ 
apt-get update && \
mkdir -p /usr/share/man/man1 && \
apt-get -qq -y --no-install-recommends install \
  zulu-11 && \
apt-get -qq -y purge gnupg2 software-properties-common && \
apt -y autoremove && \
rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME=/usr/lib/jvm/zulu-11-amd64 \
    JAVA_OPT=-Dfile.encoding=UTF-8
