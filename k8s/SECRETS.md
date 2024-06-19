
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

### Checking the server’s SSL certificate
```
openssl s_client -showcerts -connect example.org:443
```
