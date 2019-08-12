FROM alpine 

WORKDIR /stunnel

RUN apk add --update stunnel openssl

RUN openssl genrsa -out key.pem 2048 \
&& openssl req -new -x509 -key key.pem -out cert.pem -days 3650 -batch \
&& cat key.pem cert.pem >> stunnel.pem

COPY stunnel.conf stunnel.conf
CMD [ "stunnel","/stunnel/stunnel.conf" ]

