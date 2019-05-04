FROM alpine

WORKDIR /dante

RUN apk add --no-cache -X wget gcc make musl-dev
COPY dante.conf dante.conf
RUN wget https://www.inet.no/dante/files/dante-1.4.2.tar.gz
RUN tar -xvf dante-1.4.2.tar.gz
RUN cd dante-1.4.2 && ac_cv_func_sched_setscheduler=no ./configure && make && make install
ENTRYPOINT [ "sockd","-f","/dante/dante.conf" ]
