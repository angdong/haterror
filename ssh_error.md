```
$ ssh-add ../mykey
Could not open a connection to your authentication agent.
```

ssh-agent를 한번도 실행한 적이 없어서 발생하는 문제\
아래의 명령어를 쳐서 ssh-agent를 실행한 후에 재시도하면 된다.

```bash
eval $(ssh-agent)
```