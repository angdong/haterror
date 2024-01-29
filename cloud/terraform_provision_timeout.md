## Timeout Error

### env
[해당 환경](https://github.com/wardviaene/terraform-course/tree/master/demo-2) 에서 ssh 오류 발생



```
│ Error: file provisioner error
│
│   with aws_instance.example,
│   on instance.tf line 14, in resource "aws_instance" "example":
│   14:   provisioner "file" {
│
│ timeout - last error: dial tcp 3.37.129.220:22: i/o timeout
```
### solution
EC2의 default 보안 그룹에 TCP 허용


### env2
명령어 없는 오류 발생

```
aws_instance.example (remote-exec): Connected!
aws_instance.example (remote-exec): /tmp/script.sh: line 9: apt-get: command not found
aws_instance.example (remote-exec): /tmp/script.sh: line 10: apt-get: command not found
aws_instance.example (remote-exec): Redirecting to /bin/systemctl start nginx.service
aws_instance.example (remote-exec): Failed to start nginx.service: Unit nginx.service not found.
╷
│ Error: remote-exec provisioner error
│
│   with aws_instance.example,
│   on instance.tf line 18, in resource "aws_instance" "example":
│   18:   provisioner "remote-exec" {
│
│ error executing "/tmp/terraform_1913275291.sh": Process exited with status 5
```

### solution
AWS 리눅스 배포판은 `apt-get` 을 지원하지 않기 때문\
$\to$ `yum` 을 사용하기