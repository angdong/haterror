## terraform apply시 에러 발생

### env
window

[실습](https://github.com/wardviaene/terraform-course/tree/master/codepipeline-demo) 중 에러 발생

### problem
```bash
$terraform apply
```

```bash
│ Warning: Argument is deprecated
│
│   with module.vpc.aws_eip.nat, 
│   on .terraform\modules\vpc\main.tf line 908, in resource "aws_eip" "nat":
│  908:   vpc = true
│
│ use domain attribute instead
╵
╷
│ Error: Unsupported argument
│
│   on .terraform\modules\vpc\main.tf line 36, in resource "aws_vpc" "this":
│   36:   enable_classiclink               = var.enable_classiclink
│
│ An argument named "enable_classiclink" is not expected here.
╵
╷
│ Error: Unsupported argument
│
│   on .terraform\modules\vpc\main.tf line 37, in resource "aws_vpc" "this":
│   37:   enable_classiclink_dns_support   = var.enable_classiclink_dns_support
│
│ An argument named "enable_classiclink_dns_support" is not expected here.
╵
╷
│ Error: Unsupported argument
│
│   on .terraform\modules\vpc\main.tf line 1132, in resource "aws_default_vpc" "this":
│ 1132:   enable_classiclink   = var.default_vpc_enable_classiclink
│
│ An argument named "enable_classiclink" is not expected here.
```

### solution
일단 provider 버전을 낮춤\
[참고](https://www.reddit.com/r/Terraform/comments/13uc728/an_issue_with_terraform_module_320/?rdt=46083)