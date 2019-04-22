FROM alpine 

WORKDIR /stunnel

RUN apk add --update stunnel

COPY stunnel.conf stunnel.conf
COPY stunnel.pem stunnel.pem
CMD [ "stunnel","/stunnel/stunnel.conf" ]

