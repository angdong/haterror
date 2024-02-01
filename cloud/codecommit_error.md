## AWS codecommit 에러

### env
윈도우

### problem1
codecommit용 SSH 퍼블릭 키를 업로드하는 곳을 못 찾음

### solution1
IAM에서 사용자 생성 후 해당 사용자로 퍼블릭 키 업로드

(루트에서는 codecommit 권장 안하기 때문인듯)
### problem2
public 키 업로드 시 오류 발생하며 아래의 경고 메시지 출력
<span style=color:red>인식할 수 없는 퍼블릭 인코딩입니다.</span>

### solution2
ssh-ed25519 라서 안되는건가..? (이유는 몰겠음)

ssh-rsa로 키 만들기

```bash
ssh-keygen -t rsa # rsa로 지정
```