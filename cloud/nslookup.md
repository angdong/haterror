## nslookup 에러

### env
* AWS

### problem
```bash
$ nslookup DOMAIN_NAME

server can't find DOMAIN_NAME: NXDOMAIN
```

### solution
`VPC` > `작업` > `VPC 설정 편집` > `DNS 설정` 두 항목 체크

![Alt text](../img/dns_config_in_vpc.PNG)