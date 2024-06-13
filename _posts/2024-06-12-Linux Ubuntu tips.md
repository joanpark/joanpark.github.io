---
title: "리눅스(우분투) 각종 팁"
categories:
  - tips
tags:
  - Linux
  - Ubuntu
  - OS
---

# 팁 모음

 우분투 22.04.4 버전을 설치해서 사용 중이다.
 (주로 VitualBox같은 가상화 툴로 게스트 OS로 사용하고 있다)

## 버츄얼박스(VirtualBox) 우분투 터미널 안 열림 해결 방법

버츄얼박스에 우분투를 설치했는데 터미널(Terminal)이 열리지 않는 현상이 발생했다. 이러한 현상은 무인 설치(Unattended Install)를 진행하면 발생하는 현상

Settings -> Region & Langauage -> Language를 English(United States)에서 'English(Canada)'로 바꿔준다

로그아웃 후 다시 로그인, 끝!

## 한글 입력 세팅

- sudo apt upgrade ibus-hangul

- Settings -> Keyboard -> Input sources
입력소스를 그냥 Korean이 아니라 Korea(Hangul) 로 해줄 것!

-한영 전환키 : Super(윈도키 등) + space


## python 명령어를 인식 못할 경우 (python3는 설치되어 있는데도)

python-is-python3을 설치한다.

-sudo apt install python-is-python3 

