
FROM ubuntu

RUN apt-get update
RUN apt-get install -y git

WORKDIR /opt

RUN git clone http://code.google.com/p/irap/ irap
RUN apt-get install -y python gcc g++ curl openjdk-7-jdk
RUN apt-get install -y libcurl4-openssl-dev gfortran
RUN apt-get install -y make libbz2-dev python-dev readline-common
RUN ./irap/scripts/irap_install.sh -a irap_install -s irap
