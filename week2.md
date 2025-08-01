#### 퀘스트 작성자: J152신채은, J300황지현, J301황찬우, S015박현수
## 기존 미션 토론 (개선 점 찾기)
#### 기존 퀘스트 1: 미션 수행할 때 AI를 테스트 작성에 활용해보기
    - 릴레이 프로젝트에서는 코드에서 멀어지는 걸 지향 할 필요 있음
    - 테스트 데이터와 검증 내용 추천 받기로 변경 (직접적으로 코드를 작성 받는게 아닌 형태로)
#### 기존 퀘스트 2: AI에게 답변이 아니라 질문을 던지도록 활용해보기
    - 하루 미션 완료 후, 관련 키워드를 기반으로 객관식 CS 개념 문제 풀이로 확장
    - 기존 처럼 면접 질문처럼 활용해도 좋지만, 시간 효율 고민
#### 기존 퀘스트 3: 피어피드백 대화를 AI로 요약, 정리하도록 활용해보기
    - 클로바/다글로 등 활용
    - 피어피드백 내용을 기반으로, 관련 내용 검증, 추가 지식 정리 등으로 활용 가능
    - 다음날 피어피드백의 흐름, 체크포인트 등 추천사항 피드백 받아보기
#### 기존 퀘스트 4: AI를 활용해 슬랙에 내 상황을 4컷만화로 공유해보기
    - 극 I 성향을 위해 슬랙에 공유가 힘들다면, 피드백 타임 때 조원끼리 공유하기

## 관련 정보 조사
#### 기존 퀘스트 1: 미션 수행할 때 AI를 테스트 작성에 활용해보기
- 유닛 테스트는 다양한 조건과 시나리오에서 수행되어야 함
그렇지 않으면…
`https://www.instagram.com/reel/DMg_MeBo4SY/?igsh=OXRhN20ycjFxaDB6 
`
- 다양한 테스트 조건과 시나리오를 AI를 통해 뽑아내고, 미처 생각지 못한 조건을 발견 할 수 있음
`https://testomat.io/blog/ai-unit-testing-a-detailed-guide/#2-test-case-generation `

