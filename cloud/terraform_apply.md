## Terraform apply 시 에러

### env
* terraform config 파일 구성 후
* `init` -> `apply` 시 에러 발생

```
$ terraform apply
╷
│ Error: No valid credential sources found
│
│   with provider["registry.terraform.io/hashicorp/aws"],
│   on main.tf line 10, in provider "aws":
│   10: provider "aws" {
│
│ Please see https://registry.terraform.io/providers/hashicorp/aws
│ for more information about providing credentials.
│
│ Error: failed to refresh cached credentials, no EC2 IMDS role found, operation error ec2imds: GetMetadata, request
│ canceled, context deadline exceeded
```

### solution
$terraform init이 provider의 config나 credential을 보지 않기 때문에 terraform block 내에 명시를 해주기

**`provider` 내에(현재는 aws) `access_key`와 `secret_key` 명시하기**