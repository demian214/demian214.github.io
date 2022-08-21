---
layout: post
title: Android Google Map 서비스 (1)
subtitle: 위도, 경도를 이용한 좌표값 이용하기
categories: Android
tags: Android Java
---

## 위치정보(위도, 경도, 고도)

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/62/Latitude_and_Longitude_of_the_Earth.svg/2880px-Latitude_and_Longitude_of_the_Earth.svg.png" title="" alt="Earth" data-align="center">

[위도](https://ko.wikipedia.org/wiki/%EC%9C%84%EB%8F%84 "위도")는 주어진 [지구](https://ko.wikipedia.org/wiki/%EC%A7%80%EA%B5%AC "지구")의 표면 지점의 수직선(추선)과 적도면이 이루는 각이다. 같은 [위도](https://ko.wikipedia.org/wiki/%EC%9C%84%EB%8F%84 "위도")의 지점을 연결한 선은 위선이라고 부르며 적도에 평행한 동심원이 된다. [북극](https://ko.wikipedia.org/wiki/%EB%B6%81%EA%B7%B9 "북극")은 북위 90°이다. 0° 위선은 적도이며 [구면 좌표계](https://ko.wikipedia.org/wiki/%EA%B5%AC%EB%A9%B4_%EC%A2%8C%ED%91%9C%EA%B3%84 "구면 좌표계")의 기본 평면이 된다. 적도는 지구를 북반구와 남반구로 분할한다.

[경도](https://ko.wikipedia.org/wiki/%EA%B2%BD%EB%8F%84 "경도")는 주어진 지구의 표면 지점을 지나 [북극](https://ko.wikipedia.org/wiki/%EB%B6%81%EA%B7%B9 "북극")부터 [남극](https://ko.wikipedia.org/wiki/%EB%82%A8%EA%B7%B9 "남극")까지 그은 경선과 [본초 자오선](https://ko.wikipedia.org/wiki/%EB%B3%B8%EC%B4%88_%EC%9E%90%EC%98%A4%EC%84%A0 "본초 자오선")이 이루는 각이다. 모든 경선은 반원을 그리며 평행되지 않고 북극과 남극에 한데 모인다.

[런던](https://ko.wikipedia.org/wiki/%EB%9F%B0%EB%8D%98 "런던") 근교의 [그리니치 천문대](https://ko.wikipedia.org/wiki/%EA%B7%B8%EB%A6%AC%EB%8B%88%EC%B9%98_%EC%B2%9C%EB%AC%B8%EB%8C%80 "그리니치 천문대")의 바로 밑을 통과하는 자오선([그리니치 자오선](https://ko.wikipedia.org/wiki/%EA%B7%B8%EB%A6%AC%EB%8B%88%EC%B9%98_%EC%9E%90%EC%98%A4%EC%84%A0 "그리니치 자오선"))이 [본초 자오선](https://ko.wikipedia.org/wiki/%EB%B3%B8%EC%B4%88_%EC%9E%90%EC%98%A4%EC%84%A0 "본초 자오선")에 선정되고 있다. 이것보다 더 동쪽에 있는 지점은 [동반구](https://ko.wikipedia.org/wiki/%EB%8F%99%EB%B0%98%EA%B5%AC "동반구"), 서쪽에 있는 지점은 [서반구](https://ko.wikipedia.org/wiki/%EC%84%9C%EB%B0%98%EA%B5%AC "서반구")에서 있다. 그리니치의 대척지의 [경도](https://ko.wikipedia.org/wiki/%EA%B2%BD%EB%8F%84 "경도")는 서경 180°이며 동경 180°이다.

## 다양한 위치정보

도.분.초(일상에서의 위치정보) → Location 객체(도.실수값) → LatLng 객체(지도에서 좌표값)

## 작동구조

LocationManager

↓

LocationProvider - 최적의 위치정보 제공자    

- GPS
- Network

위치정보를 제공받는다.

↓

<<interface>>

LocationListener

① 직접수신 → 사용자가 지도에 표식 남기기

② 자동으로 표시

## 지도(Map)

→ 맵서버(Google, Daum, Naver)
회원가입/인증 → 인증키 발급
