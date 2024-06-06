---
title: "터미널에서 git / github 사용해보기"
categories:
  - tips
tags:
  - git
  - Github
  - terminal
---
# 터미널에서 git / github 사용해보기

안녕하세요 오늘은 터미널(쉘이라고도 하죠)에서 깃을 사용하는 법을 정리해보겠습니다. 😀 💻

편리한 Github Desktop 이나 SourceTree 같은 편리한 깃 클라이언트 프로그램들이 있지만 
때로는 터미널에서 깃을 다루어야 할 때가 있죠. 오늘은 터미널에서 ssh 방식을 이용해 깃을 
사용하는 방법을 정리해봅니다.

## 터미널을 연다 

## git 을 설치한다 (sudo apt-get install git)

```
$> sudo apt-get install git
```

깃을 설치했으니 바로 깃허브 리포지터리에서 뭔가를 다운로드(clone) 해 볼 수 있겠죠?
그러나 

> remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.

이런 에러가 아마도 뜰 것입니다. 정책상 깃허브에서 이제는 터미널에서 패스워드로 인증하는 방식은 없앴기 때문이죠.
저 링크를 따라가보면 ssh 방식을 사용하라고 안내를 할 것입니다.

## git ssh 설정을 한다.

1. cd ~/.ssh 명령으로 디렉토리 이동을 합니다.

2. ssh-keygen 명령으로 ssh key를 생성합니다

```
$> ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
3. ls 명령으로 확인해보면, id_rsa, id_rsa.pub 두 개 파일이 생성된 것을 볼 수 있습니다.

* 참고는 rsa는 암호화 알고리즘을 말하는 것으로 알고리즘을 만든 사람들의 이름을 따서 붙인 이름입니다.
(Rivest-Shamir-Adleman (RSA) encryption algorithm)

4. cat id_rsa.pub 명령으로 키를 확인합니다. 
ssh-rsa 로 시작해서 이메일 주소로 끝나는 긴 암호화된 문자열이 나옵니다. 

이것을 복사해서 깃허브에 연결해주어야 합니다.

4. 깃허브 계정 설정에서도 ssh key를 새로 생성하고, 위의 터미널에서 생성된 키를 복사하여 연결해준다.

> github account setting -> ssh and gpg key 항목 -> new ssh key -> 복사한 키 넣어주기

## 깃 클론(clone) 해보기

```
git clone git@github.com:[username]/[repository name].git
``` 

이제 저장소에 있는 파일들이 잘 받아 지는 것을 볼 수 있습니다.

## 깃 커밋(commit) 해보기

클론을 할 때는 물어보지 않았지만, 처음 커밋을 할 때는 신원 정보(이메일과 주소)를 요청하는 메시지를 보게 될 것입니다.
아래와 같이 설정해주시면 됩니다.

> git config --global user.email "you@example.com"
  git config --global user.name "내 이름"

## 터미널에서 깃 명령어 정리 

자 이제 기본적인 설명은 다 된것 같으니. 깃에서 자주 쓰이는 기본 명령어들만 정리해보겠습니다.

* git clone
* git add 
* git add . : 이렇게 점을 추가해서 명령을 내리면, 변경된 모든 파일을 커밋 목록에 추가한다.
* git commit -m "메시지"
* git push
* git pull 

깃 클라이언트 프로그램을 써 본 분들은 위 내용만 보아도 어떤 명령인지 알 수 있겠죠.😀

