## Convert_DER(crt,cer,der)format_to_PEM

#### DER FORMAT
The DER format is the binary format of the PEM.

- DER certificates have the .der, .cer extensions
- They are generally used for JAVA servers

#### PEM FORMAT
The PEM format is the most common format among SSL certificates issued by certification authorities. This typeof certificate contains the following lines : "-----BEGIN CERTIFICATE-----" and "-----END CERTIFICATE-----". Certificates with the .pem extension are identical to the .crt or .cer extensions. It is thus possible for you to modify the extension of these files. PEM certificates can contain both the certificate and the private key in the same file. However, most servers like Apache want you to separate them into separate files.

- PEM certificates have the .pem, .crt, .cer and .key extensions
- They are encoded in ASCII Base64 format
- They are generally used for Apache servers or similar configurations

### CONVERT PEM TO DER

```
openssl x509 -outform der -in certificate.pem -out certificate.der
```

### CONVERT DER TO CER

```
openssl x509 -inform der -in certificat-ssl.der -out certificat-ssl.cer
```

### CONVERT DER(.CER) TO PEM 

```
openssl x509 -inform der -in certificate.cer -out certificate.pem
```

### CONVERT CER TO DER

```
openssl x509 -in certificat-ssl.cer -outform der -out certificat-ssl.der
```
