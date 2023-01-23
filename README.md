# goodjin92.github.io

[goodjin92.github.io](https://github.com/goodjin92/goodjin92.github.io)



Hugo를 활용한 블로그 구성 (PaperMod 테마 사용)

아래는 블로그 활용에 대한 간단한 방법 정리



## 1. 새글 쓰기

Powershell에서 아래 명령어 입력

```powershell
hugo new post/draft.md
```



## 2. 내부 테스트

1. ```power
   hugo server  # 일반적으로 볼 때
   or
   hugo server -d  # Draft 포함하여 볼 때
   ```

2. http://localhost:1313/ 에 접속

3. 만약 포트를 바꾸고 싶은 경우 아래와 같이 입력하기 (-p : 포트 변경)

   ```powershell
   hugo server -D -p 80
   ```

   

## 3. 블로그에 글 게시하기

1. blog 폴더에서 powershell 실행

2. 아래와 같이 입력하기

   ```powershell
   ./deploy.sh "comment"
   ```

​		[deploy.sh 코드 보기](https://github.com/goodjin92/blog/blob/main/deploy.sh)



## 4. 게시글에 이미지 첨부하기

[링크 참고하기](https://velog.io/@uzchu/Github-%EB%B8%94%EB%A1%9C%EA%B7%B8-image-%EC%82%BD%EC%9E%85%ED%95%98%EA%B8%B0)