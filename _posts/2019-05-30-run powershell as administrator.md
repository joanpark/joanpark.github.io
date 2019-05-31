---
title: "파워셸 관리자 권한으로 실행하기"
categories:
  - Programming
tags:
  - powershell
  - node.js
---


node.js 프로그래밍을 하다보면
터미널(파워셸[^1])에 관리자 권한을 부여해야 하는 경우가 있다.(특정 모듈 설치시)

예를 들어, 이렇게 윈도우즈 빌드 툴 같은 걸 설치할 때 관리자 권한이 필요한데

```
npm install --global --production windows-build-tools
```

두 가지 방법이 있다.

1. 윈도10에서 검색으로 powershell을 찾아, 파워셸을 열 때, 마우스 오른쪽 버튼을 클릭하고 '관리자 권한으로 실행'


2. vs code 안에서 파워셸을 쓰는 경우가 많으니, 아래 링크와 같이 vs code 실행파일의 호환성 설정안에서 실행시 '관리자 권한'을 주면 된다.
https://superuser.com/questions/1255775/give-administrator-privileges-to-existing-powershell



### 참고

[^1]: 파워셸 더알아보기

    [파워셸 도움말](https://docs.microsoft.com/ko-kr/powershell/scripting/overview?view=powershell-6)

    [위키피디아 파워셸](https://ko.wikipedia.org/wiki/%EC%9C%88%EB%8F%84%EC%9A%B0_%ED%8C%8C%EC%9B%8C%EC%85%B8)

    [MS윈도 명령프롬프트 사라지나](https://news.naver.com/main/read.nhn?mode=LSD&mid=sec&sid1=001&oid=092&aid=0002106773)
