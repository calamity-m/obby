Category: [[Help]]
Tags: #help #certs #openssl

# How do I inspect a pem certificate?

```
openssl x509 -in cert.pem -noout -text
```

# How do I inspect all bundled certs in a pem certificate?

```
while openssl x509 -noout -text; do :; done < cert-bundle.pem
```

