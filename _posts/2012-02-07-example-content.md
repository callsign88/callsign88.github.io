---
layout: post
title: Example content
description: >
 [Default] DEV/Build Blog Post 오랜기안 작업하면서 정기점검이나 대규모 작업 장애에 대처하면서 발생한 각종 Coldcase에 대한 기록들 
tags: [Dev]
author: author2
canonical_url: http://hyde.getpoole.com/2012/02/07/example-content/
---

Connected 란 의미를 정확히 알지도 못한체 <a href="#">Network Machine</a>, 대규모 트래픽을  *Control&handling.* 하게 되었다. CLI cmd 하나가 어떤 치명적인 영향을 미칠지도 모른체... 수많은 LAN Cable 하나가 원인을 알수 없는 접촉불량과 손상으로 인해서 예기치 못한 장애가 발생했을 때 어떤 것을 해야할 지 도 모른체 

> 대규모 Server System 이전 및 Network Backbone Switch의 작업으로 인해서 단계별 Scnario 와 Protocol을 확정하고 할당된 영역의 작업을 진행하고 있을 때 장애가 발생했다. 

Network 장애와  **Network Fail** 순간적인 트래픽의 급증이 발생해서 모든 Alarm Sign이 미친듯이 전송되고 손에서 진동이 멈추지 않았다. 하지만 어떤 것을 해야할지도 전혀 모른체 당황하고만 있었다.

## NETWORK WORK PROTOCOL

Network작업에 대한 Gary A. Donahue 의 "Network Warrior" 의 몇 가지 격언들이 생각나서 간단하게 내용을 기재해본다. [Developer Network](https://www.gad.net/).

- Maxim#1. Network designs are based on Politics, Money, and The right way to do it—in that order.
- Maxim#2. The only valid reasons to change aproperly sized pro-duction network are Simplification, Standardization, and Stabilization.
- Maxim#3. IT projects that lower costs, increase performance or capacity, or increase reliability.


이 격언들은 네트워크 업무를 수행하면서 한번 더 생각하게 하고 결정을 참고하는 많은 도움이 되었다. 


#### Human Error 인적오류 
Human error can be one of the hardest problems to track, and, once discovered,may
be almost impossible to prove.

#### Mutiple Componenet Faulure 다중 복합장애 
Many networks are designed to avoid single points of failure.

#### Disaster Chains 장애체인
When one device fails, another device takes over.

#### No Failover Testing 페일오버 테스트 부재 
Had failover testing been done, the problem would have been found during testing
andtheoutageavoided.

#### Trouble Shooting 문제해결
The best resolutions were the ones that happened quickly and weren’t necessitated by my mistakes..

#### Remain Calm 침착함
The more stressed you allow yourself to become, the longer the outage will last.

#### Actions 행동들
구체적으로 추가해 진행해야할 `Actions` 행동들에 대해 나열해본다. 

// Log Your Actions                   로그기록
// Find Out What Changed              직전에 변경된 사항들이 무엇인지 
// Check the Physical Layer First!    물리 Layer 단계부터 체크시작
// Assume Nothing; Prove Everything   단정짓지 말자 
// Isolate the Problem                문제는 분리해서 객관적인 시각으로    



### Lists

위에 더해서 추가적으로 사고적 측면과 경험치에서의 참고할만 목록들이라고나 할까 ...

* Don’t Look for Zebras!
* Do a Physical Audit.
* Escalste.
* Troubleshooting in a Team Environment.
* The Janitor Princile. 

이런 경험적인 원칙들에 대해서 미리 생각해놓고 어떤 예기치 못한 상황에 직면하게 되었을 때 당황하지 말고 침착함을 유지하면서 단계별로 진행해나간다면 아주 이상적인 상황이 될 것이다. 현실은 그러하지 못하지만... 



## Ends 

1. Why Everything Is Messed Up --- 모든 것이 엉망인 이유 (이유가있다. 이해하자)
2. How to Sell Your Ideas to Management --- 경영진과의 관계(Ideas 판매)
3. When to Upgrade and Why --- UPGRADE 의 시기와 이유 (비용집행의 정당성) 
4. The Dangers of Upgrading --- UPGRADING 의 위험성 (작업의 책임과 무결성)
5. Valid Reasons to Upgrade --- UPGRADE 를 해야하는 유효성 (기술개선과 서비스적 효용 )
6. Why Change Control Is Your Friend --- 변화가 너의 친구인 이유 (지금이 영원할수는 없다)
7. How Not to Be a Computer Jerk --- 컴덕이 되지는 말자! (컴덕만큼이나 존재의 이유가 필요하다)


지금까지 느낀 점들이다. 
