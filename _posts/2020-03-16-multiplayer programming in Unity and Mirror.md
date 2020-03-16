---
title: "멀티플레이 게임 개발 in 유니티 & 미러(Mirror) (1)"
categories:
  - Game Programming
tags:
  - unity
  - network-programming
  - mirror
---

# 멀티플레이 게임 개발 in 유니티 & 미러(Mirror) (1) 

## 참고 링크

* [미러 에셋스토어][mirror-assetstore]
* [미러 유튜브 강의][mirror-youtube]
* [미러 github][mirror-github]
* [미러 유니티 포럼][mirror-unityforum]

## 미러(Mirror) 에 대한 소개

유니티용으로 제작된 하이 레벨 Network API
하위 레벨에서 Telepathy라는 C# TCP Library를 이용하고 있다.
미러와 텔레파시 모두 vis2k라는 팀에서 제작하였는데, 심플하면서도 강력한 네트웍 기능을 제공한다.

## 특징

MMO스케일 테스트 완료 (1000개 접속 무리없이 소화)

쉬운 사용과 신뢰성

서버구조와 클라이언트 구조가 동일

클라-서버간 커맨드 통신 방식

서버-클라간 RPC 통신

동기변수(SyncVar): 자동적으로 상태 동기화

미러는 유니티의 기존 네트워킹 시스템인 UNET(지금은 지원 안됨)의 대안 라이브러리로 사용할 수 있다. 

호환 유니티 버전: Unity 2018.4 LTS and 2019



[mirror-assetstore]: https://assetstore.unity.com/packages/tools/network/mirror-129321?locale=ko-KR
[mirror-github]: https://github.com/vis2k/Mirror
[mirror-unityforum]: https://forum.unity.com/threads/mirror-networking-for-unity-unet-replacement.425437
[mirror-youtube]: https://www.youtube.com/watch?v=oR9P0gSaAOU&list=PLkx8oFug638oBYF5EOwsSS-gOVBXj1dkP&index=2
