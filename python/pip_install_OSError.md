## pip install 안되뮤ㅠㅠ

### env
윈도우, (사내 클라우드)

### problem
```
$ python -m pip install --user virtualenv
Collecting virtualenv
Obtaining dependency information for virtualenv from https://files.pythonhosted.org/packages/83/22/54b1180756d2d6194bcafb7425d437c3034c4bff92129c3e1e633079e2c4/virtualenv-20.25.0-py3-none-any.whl.metadata
WARNING: Retrying (Retry(total=4, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self-signed certificate in certificate chain (_ssl.c:1000)'))': /packages/83/22/54b1180756d2d6194bcafb7425d437c3034c4bff92129c3e1e633079e2c4/virtualenv-20.25.0-py3-none-any.whl.metadata
WARNING: Retrying (Retry(total=3, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self-signed certificate in certificate chain (_ssl.c:1000)'))': /packages/83/22/54b1180756d2d6194bcafb7425d437c3034c4bff92129c3e1e633079e2c4/virtualenv-20.25.0-py3-none-any.whl.metadata
WARNING: Retrying (Retry(total=2, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self-signed certificate in certificate chain (_ssl.c:1000)'))': /packages/83/22/54b1180756d2d6194bcafb7425d437c3034c4bff92129c3e1e633079e2c4/virtualenv-20.25.0-py3-none-any.whl.metadata
WARNING: Retrying (Retry(total=1, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self-signed certificate in certificate chain (_ssl.c:1000)'))': /packages/83/22/54b1180756d2d6194bcafb7425d437c3034c4bff92129c3e1e633079e2c4/virtualenv-20.25.0-py3-none-any.whl.metadata
WARNING: Retrying (Retry(total=0, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self-signed certificate in certificate chain (_ssl.c:1000)'))': /packages/83/22/54b1180756d2d6194bcafb7425d437c3034c4bff92129c3e1e633079e2c4/virtualenv-20.25.0-py3-none-any.whl.metadata
ERROR: Could not install packages due to an OSError: HTTPSConnectionPool(host='files.pythonhosted.org', port=443): Max retries exceeded with url: /packages/83/22/54b1180756d2d6194bcafb7425d437c3034c4bff92129c3e1e633079e2c4/virtualenv-20.25.0-py3-none-any.whl.metadata (Caused by SSLError(SSLCertVerificationError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self-signed certificate in certificate chain (_ssl.c:1000)')))
```

### solution
```bash
python -m pip install --user virtualenv --trusted-host files.pythonhosted.org
```