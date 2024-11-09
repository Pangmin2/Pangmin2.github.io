---
layout: post 
title: Virtual DOM 기초
subtitle: React Virtual DOM
author: 팡민
categories: React
tags: React
top: 1
sidebar: []
---
## 서론
Virtual DOM에 대해 알아보기에 앞서, DOM이라는건 무엇일까?
DOM은 Document Object Model의 줄임말으로 하나씩 풀어서 해석해본다면

Document : 문서
Object : 객체
Model : 모델

즉, DOM은 문서 객체 모델로 해석되게 되는데, 여기서 문서는 프로그래머가 작성하는 HTML, XML 문서를 나타내게 되고
객체는 그런 문서들을 구성하는 각 요소를 객체형태로 다루기 위한 div 태그나, h 태그 등의 객체,
모델은 문서를 이루는 객체들 간의 관계 혹은 계층 구조를 나타내는 트리 형태의 모델을 뜻한다.

요약하자면 DOM이란 HTML 문서를 브라우저가 이해할 수 있는 객체의 트리 구조 모델이다.
JavaScript에서는 해당 DOM을 이용해 문서를 동적으로 추가하거나, 수정, 삭제를 수행하게된다.


## Virtual DOM 이란?
앞서 DOM에 대해서는 문서객체모델로 간략하게 설명했는데, 이번에는 Virtual DOM, 가상의 DOM 이라는 표현을 사용한다.
Virtual DOM은 이름 그대로 실제 DOM과는 다른 또다른 가상의 DOM을 의미하게 되는데,