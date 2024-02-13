ㅠㅠㅠㅠㅠㅠㅠㅠㅠㅠS3에 접근이 안됨

This XML file does not appear to have any style information associated with it. The document tree is shown below.

```html
<Error>
<Code>AccessDenied</Code>
<Message>Access Denied</Message>
<RequestId>E415X18TYNNN35XP</RequestId>
<HostId>ayt1aOC/1u+NWB46GXtd2p4o6ouvv9hew6b0drZJLd2N6ncxRGm48/G3+ATlqqdtzFnCqdgYYL8=</HostId>
</Error>
```

## soln

[참고 1](https://velog.io/@rachelyu1025/AWS-S3-CloudFront-403-Access-Denied-%EC%98%A4%EB%A5%98-%ED%95%B4%EA%B2%B0)

1. 오류페이지 설정으로 해결 안됨
2. ..

[참고 2](https://rainbound.tistory.com/472)

1. S3 정적 웹 사이트 호스팅
2. cloudfront 배포 생성
   1. 원본 도메인 S3 연결
   2. 원본 액세스 > 원본 액세스 제어 설정 후 OAC 추가(혹은 선택)\
        이 경우, 제어 설정의 이름은 원본 도메인과 일치해야 함
   3. 생성된 cloudfront 원본의 정책 복사
   4. cloudfront에서 복사한 정책을 S3에 붙여 넣기

근데 왜 안되지....\
$\to$ 퍼블릭 액세스 차단 끄고, 전체 액세스 허용 -> 하니까 되네...

S3에 대한 직접 접근은 허용하지 않고, CloudFront 접근은 허용하도록 변경해보기!