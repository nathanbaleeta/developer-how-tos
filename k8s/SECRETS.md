
### Checking the expiration date of the SSL certificate
```
openssl x509 -noout -dates -in domain.crt
```

### Verify certificate file
```
openssl x509 -noout -text -in domain.crt
```
