FROM debian 

WORKDIR /home/3proxy

RUN apt update && apt install build-essential wget -y
RUN wget https://github.com/z3APA3A/3proxy/archive/0.8.12.tar.gz
RUN tar -xvf 0.8.12.tar.gz 
RUN cd 3proxy-0.8.12 && make -f Makefile.Linux && make -f Makefile.Linux install
RUN rm -rf 3proxy-0.8.12
RUN rm -rf 0.8.12.tar.gz

COPY 3proxy.conf 3proxy.conf 
ENTRYPOINT [ "/usr/local/bin/3proxy","/home/3proxy/3proxy.conf" ]