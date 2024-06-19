
### Checking the expiration date of the SSL certificate
```
openssl x509 -noout -dates -in domain.crt
```

### Verify certificate file
```
openssl x509 -noout -text -in domain.crt
```

### Check CSR file
```
openssl req -noout -text -in domain.csr
```

### Check PEM file
```
openssl x509 -in certificate.pem -text
```

### Check private key file
```
openssl rsa -in privateKey.key -check
```
OR
```
openssl rsa -noout -text -in domain.key
```

### Checking the server’s SSL certificate
```
openssl s_client -showcerts -connect example.org:443
```

### Verify Distinguished Name of SSL Certificate
```
openssl x509 -noout -subject -in domain.crt
```
