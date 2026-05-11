---
layout: post
title: Related AI Projects 그리고 단상
description: >
  AI 시대로 진입하고 나서 시시각각 ms 단위로 변하고 있는 기술스택의 세상에서 여러가지 단상들에 대한 기록을 하고 있다. 무작위적으로 그때마다 Tweet처럼(이젠X) 추가하는 것이라 오히려 Blog기록이 더 귀찮겠지만 
tags: [Build]
---

우선 HW기술적으로 확인해야할 상황들이 꽤 많았다. Full Stack 의 기조를 유지한만큼 우선적으로 HW적 성능지표를 확인하고 싶었다. 얼마나 효율적으로 작업을 처리하는 지에 대한 기본 지표들 (Clock speed, IPC, Core개수, Threads, Cache 등등)과 같이 GPU 동작하기 위한 HW설계 및 지표들 

~~~
GPU Memory 와 LLM 

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Model | Level: Counting

Keywords:

  • Model Parameter 모델 파라미터 
  • Activations 활성화 
  • KV Cache 캐쉬 

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Compression | Memory Count

Keywords: M=(Px4B/(32/Q))*1.2

  • Px4B
  • 32/Q
  • X1.2
~~~

(LLM 추론에 필요한 GPU Memory를 추정하는 기본적인 공식이다. 😕)

좀 더 세부항목을 확인해본다. 

~~~
M은 기가바이트 단위의 GPU Memory 이다. 

P(Model Parameter 개수) GPT-3는 1750억개(175Billion)
    4B: 매개변수당 사용되는 4Byte
    Q(Parameter당 Bit수):모델 가중치를 로드할떄 사용하는 데이터정밀도 
      □ 32Bit(FP32)
      □ 16Bit(FP16)
      □ BF16(BFloat16)
      □ 8Bit(INT8)
      □ 4Bit(INT4)

OverHead
    Keywords:
      □ Activations 활성화
      □ KV Cache 캐쉬
      □ TemporaryBuffers 임시버퍼
      □ SoftwareOverhead SW오버헤드
~~~


이제 이 수치와 지표들을 가지고 계산예시를 해보려고 한다. 특정개의 파라미터를 가진 모델을 비트 정밀도로 로드해서 추론한다고 가정하는 것이다.  

## 계산예시
### 계산과정
* 1.모델파라미터 수
* 2.모델파라미터 수
* 3.모델파라미터 수
* 4.모델파라미터 수
* 5.모델파라미터 수


### 실직적 의미 
* 1.
* 2.
* 3.
* 4.
* 5.


### Memory 최적화 기법
* 1.
* 2.
* 3.
* 4.
* 5.

### Can it Run LLM  확인방법
* 1.
* 2.
* 3.
* 4.
* 5.


출처&참고 

[HuggingFace](https://huggingface.co/spaces/Vokturz/can-it-run-llm)

VRAM [VRAM](https://health-coding.tistory.com/108)
TOPS [TOPS](https://blog.naver.com/qualcommkr/223461135901)
LLM [LLM](https://hunihub.link/genai/GPU-Memory-Calculation-and-Can-it-Run-LLM-Tool-Guide/)
