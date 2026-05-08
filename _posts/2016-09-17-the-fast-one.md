---
layout: post
title: System Design Guide for SW professionals
description: >
  도서 *요즘 개발자를 위한 시스템 설계수업* 에서 간단하게 정리한 내용들
tags: [Build]
---

시스템과 네트워크 영역이 고도화 되다보니 관련된 내용이나 최근 기술들에 대한 도서를 되도록 확인해보려고 한다.  [BOOKS][link]

### 1부 시스템설계기초 
시스템 설계의 기초 /분산 시스템의 속성 /분산시스템의 이론과 데이터 구조에 대해서 상세하게 설명이 되어 있다. 

### 2부 분산시스템의 핵심구성요소 
핵심요소인 DNS LoadBalancer Application GW 에 대한 내용들이다. DNS의 이해와 부하분산 및 확장된 Application 영역의 이해 
그리고 DB와 Storage, Caching에 대한 이해 MQ ... 

### 3부 시스템 설계 실전으로 들어가기 
이를 바탕으로 실전 시스템 설계로 들어간다. 저자 Dhirendra Sinha는 Google에서 매니저로 재직중이고 분산시스템의 설계과 다양한 경험을 갖추었고 저자 Tejas Chopra는 Netflix 엔지니어로 머신러닝 및 소프트웨어 엔지니어링의 전문성과 리더쉽을 보여주고 있다고 한다. 이 경험을 기반으로 실제 X서비스 Instagram, Google DOCS, Netflix 등 실제사례를 기술한다.  

## 분산시스템 속성 

* 일관성
* 가용성
* 허용성
* 지연시간




## 분산시스템 기본요소 

* DNS
* LoadBalancer
* Application Gateway

## 고수준 설계 탐구 
첫장의 머리말이다. 
*기능적 요구사항과 비기능적 요구사항, 서비스의 예상규모를 산정한 결과를 바탕으로 이제 X의 고수준 설계를 살펴보려고 합니다.* 


***



[docs]: ../docs/7.5.2/index.md
[link]: https://www.oreilly.com/library/view/system-design-guide/9781805124993/


