```
provisioner "file" {
    source = ""
    destination = ""
}
```

$\to$  Missing connection configuration for provisioner.

sol)

```
connection {
    type        = "ssh"
    user        = "ubuntu"
    private_key = file("~/Downloads/AWS_keys/test.pem")
    host        = self.public_dns
}
```

와 같이 instance 내에 connection 도 선언하기

-> 아직 못고침;;