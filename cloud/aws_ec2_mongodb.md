# mongosh 설치 에러

```
mongosh: OpenSSL configuration error:
001908B0DC7F0000:error:030000A9:digital envelope routines:alg_module_init:unknown option:../deps/openssl/openssl/crypto/evp/evp_cnf.c:61:name=rh-allow-sha1-signatures, value=yes
```

sol)

```
sudo yum remove mongodb-mongosh
sudo yum install mongodb-mongosh-shared-openssl3
sudo yum install mongodb-mongosh
```