---
title: "유니티 타임라인 & 씨네머신 튜토리얼"
categories:
  - GameDevelopment
tags:
  - unity
  - cinemachine
  - timeline
  - tutorials
---

![Title Image, Unity Timeline and Cinemachine Tutorials](/assets/images/xbox-1602822_1920.jpg "Unity Timeline and Cinemachine Tutorials")

#### 튜토리얼 목차
* [타임라인과 씨네머신 튜토리얼 소개 (돌리트랙 포함)](#content-1)
* [타임라인 소개](#content-2)
* [씨네머신 소개](#content-3)
* [씨네머신, 클리어샷](#content-4)
* [타임라인 시작하기](#content-5)
* [타임라인, 트랙의 이해](#content-6)
* [타임라인, 애니메이션 클립으로 작업](#content-7)


#### 시작하기

유니티 최신 기능인 타임라인과 씨네머신을 이용해서 간단한 30초 짜리 컷씬 예제를 만들어 볼 것이다.
(영문 유니티 튜토리얼을 참고하였다. https://learn.unity.com/)
그 밖의 돌비트랙, 버추얼카메라에 대한 개념도 학습하게 된다.

예제 프로젝트는 아래 링크에서 다운로드 받을 수 있다.
https://www.dropbox.com/s/uqh6iurd646mvwt/TimelineAndCinemachineTutorial-WG.zip?dl=0

아래, 유니티 유럽에서 제작한 타임라인&씨네머신 관련 동영상도 확인하자.
https://www.youtube.com/playlist?list=PLX2vGYjWbI0RvixSO2Ko08axqABaKzGq_


#### 1. 타임라인과 씨네머신 튜토리얼 소개 (돌리트랙 포함) {#content-1}

##### 1) 버추얼 카메라 추가, 카메라에 대상 추적 기능 설정하기

예제 프로젝트를 유니티에서 연다.(유니티 버전 2019.1.4f1 사용)  

예제의 TimelineForest-Start 라는 유니티 씬 파일을 연다

패키지 매니저에서 씨네머신 패키지가 최신으로 설치되어 있는지 확인

CM_Cameras 라는 빈 게임오브젝트를 씬에 추가

버추얼 카메라 생성하기  
* 유니티 메뉴, Cinemachine -> Create Virtual Camera

버추얼 카메라의 LookAt, Follow 설정하기  
* 씬의 캐릭터 객체의 FollowTarget 하위 객체를 버추얼 카메라의 LookAt과 Follow에 연결(드래그앤드랍)

버추얼 카메라의 Body Follow Offset 설정 : 버추얼 카메라가 캐릭터의 등 뒤 적절한 위치에 오도록 설정

포스트 프로세싱 이펙트(DOF 등 설정)
* 메인 카메라에 CinemachinePostFx 콤포넌트 붙이기  
* Profile에 이미 만들어져 있는 Post-Profile이라는 이름의 애셋을 연결
* FocusTracksTarget을 체크하여 자동으로 현재의 FollowTarget에 맞게 DOF 설정되게 하기

영상 (9:48)까지 보았음


##### 2) How to add and animate the Cinemachine Dolly Track 

##### 3) How to sequence cameras with Timeline and Cinemachine 

##### 4) How to animate game object properties with Timeline 

##### 5) How to add music and screen fading to your animation



#### 2. 타임라인 소개 {#content-2}


#### 3. 씨네머신 소개 {#content-3}


#### 4. 씨네머신, 클리어샷 {#content-4}

#### 5. 타임라인 시작하기 {#content-5}

#### 6. 타임라인, 트랙의 이해 {#content-6}

#### 7. 타임라인, 애니메이션 클립으로 작업 {#content-7}


