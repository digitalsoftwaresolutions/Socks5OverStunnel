# Socks5OverStunnel
Dante Over Stunnel (Docker)

# CAUTION 
generate your own PEM file with 
```
openssl genrsa -out key.pem 2048
openssl req -new -x509 -key key.pem -out cert.pem -days 1095
cat key.pem cert.pem >> stunnel.pem

```
YOU SHOULD NEVER USE THE PROVIDED PEM FILE (it's just for templating)
