---
layout: post
title: Infrastructure Architecture 
description: >
  인프라 아키텍처에 대해서 OSI Level 계층별로 간단하게 정의하고 고려해야할 사항들에 대해서 다시한번 Reminder 해보려고한다. 문제 발생시에 항상 단계별로 접근해서 확인해야하는 기계적 행동반복과 이를 통해서 예기치 못한 사항에 대응할 수 있는 사전 모의 TEST와 같은 느낌이랄까.....[NETACAD](https://www.Netacad.com).
tags: [Build]
excerpt_separator: <!--more-->
---

## Features
Infra Architecture, 설계시에 OSI계층별로 고려해야할 사항들에 대해서 간력하게 단계별로 정리

OSI 7Layer Level include:

* Physical 계층 / Hardware 직접연결-이중화(Redundancy) 전원 회선 NIC & 그리고 성능용량 (Capacity)
* DataLink 계층 / 네트워크 내부통신 MAC:VLAN:LOOP Avoidance
* NETWORK 계층 / IP Address설계 Routing Firewall VPC etc....운영성 확장성 보안 
* Transport 계층 / TCP UDP LoadBalancer Connection관리
* Session 계층 / Login API Session WEB Socket
* Presentation 계층 /  TLS 암호화  DATA Format 성능최적화 
* Application 계층 / 실서비스 WEB API DB Cache MQ 
* 핵심고려사항 서비스연속성 Cache전략 DB설계 비동기처리 운영 배포 

<!--more-->


**NOTE**: 실제 설계시 중요한 사항들 OSI전체를 관통하는 핵심들에 대해서 정리

{:.message}

## Availabillity 가용성
어떤 환경에서도 서비스가 정상적으로 유지될 수 있는지.. 이로 인해 IDC에 인프라를 설계했지만 IDC장애시에도 무용지물이 되었다. 카카오에 대한 [장애회고](https://www.youtube.com/watch?v=15giy9e72c4) 결국은 Multi-AZ 가용영역 /Failover /Auto Healing 자동복구

## Scalability 확장성 
Traffic 증가에 대한 대응.. 40G BW로 설계했는데 순간적인 폭증으로 100G 이상의 트래픽이 몰린적도 있었고 C class 대역으로 할당했다가 IP설계가 충분하지 않은 상황도 발생했다. 결국에는 Horizontal scaling /Stateless /Cache 

대부분 서비스의 규모가 점차 팽창하고 성장하다 보면 기술부채가 생기기 마련이다. 기술부채로 인한 딜레마 상황에 빠지게 된다. 수평적 확장을 할 수있는 설계가 미리되어 있다면 좋겠지만 결국에는 길고 긴 Migration 작업을 거치게 된다. 

수평적 확장이 가능하도록 Session Login 등등 Stateless 핵심조건인데 선구안적인 설계였다면 박수를 쳐주고 싶다. 현실은 쉽지 않다는...

## Security 보안 


### Rule 기본원칙 
Least privilege /Zero trust 그리고 /Network segmentation

This includes:

* 최소권한 필요한 만큼만 허용해야한다. 하지만 안된다고 시다릴 것이다. 
* 아무것도 신뢰하지 말고 모든 것을 검증.. 그렇게 만들어야 한다. 
* 네트워크 세밀하게 분할해야 한다. 그런데 네트워크 작업하기가 가장 불가능
* 가장 어렵고도 긴 Mission 이다. 100:0 의 치킨런 싸움이다. 

## Performance 성능 
최종적인 서비스 영역이던 내부구성요소이던지 간에 지속적인 성능을 발휘하려면 결국에는 병목을 제거해야 한다. `Bottleneck`:

~~~yml
CPU: CPU Schedule 
Disk: DISK I/O
Network: https://www.cisco.com
DB: RDB vs NoSql Replication Sharding Backup 
~~~

## 추가적인 사항들... 운영 모니터링 비용 DR 
이외 추가적인 사항들로 운영성 모니터링 비용과 복구전략 유연성 자동화등에 대한 고려가 되어야 하지만 이상적인 항목이 되는 경우가 많다. 하지만 운영과 모니터링 DR 복구전략에 대해서는 명확한 대비를 해야한다. 

1.  운영성 Operability 
    서비스 연속성을 유지하기 위해서는 가장 중요한 항목이다. 

    

    ~~~yml
    Automation: 자동화
    Iac: Code 관리
    Monitoring: 실시간 각종 Tools, 
      ~~~

2.  관측성 Observability
    문제 원인은 추적 가능해야 한다. 

    

    ~~~yml
    Log:
    Metric: 
    Trace: 
    ~~~

3.  비용 Cost
    어쩌면 이게 더 가장 중요한 항목이다.  Cloud 에서는 특히 

    ~~~yml
    Cost: 비용합리성
    Scale: Forecast 
    Tier: Hybrid? Cloud?  
    ~~~

4. 복구전략 DR

   ~~~yml
   Multi_DR: 아무리 강조해도 지나치지 않다.
   Replication: 실시간 동기화는 어떻게 할지 
   Backup: 백업은 잘 되고 있습니까?
   ~~~


[docs]: ../docs/7.5.2/index.md
[tag]: http://www.minddust.com/post/tags-and-categories-on-github-pages/
