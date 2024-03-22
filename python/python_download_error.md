## Python 명령어 안됨

### env
Windows10

python 공홈에서 설치

### problem
![Alt text](img/python_appstore.PNG)

python을 정상적으로 설치, 환경 변수까지 설정하였으나 위와 같은 현상 발생\
python 실행 파일 명령어로 인식을 하지 않고, 파이썬을 설치하는 app store로 이동

app store를 여는 alias로 지정되어 있기 때문인 것 같음..;
### solution
[땡큐 스택오버플로우](https://stackoverflow.com/questions/58754860/cmd-opens-windows-store-when-i-type-python)

```bash
Remove-Item $env:USERPROFILE\AppData\Local\Microsoft\WindowsApps\python*.exe
```