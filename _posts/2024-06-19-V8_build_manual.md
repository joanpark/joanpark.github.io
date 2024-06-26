---
title: "V8 빌드하기"
categories:
  - Library
tags:
  - V8
  - Javascript
  - Build
---

# Windows

미리 준비할 것:
- 파이썬 설치 (3.12.4)
- 7z 설치 (7z를 설치한 후, 7z.exe 위치에 대하여, 환경변수 경로 설정을 해준다.)
- ninja 빌드 툴 (https://github.com/ninja-build/ninja/releases) (설치 후, ninja.exe 위치에 대하여 환경변수 경로 설정을 해준다)
- ** 모든 환경 변수, 경로는 계정 변수(path) 아닌, 시스템 변수(path)로 할 것

$> powershell -command "Invoke-WebRequest https://storage.googleapis.com/chrome-infra/depot_tools.zip -O depot_tools.zip"

$> 7z x depot_tools.zip -o*

$> set PATH=%CD%\depot_tools;%PATH% (즉, depot_tools, 환경변수 경로 설정을 해준다)

visual studio 2019 community 설치  
visual studio installer 실행 
  - c++를 사용한 데스크톱 개발
  - 설치 세부정보
    - 최신 빌드 도구용 C++ ATL
    - 최신 빌드 도구용 C++ MFC

windows SDK 10.0.19041.0 설치  (winsdksetup.exe)
(https://developer.microsoft.com/ko-kr/windows/downloads/sdk-archive/)
- Debugging tools for windows 포함 시킬 것

$> set GYP_MSVS_VERSION=2019 && set DEPOT_TOOLS_WIN_TOOLCHAIN=0

$> gclient config https://github.com/ncsoft/v8.git

$> gclient sync --with_branch_heads -r 9.7.106.9999
(이 시점에 파이썬 설치가 되어 있어야 한다)

$> cd v8

$> gn gen out/x64.release -args="v8_use_external_startup_data=false v8_monolithic=true v8_enable_pointer_compression=false v8_enable_i18n_support=false is_debug=false v8_static_library=true is_clang=false"

$> ninja -C out/x64.release v8_monolith


