FROM alpine 

WORKDIR /home/3proxy

RUN apk add --no-cache -X http://dl-cdn.alpinelinux.org/alpine/edge/testing 3proxy
COPY 3proxy.conf 3proxy.conf 
ENTRYPOINT [ "3proxy","/home/3proxy/3proxy.conf" ]