#### 기존 퀘스트 2: AI에게 답변이 아니라 질문을 던지도록 활용해보기
- 한주간 학습 한 CS 지식을 객관식 문제로 풀어볼 수 있음
- 객관식 문제 제작 시 문제와 답을 분리하는 프롬포트 필요
- 채점 기능까지 有
- 향후 오답 중심 해설 / 주제별 복습 가이드 등 확장 가능, 학습 저장소에 넣어두면 복습에 유용함
- gpt 외 문제 생성에 특화된 ai 추천
    ```
    https://quiz.zep.us/
    https://opexams.com/ko/ai-quiz-generator/
    ````
#### 기존 퀘스트 3: 피어피드백 대화를 AI로 요약, 정리하도록 활용해보기
- 피어피드백을 요약만 하는 기존 퀘스트에서 피드백을 해주기까지
- 내용 검증: 요약된 피드백이 정확한지, 실제 학습 내용과 부합하는지 확인 -> LLM이 자동으로 "사실 검증(Fact-check)" 시도 가능
- 한계: AI 자체가 절대적 진위 판별보다는 자료 참조 기반 확인(공식 문서 링크 제공) 형태가 더 안정적
- 활용 플랫폼: 클로바, 노션AI, ChatGPT, 다글로 등
- 하나의 플랫폼에서 모든 처리가 힘들다면, 여러 플랫폼 AI 활용 가능 (예: 다글로로 요약 후 Gemini로 검증)
#### 기존 퀘스트 4: AI를 활용해 슬랙에 내 상황을 4컷만화로 공유해보기
- gpt에게 역으로 프롬프트 전문가 역할 부여해 추천을 받는다거나 컷별로 시선처리 및 문구를 구체화해주기 
`(https://brunch.co.kr/@1212ac31a500435/283)`
- 네컷만화 한글 깨짐 문제: 글자는 빼달라고 하거나 분리해서 편집할 수 있게 해달라고 요구
`(https://kr.linkedin.com/posts/duckjungkim_%EC%9A%94%EC%A6%98-%EC%9C%A0%ED%96%89%ED%95%98%EB%8A%94-chatgpt-4o%EB%A5%BC-%EA%B0%80%EC%A7%80%EA%B3%A0-4%EC%BB%B7-%EB%A7%8C%ED%99%94%EB%A5%BC-%EA%B7%B8%EB%A6%AC%EB%A9%B4-%ED%95%9C%EA%B8%80%EC%9D%B4-%EA%B9%A8%EC%A0%B8%EC%84%9C-activity-7312652015371726848-7HG4)`
- 상황 설명을 통해 ai가 자동으로 네컷 만화 생성
`(https://chatgpt.com/g/g-ppek1qROk-4keosmanhwa-saengseonggi)`
- 직접 제작해보기:
// 사진 삽입


## 퀘스트 목록
#### 퀘스트 1: 복잡한 메소드 대상 AI 기반 유닛 테스트 시나리오 도출
- 배경:
    - 제어 흐름이 복잡하거나 예외 상황이 많은 메소드의 경우, 개발자가 모든 가능한 조건과 시나리오를 수동으로 예상하여 테스트 케이스를 작성하기란 매우 어려움.
    - 이는 테스트 커버리지의 부족으로 이어져 숨겨진 버그가 발생할 위험을 높임.
    - 최근 AI 기술은 이러한 복잡성을 해결하고, 사람이 미처 생각지 못한 다양한 테스트 조건과 시나리오를 생성할 수 있음.
- 목적:
    - AI를 활용하여 동작을 예상하기 어려운 복잡한 메소드에 대한 다양하고 포괄적인 유닛 테스트 시나리오와 조건을 도출하기.
    - 이를 통해 개발자가 놓칠 수 있는 예외 케이스나 엣지 케이스를 발견하고, 테스트 커버리지를 극대화하여 코드의 신뢰성을 향상시키는 것을 목적으로 함.
- 달성 기준:
    1. 메소드의 비즈니스 로직 및 제어 흐름을 분석하고
    2. 사람이 수동으로 작성하기 어려운 1가지 이상의 테스트 시나리오와
    3. 각 시나리오에 필요한 구체적인 입력 조건(input) 및 예상 결과(expected output)를 제시하기.
#### 퀘스트 2: AI에게 cs지식에 대한 질문을 요청하고, 생성된 질문을 풀어보며 cs지식 리마인드하기
- 배경 : 
    - 우리는 AI를 나의 질문에 대한 답을 하는 용도로 사용하는 경우가 많음. 
    - AI를 다양하게 사용하기 위해 반대로 내가 원하는 질문을 AI로부터 제공받고 이 질문을 통해 학습에 도움을 받는 방향으로도 AI를 사용해보는 경험을 하고자함.
- 목적 : 
    - 미션을 수행하면서 얻은 CS 지식들은 시간이 지나면 기억이 흐려질 수 있음. 
    - AI로부터 CS지식에 대한 간단한 객관식 질문을 받고 이를 풀어봄으로써 학습내용을 리마인드 하기.
    - 나아가 내가 잘 모르고 있었던 부분까지 확인하여 메타인지적 사고를 할 수 있도록 함.
- 달성기준:
    1. AI에게 CS지식과 관련한 질문을 생성해달라고 요청
        - 꼭 gpt가 아니어도 되고 객관식이 아니어도 됨, 다만 간단하게 문제를 풀어보고 학습내용을 리마인드하는것이 목적이므로 복잡한 답을 요구하는 문제 형식은 지양하는 것이 좋음
    2. 학습 내용을 리마인드 하는 것이 주 목적이므로 조금 시간이 지난 cs 지식에 대한 질문을 요청하면 더 좋음
        - 위의 요청시 답은 따로 요청할 때에 생성해달라고 요청
    3. 생성된 문제를 풀어보고 답을 전달하여 채점 요청
    4. 오답이 있다면 해설을 요청하고 오답노트를 만들어 해당 지식을 사용한 미션의 gist에 업데이트하기
#### 퀘스트 3: 피어피드백 AI정리 및 AI피드백
- 배경: 
    - 피어피드백에서 좋은 의견과 내용들이 많이 나옴.
    - 이를 요약 정리하면 향후 학습에 도움이 됨.
- 목적: 
    - 좋은 내용을 AI를 활용하여 요약 정리해보기.
    - 이를 기반으로 다음 피어피드백에 기여할 수 있는 피드백 받아보기.
- 달성기준: 
    1. AI를 활용하여 피어피드백 내용을 요약. 
    2. 요약된 내용을 토대로 추가 학습내용, 향후 피어피드백 체크포인트 등 AI의 추천 피드백을 받아보기.
    3. 관련 프롬프트를 저장하고 릴레이프로젝트 팀원과 공유하기.
#### 퀘스트 4: AI를 활용한 네컷 만화 생성 및 공유
- 배경:
    - 고난도 미션 수행 중에 일상에서 잠깐의 쉼을 얻고 기분 전환용 미션이 필요하다는 생각
    - 비대면이다보니 동료들과 일상 공유가 쉽지 않은 점, 공유 방식이 쉬우면서도 재밌으면 좋겠다는 점에서 탄생.
- 목적: 
    - 네컷만화를 통한 일상 공유로 동료들간의 친밀감, 유대감 형성 및 기분 환기 목적.
- 달성 기준: 
    - 노션에 ai로 생성한 네컷 만화를 인증하거나 
    - 다음주 릴레이 프로젝트 인증 시간에 팀 동료들과 공유 및 week2.md파일 기록.

---

## 2주차 수행내역 

---

## J244 정연진 Week2 릴레이 프로젝트

## 퀘스트 2: AI에게 cs지식에 대한 질문을 요청하고, 생성된 질문을 풀어보며 cs지식 리마인드하기

## 선정배경

- 시간이 지나면 배운 내용을 자연스럽게 잊어버리기 쉽다. 그러기 위해선 복습이 필수적인데 항상 비슷한 것만 반복하기가 쉽다.

- 하지만 AI에게 문제를 내달라고 요청하면 자연스럽게 문제의 분야가 섞일 수 있어 실질적인 도움이 될 것이라 판단했다.

## 달성기준

- AI에게 객관식, 서술형을 섞어 10문제를 제출해 달라고하고 문제를 푼다.
- 틀린문제는 해설과 함께 오답노트를 작성해 달라고 한다.
- 오답노트를 엮어서 릴레이 프로젝트에 업로드한다. 

## 2025-07-31 질문 생성 + 문제풀이

### Gemini 사용

우선 Gemini에게 다음과 같이 물어봤다.

```
그 동안 내가 프로그래밍에 관한 질문을 많이 했으니 그걸 토대로 객관식, 서술형 10문제를 선정해서 나에게 내줘.
해설이나 힌트없이 문제만 내주고 내가 답을 제시하면 그걸 토대로 해설과 오답노트를 생성해줘. 이제 문제를 내줘.
```
단순히 문제를 나열해 줄줄 았는데 신기하게도 우측에 퀴즈를 생성해서 바로 풀 수 있도록 제시해줬다. 

https://gemini.google.com/share/67a6c3869c29


<img width="708" height="559" alt="image" src="https://github.com/user-attachments/assets/a57f92e5-55b8-43ef-92d4-6d2000e0277b" />

<img width="725" height="551" alt="image" src="https://github.com/user-attachments/assets/98656c39-aae2-4ed7-89c9-cb77bb37a804" />

<img width="710" height="560" alt="image" src="https://github.com/user-attachments/assets/19b5225e-9642-4ee5-86c4-89f67f596a14" />

<img width="708" height="550" alt="image" src="https://github.com/user-attachments/assets/e43f5d37-72dc-41ae-b20b-ff6fd6d9001c" />

<img width="715" height="579" alt="image" src="https://github.com/user-attachments/assets/2b375fb2-8f75-4c88-a7c5-2411698de606" />

<img width="718" height="552" alt="image" src="https://github.com/user-attachments/assets/0c2e7a0a-bf4a-4342-a080-448aaab35383" />

<img width="696" height="591" alt="image" src="https://github.com/user-attachments/assets/928833a5-d084-4e15-b11f-a068db985397" />

<img width="707" height="544" alt="image" src="https://github.com/user-attachments/assets/43407cb8-a910-4f04-8c74-bbe56609e592" />

<img width="689" height="448" alt="image" src="https://github.com/user-attachments/assets/8d9f31da-cf13-4016-9486-308570ddbb37" />

<img width="706" height="544" alt="image" src="https://github.com/user-attachments/assets/5393e802-3404-4f88-91c8-5c461489daca" />


### 정답

<img width="713" height="607" alt="image" src="https://github.com/user-attachments/assets/9bce01dc-6fc4-46c6-b958-6aa700dcdece" />

<img width="711" height="644" alt="image" src="https://github.com/user-attachments/assets/640480c6-102d-4810-8466-033246f7ccfe" />

<img width="688" height="648" alt="image" src="https://github.com/user-attachments/assets/2e22672a-bd22-4088-9383-9120828c0bbe" />

<img width="713" height="645" alt="image" src="https://github.com/user-attachments/assets/99e58c9c-2533-46c7-83f3-959ad2d3e241" />

<img width="702" height="662" alt="image" src="https://github.com/user-attachments/assets/927a599f-9b54-4be8-8ce4-ceb864eda35e" />

<img width="712" height="623" alt="image" src="https://github.com/user-attachments/assets/ea199c76-0145-4212-9e00-68c83af5c9f5" />

<img width="713" height="673" alt="image" src="https://github.com/user-attachments/assets/06f224c4-255f-4f5a-9913-90be9fa4e318" />

<img width="707" height="726" alt="image" src="https://github.com/user-attachments/assets/f480b372-83b4-4e9c-8969-dbd6356338a7" />

<img width="692" height="630" alt="image" src="https://github.com/user-attachments/assets/c2b5c329-6d87-49b7-9716-40e6bc3ce8c0" />

<img width="702" height="634" alt="image" src="https://github.com/user-attachments/assets/a4d1c68a-8982-4796-aa11-ec5b86f2a349" />

이와 같이 문제를 맞추면 밑에 해설을 달아주고, 틀린 경우 틀린 이유와 정답을 알려준다. 
난이도는 적당한 퀴즈정도였지만 아마 어렵게 내달라고 한다면 더 어려운 문제도 내줄것 같아 다시 물어봤다. 

### 재질문
```
문제는 잘 풀어봤어. 지금 보다 한 단계 어려운 문제를 내줄 수 있어?
```
https://g.co/gemini/share/b8b031eacb03

이런 식으로 난이도는 조절 가능한 듯 하다. 생각보다 문제가 괜찮아서 유용하게 학습에 쓰일 수 있다고 본다. 

<img width="710" height="915" alt="image" src="https://github.com/user-attachments/assets/ae3c6130-7885-411b-8a34-97058e81072e" />

### 공유

마지막으로 슬랙 random 채널에 공유하였다. 

<img width="1970" height="688" alt="image" src="https://github.com/user-attachments/assets/f7b7b9de-8ea9-4864-82fc-01ea995e3d28" />

---


## K032 홍지민 Week2 릴레이 프로젝트

## 퀘스트 3: 피어피드백 AI정리 및 AI피드백

### 선택 배경
동료들의 피어피드백에서 좋은 피드백과 조언들을 많이 얻을 수 있었습니다. 하지만 내용이 너무 어려워 정리하기 어려운 경우도 있었고, 놓치는 경우도 있었습니다.
그래서 피어피드백을 요약하고, 그 내용을 바탕으로 AI의 추천 피드백을 받으면 유익할 것 같아 이 미션을 맡기로 했습니다.

### 수행 계획
1. 녹음/녹화 도구 활용
  - 클로바노트를 활용해 피어 피드백 대화 내용 기록
2. AI 요약 자동화
  - 클로바노트, GPT 활용해 대화내용 요약
3. 사실 검증 시도
  - 요약된 피드백이 학습 내용과 일치하는지 확인
  - 공식 문서, 튜토리얼 등으로 검증
4. 최종 피드백 공유
  - 동료들에게 공유, 다음 학습에 반영 가능하도록 구성

### 수행 과정
동료들에게 허락울 구한 후, 피어피드백 대화 내용을 클로바노트로 녹음하고 요약했습니다. <br/>
![KakaoTalk_Photo_2025-07-31-22-15-02 001-side-crop](https://github.com/user-attachments/assets/0aedee24-9cd6-4dd2-97ad-1f4ba74bbb19)

이후, 요약된 내용을 바탕으로 GPT를 통해 피드백을 정리했습니다. <br/>
<img width="1308" height="783" alt="스크린샷 2025-07-31 오후 10 33 13" src="https://github.com/user-attachments/assets/154308bb-5373-4a10-9a52-b0ed8f85f932" />
<img width="1305" height="785" alt="스크린샷 2025-07-31 오후 10 33 31" src="https://github.com/user-attachments/assets/cbd84ee0-909d-4849-a556-ff02a47c36f3" />


### 소감
GPT가 생각보다 흐름을 잘 정리해주어서, 앞으로 피어피드백을 할 때 유용하게 활용할 수 있을 것 같습니다. 단 음성 인식의 한계로 인해 잘못 인식된 단어들도 있었어서, 너무 맹신해서는 안될 것 같다는 생각도 들었습니다.