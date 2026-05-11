---
layout: post
title: Google/Open API
description: >
  Google/Open API 연동시에 참고할 사항들이다. 
image: /assets/img/caleb-george.jpg
hide_image: true
tags: [Build]
redirect_from: /2017/11/17/whats-new-in-v7/
---

API연동하기 위해서는 KEY를 발급받고 연동작업을 진행해야한다. 대부분 가입후에 로그인하고 발급받은 후에 후속작업을 진행하지만 몇 가지 참고사항이 있다. 우선 Credit Card도 등록하지만 결제한도 limit를 설정해야한다. 그리고 Billing 이나 Dashboard에서 설정사항값으로 잘 동작하고 있는지 반드시 확인이 필요하다. 


## ChatGPT OpenAPI
[OpenAPI](https://platform.openai.com/home)여기서 확인이 가능하다. 로그인해야 한다. 로그인 후에 우측 상단의 Dashboard나 좌측의 Usage에서 추가적인 확인이 가능하다. 

![Hydejack's background image]({{ site.baseurl }}/assets/img/open.jpg){:.lead}

추가적으로 질의/응답의 Token 량을 가지고 후속비용예측이 가능하다. 관련 결과를 가지고 질의하면 예상비용도 친절하게 알려준다.(자본주의의힘?)
https://platform.openai.com/tokenizer[Token확인](https://platform.openai.com/tokenizer)



## Google API 
이 Post를 작성한 궁극적인 원인이다. 동일하게 로그인후에 관련 메뉴를 확인하면 된다. https://aistudio.google.com/app/api-keys <a href="https://aistudio.google.com/"></a> 하지만 친절하지 않고 복잡하다.


비용결재도 Tier-Group&후불에 대해서 미리 인지하고 처리를 해야하고 *"무엇인가? 사전이해가 많이 필요하다"* 물론 개인적인 시각의 차이일수 있다. 하지만 User친화적인 감각은 아닌 듯 하다. 

![Hydejack's background image]({{ site.baseurl }}/assets/img/studio.jpg){:.lead}


## API연동  
이후에 각 API를 연동하고 `.gitignore`처리하고 추가로 FrontEnd영역에서(simpleHTML 이나 React/NodeJS등등) API연동관련 작업한 기록들은 2Platform의 차별점들과 함께 별도의 기록으로 Post하려고 한다. 







