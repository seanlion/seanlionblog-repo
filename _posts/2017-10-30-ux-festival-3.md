---
layout:     post
title:      대학 축제 사이트를 만들어보자(3)
permalink: ux/17
description: 대학축제 사이트 기획 과정을 공유합니다.
date:       2017-10-30
summary:    대학 축제 사이트 기획 & 개발과정을 공유합니다.
category: 	서비스와 UX 습작
---

[대학 축제 사이트를 만들어보자 (1)](https://seanlion.github.io/ux/7)

[대학 축제 사이트를 만들어보자(2)](https://seanlion.github.io/ux/11)

지난 글들에서 왜 사이트를 기획하게 되었고 리서치 내용과 결과에 대해 살펴보았다. 오늘 글에선 정보 구조 설계, 화면 설계, 프로토타이핑 및 테스트에 대해 얘기해보겠다.

- - -

## IA를 짜보자

정보구조의 글만은 아니기에 짧게만 정보 설계를 짚고 넘어가자.

댄 섀퍼의 말을 빌리자면 정보 설계는 사용자들이 원하는 정보를 찾기 위해서 콘텐츠를 어떻게 구조화하고 이름 지을 것인지에 대한 분야이다. 우리가 어떤 웹사이트를 들어가도 메뉴를 볼 수 있고 그 메뉴 안에는 사이트만의 기준으로 정보들이 나열되어 있다. 이런 정보들의 구조를 설계하는 것을 Information Architecture(IA)라고 한다.
 
지난 시간에도 짧게 설명했지만 IA를 짜는 것은 굉장히 중요하다. 눈에 보이는 사용성 뿐만 아니라 사이트 이미지를 결정지을 수도 있기 때문이다. IA는 브랜드 이미지와 직결된다.

어떤 웹사이트들은 만드는 것 자체에만 정신이 팔리거나 의견이 난립해서 그 사이트를 만든 사람들만 보기 쉬운 사이트로 전락하기도 한다. 그래서 많은 사람들이 드나드는 웹 사이트일수록 정보 구조에 대한 문제를 고민해야 한다. 예를 들어 많은 고객들이 찾는 쇼핑몰 사이트에서 노트북을 찾기가 어렵다면 어떻게 되겠는가? 사용자는 열심히 노트북만 찾다가 결국 그 페이지를 나가버릴 것이다. 이처럼 공간 안에서 어떻게 정보를 표현할 것인가는 굉장히 중요하다. 결국 그것은 시간과 비용으로 직결되기 때문이다.


그래서 구조를 짤 때 다른 것보다 신경을 더 많이 썼다. 밑의 그림은 설계한 축제 사이트의 IA이다.
 
<br>

<p align ="middle">	
 <img src="/images/festival_ia.png" width = "100%">
</p>

{: refdef: style="text-align: center;"}
###### _축제사이트의 IA_
{: refdef}

<br>

#### 정보의 우선순위 

시각적으로 정보 구조를 만들기 위해 가장 우선적으로 고려한 요인이다. 왼쪽 -> 오른쪽으로 배치해 중요도를 표시했으며 서베이 결과를 토대로 만들었다. 

#### 트리 구조

일반적인 IA는 위에서 아래로 뻗어 나가는 트리 구조이다. 구조에는 좁고 깊은 Deep한 구조 넓고 얕은 Flat한 종류가 있는데 나는 1~2 뎁스로 구축해서 Flat한 구조로 만들었다.

#### 레이블링

사실 정보 구조를 설계 할 때 레이블링이 가장 어렵다. 의미가 직관적으로 다가와야 하며 막 지어서는 안되기 때문이다. 또한 웹에서의 피드백은 오프라인처럼 즉각적이지 않기 때문에, 처음 레이블을 붙일 때 많은 시간을 투자할 필요가 있다.

[IA에 대한 이정기님의 글](https://sites.google.com/site/studyux/ia/ia)에 따르면 레이블링 시에 다음과 같은 점을 고려해야 한다.

-주요한 레이블이 쉽게 눈에 띄는가? 그렇다면 그 이유는?

-예상치 못하거나 혼란한 부분이 있다면 이에 응당하는 설명이 따라붙어있는가?

-레이블에 대한 추가 설명을 얻기 위해서 클릭을 해야 하는가?

이런 기준에 맞춰 나도 초기에 설정한 레이블들 중 일부를 이후에 조금 바꾸었다.

- - -

## 화면 설계를 해보자

화면 설계에서 가장 고민했던 부분은 스크린 레이아웃이었다. 개발을 직접 하다 보니 레이아웃 스케치 시 구현 가능 여부도 고려해야 했기 때문이다. 

PC웹, 모바일 웹, 반응형, 적응형, 스크롤형, 고정형 레이아웃 등의 스크린 레이아웃에 대해 고민을 많이 했다. 우선 여기서 간단히 레이아웃의 종류에 대해 설명하고 넘어가겠다.

### 반응형vs 적응형


<br>

<p align ="middle">	
 <img src="http://indust.kr/wordpress/wp-content/uploads/2016/11/49000_29406_2831-600x374.jpg" width = "70%">
</p>

{: refdef: style="text-align: center;"}
###### _적응형 웹과 반응형 웹._
{: refdef}

<br>

#### 반응형

반응형 웹이란 가로 크기에 변화를 줄 때, 컨텐츠들이 사이즈에 맞춰 유동적으로 재배치 되는 웹 사이트의 형태이다. 마치 웹이 “너가 어떤 화면 크기를 가지고 있을지 몰라서 다 준비했어! 가지고 있는 화면 크기에 맞춰질거야!” 라고 외치는 것과 같다. 기본적으로 css 미디어쿼리(media-query)를 이용한다. 

일반적으로 반응형 웹이 적합한 사이트는 간단하고 심플한 사이트다. 블로그나 소개 페이지 같은 정보를 전달하는 역할의 사이트가 적합할 것이다. 그래서 동적이며 콘텐츠의 양이 방대한 사이트의 경우 반응형은 적절하지 않다. 쇼핑몰 사이트, 포털 사이트 등이 그렇다.


#### 주의사항

기본적으로 미디어 쿼리를 사용하지만 여기에 의존하면 안된다. 조건적인 로딩을 사용하여 현재 장치를 위해 필요한 자바스크립트만 로딩해야 한다. 브라우저는 기본적으로 모든 기기에 대한 css (스타일과 셀렉터) 전체를 로드하고 파싱(정보를 전송) 한다. 모바일 환경도 마찬가지이며 더 큰 스크린을 위한 CSS까지 다운로드하고 파싱하게 된다. 결국 그만큼 접속이 느려지게 되는 것이다. 그래서 필요한 CSS 미디어 쿼리만 로드해야 한다. 하지만 이 웹사이트의 경우 필요한 정보가 엄청 방대하진 않기에 그냥 진행했다.(그리고 일단 원칙은 알고 있는데 직접 개발해야 해서 그런지 필요한 쿼리만 로드하는게 힘들었다….)

<br>

#### 적응형

반면에 적응형 웹은 약간 다르다.

적응형 웹은 미리 정해진 몇 가지 화면 크기를 기준으로 두고 비율에 맞춰 페이지를 구성하는 방식이다. 
적응형은 클라이언트 쪽이 아닌 서버 쪽에서 사용자의 디바이스를 확인하고 그 디바이스 크기를 기초로 HTML 및 CSS코드의 배치를 결정한다.
화면에 담길 콘텐츠의 양을 조절하고 기기에 최적화된 디자인을 함으로써 가독성을 높일 수 있다.

행과 열로 표현하는(그리드 형태) 데이터 형태가 빈번하거나 시스템 성능이 중요한 웹 사이트의 경우에 적응형을 이용한다. 포털 사이트를 보시면 잘 아시겠지만 모바일과 pc의 정보 구조가 다르다.

<br>

<p align ="middle">	
 <img src="http://www.comworld.co.kr/news/photo/201606/49000_29405_2831.jpg" width = "70%">
</p>

{: refdef: style="text-align: center;"}
###### _네이버와 다음의 적응형 웹._
{: refdef}

<br>

#### 주의사항
우선 각 디바이스에 적절한 시스템을 각각 제작해야 하기때문에 비용과 효율성이 떨어진다. 또한 수정사항이 있을 경우 모두 수정·변경해야 하며, 새로운 디바이스가 시장에 나오면 이에 대한 적용을 해야한다. 이번에 나올 아이폰 X가 그런 예이다.

- - -

### 반응형으로 제작, 그 다음은?

기본적으로 멋쟁이 사자처럼에서 PC 웹 기준으로 개발을 배웠긴 했지만 모바일 퍼스트 시대에 살면서 모바일 웹을 기획하지않는 것은 말이 안 된다. 그러다보니 자연스레 처음부터 반응형 웹을 기반으로 레이아웃을 짜게 되었다. 

그 이후 또 한번의 갈림길에 섰는데 스크롤형 원 페이지 vs 기본적인 링크 이동형 페이지라는 레이아웃을 고려해야 했기 때문이다.

<br>

<p align ="middle">	
 <img src="http://wonpage.co.kr/wp-content/uploads/2014/12/%EC%9B%90%ED%8E%98%EC%9D%B4%EC%A7%80%EC%9B%B9%EC%82%AC%EC%9D%B4%ED%8A%B8%EB%9E%80.png" width = "70%">
</p>

{: refdef: style="text-align: center;"}
###### _원페이지 디자인. 이렇게 만들면 장점이 많다._
{: refdef}

<br>

이건 개발 가능 여부를 가장 먼저 따졌다. 물론 원 페이지가 더 장점은 많았다. 원 페이지 같은 경우 분명 자바스크립트를 이용한다. 동적인 형태이기 때문이다. 허나 제작 당시 팀원들 모두 다 자바스크립트를 그렇게 잘 하진 못했고 이해도도 많이 부족했다. 기본적으로 배워온 것이 a태그(링크) 기반의 이동형 페이지였기 때문에 기본형 페이지를 선택할 수 밖에 없었다. 물론 학습하거나 외부 코드를 끌고 와서 여차저차 할 수 있었겠지만 ‘거기에 드는 학습 및 구축 시간’과 ‘원페이지와 이동형 페이지에 대한 사용자들의 이해도 차이가 거의 없을 것이다’를 생각하니 이동형 페이지가 더 나아보였다. 

화면 설계는 우선 비주얼 디자인 보단 디자인 스펙을 추가한 와이어프레임 제작, 아이덴티티 컬러만 세우고 넘어갔다.(비주얼 디자인은 프로토타이핑 & 개발단계에서 진행했다.) 동시에 관련 정보의 텍스트를 고안하고 이미지를 수집했다. 이미지는 총학생회와 협의 하에 제작했다. 중간에 멤버가 디자이너 한 명을 영입(?)해 좋은 이미지를 만들 수 있었다. 

여기서 가장 고려한 점은 모바일 웹의 햄버거 버튼이다. 기본적으로 햄버거 버튼의 장단점을 알고 있었고 잘 안 쓴다는 추세라는 걸 알고 있었지만 아무래도 웹에서는 그 추세가 적용될 수 없다고 생각했다. 앱 같이 tab같은걸 둘 수 없으니 정보 구조를 보여줄만한 다른 방법이 없었다. 

<br>

<p align ="middle">	
 <img src="/images/fest_wireframe.png" width = "70%">
</p>

{: refdef: style="text-align: center;"}
###### _작업했던 와이어프레임 뭉치들._
{: refdef}

<br>


아이덴티티 컬러는 총학생회를 상징하는 버건디 색을 선택했고 배경,푸터 색은 흰색 계열 색으로 정했다. 
(학교를 상징하는 컬러가 딱히 없어서 아이덴티티 컬러는 대체제로 정했다.)

<br>

<p align ="middle">	
 <img src="/images/fest_colorset.png" width = "70%">
</p>

{: refdef: style="text-align: center;"}
###### _페이지 컬러셋._
{: refdef}

<br>

- - -

## 프로토타이핑 & 테스트

와이어프레임 이후 바로 프로토타이핑을 만들고 테스트를 진행했다. 어도비 xd를 사용해 모바일 
상에서 실사에 가까운 프로토타입을 구현했다. (지금 보니 푸터가 좀 두드러진 느낌이다. 만든거 세상에 그렇게 알리고 싶었나.)

<br>

<p align ="middle">	
 <img src="/images/fest_proto.png" width = "30%">
</p>

{: refdef: style="text-align: center;"}
###### _프로토타입 결과물의 일부. gif로도 올려보고 싶다._
{: refdef}

<br>

그 이후 사람들에게 테스트를 진행했다. 학교 학생들 3명을 대상으로 특정 Task 수행을 던져주고 미니멀한 테스트를 수행해보았다. 

#### 부여한 Task

1.축제 두번째 날의 축제 프로그램 ‘OO’을 신청 해보시오.

2.OO학과의 주점 메뉴를 찾아보시오.

학생들은 대개 잘 task를 수행했다. 햄버거 메뉴에 대한 인지도 잘 했고 원하는 정보를 빨리 캐치해냈다. 다만 중간중간 다음과 같은 문제들이 발견되었다.

#### 문제점

1.홈 화면에서 디바이스 크기에 따라 스크롤 가능 인지 여부가 불투명하다.
2.프로그램 신청이 끝나면 뭘 보여주는지 모르겠다.
3.학과별 보드 리스트의 간격이 너무 좁아서 클릭하기가 힘들다.

곧 바로 수정에 들어갔고 다음과 같은 방법으로 문제를 해결했다.

#### 해결

1번 - 첫 이미지 크기를 수정해 어떤 디바이스이든 간에 밑에 나올 항목이 화면에 걸치게 만듬, 스크롤 인지가 가능해짐.

2번 - 이해관계자와의 협의 문제(총학생회), 프로그램 신청 이후 사용자들이 받을 정보를 제작 후 링크 연결.

3번 - 보드 리스트의 간격을 2배 늘려서 클릭 가능 영역 확대

개발 전에 테스트를 진행한 것이 큰 도움이 되었다. 아마 사이트를 개발 완료하고 이러한 문제가 터졌으면 급하게 수정을 해서 완성도가 떨어지거나 효과적으로 개선하지 못했을 것이다.

이 경험으로 프로토타이핑의 중요성을 알게 되었다. 문제점을 캐치해내고 빠르게 수정할 수 있기 때문이다. 배웠던 이론적 지식을 실제로 수행 해보니 그 중요성을 더 크게 느낄 수 있었다. 

프로토타이핑을 진행 한 이후 바로 실제 개발에 들어갔다. 개발 요소 정의, 사용했던 소스 등에 대해선 다음 시간에 이야기해보도록 하겠다. 
