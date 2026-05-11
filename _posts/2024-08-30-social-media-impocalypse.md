---
layout: post
title: Massive system Architecture. 대규모 시스템 설계
description: >
  도서  *가상면접 사례로 배우는 대규모 시스템 설계기초*  에서 정리된 내용과 참고할만한 사항들을 간단하게 정리했다.   
tags: [Build]
excerpt_separator: <!--more-->
---

## Massive System 
* 서버규모 확장 
  * Server 규모가 증가하면 Scale up/out 에 대한 고려 
  * DB다중화 대부분 `write`보다는`read` 상황에 맞는 설계
  * Cache에 대한처리 동일호출/빈도에 참조되는 Eviction 정책
* CDN Contents 전송에 대한 비용/기한/장애 대처방안 필수고려

<!--more-->

**NOTE**: 가상면접 사례로 배우는 대규모 시스템 설계기초 [인사이트](https://blog.insightbook.co.kr/2021/07/22/)
{:.message}

## Stateless 한 웹계층 
* Session 에 대한 고려 Sticky Session 
* Stateless 설계 - 단순 안전 규모확장이 쉬운 장점  
* 적용된 설계안 참고 

## DataCenter 데이터센터
* 다중 데이터센터 아키텍처를 설계하기 위한 사항들
* Routing 우회 /GeoDNS 
* DB동기화 및 Deploy일관성 

## MQ MessageQue 
* MQ 처리에 대한 고려 
* 비동기적 처리 

## Log, Metric, Automation 로그 메트릭 자동화 
* Log 집합체 문제를 보다쉽게 
* Metric 각종 지표들 수집  
* 자동화 도구들 

***

[See *System Design Interview* on Youtube](https://www.youtube.com/watch?v=i7twT3x5yv8)유튜브참고영상


[docs]: ../docs/7.5.2/index.md
