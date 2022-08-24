---
layout: post
title: 가상기기(AVD) 안에 이미지 파일 넣기
subtitle: ChatApp 토이 프로젝트
categories: Android
tags: Android Java Chat
---

프로젝트를 테스트하기 위해 에뮬레이터 안에서 사용할 이미지 파일이 필요할 때가 있다. 그 방법을 알아보자

1. 프로젝트를 실행할 가상기기(AVD)의 사양확인.
   
   - 설정된 용량에 비해 큰 파일이 저장되면 가상기기가 작동을 멈추는 에러가 발생한다.
   
   -  넉넉히 설정할 것(8GB 이상 권장).

2. 장치 파일 탐색기(Device File Explorer)를 열고 sdcard > Pictures 폴더 안에 이미지를 넣어준다.

3. sdcard 폴더를 우클릭하여 동기화(Synchronize)를 실행시킨다. 
