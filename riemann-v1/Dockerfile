FROM ubuntu

RUN apt-get update
RUN apt-get install -y openjdk-8-jdk
RUN apt-get install -y wget tar aptitude 
RUN wget -P / https://github.com/riemann/riemann/releases/download/0.3.0/riemann-0.3.0.tar.bz2

RUN aptitude install bzip2
RUN tar xvfj /riemann-0.3.0.tar.bz2

RUN mkdir /etc/riemann
COPY riemann.config /etc/riemann/


EXPOSE 5555 5556
CMD ["/riemann-0.3.0/bin/riemann", "/etc/riemann/riemann.config"]
