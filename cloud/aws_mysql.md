# aws에서 mysql 설치 안됨

```
sudo yum install -y mysql
No match for argument: mysql Error: Unable to find a match: mysql
```

Amazon Linux 레포지토리가 MySQL을 포함하고 있지 않기 때문

sol)

[ref](https://repost.aws/questions/QUlwc51WiaRpaFa9NwLBmi5g/unable-to-find-a-match-mysql-on-ec2-connect)

```
sudo su -
dnf -y localinstall https://dev.mysql.com/get/mysql80-community-release-el9-4.noarch.rpm
dnf -y install mysql mysql-community-client
dnf -y install mysql-community-server
```