# Week1-Day4

## Today Peersession

### 강의리뷰 및 레퍼런스 정리

##### 1. 딥러닝 학습방법 이해하기

- softmax : 어떤 특정 클래스 K에 속할 확률
- 신경망은 선형모델 + 활성함수를 해야 비선형 형태로 변형
- 역전파 계산시 연쇄법칙(Chain Rule)을 적용해서 gradient vector를 활용한 경사하강법을 적용

##### 2. 확률론 맛보기

- 회귀/분류에 따라 어떤 것을 최소화할 지를 결정하는 것이 좋음
- 몬테카를로를 사용하면 대수의 법칙 원리에 따라서 근사할 수 있음
  - [대수의 법칙-위키](https://ko.wikipedia.org/wiki/큰_수의_법칙)

##### 3. 통계학 맛보기

- [MLE 추가자료](https://blog.naver.com/nilsine11202/221906921675)
- MLE 예시 정규분포 자료는 강노가 좀 이상하기 때문에 직접 해보는게 좋을듯
  - [추가자료](https://angeloyeo.github.io/2020/07/17/MLE.html#mle의-좀-더-복잡한-예시-모평균-모분산-추정)

##### 4. 베이즈 통계학 맛보기

- 베이즈 정리는 예시랑 같이 보는 게 이해하기에 제일 좋음
- precision, recall, specificity
  - [추가자료1](https://eunsukimme.github.io/ml/2019/10/21/Accuracy-Recall-Precision-F1-score/)
  - [추가자료2](https://ko.wikipedia.org/wiki/정밀도와_재현율)

##### 5. CNN 첫걸음

- Convolution에서는 kernel을 움직이며 적용하므로 커널크기만큼 활용 (파라미터 크기 감소)
- [Convolution Visualizer](https://ezyang.github.io/convolution-visualizer/)
- Convolution 역전파는 Convolution 연산과 동일한 방식

##### 6. RNN 첫걸음

- sequence data는 i.i.d를 잘 위배하므로 주의해야함
- sequence data는 가변적인 길이의 데이터를 다룰 수 있는 모델이 필요함
- RNN은 MLP와 유사함
  - 과거의 정보를 사용하기위해 이전의 잠재변수를 입력으로 재활용
  - RNN 역전파 원리는 BPTT

### 레퍼런스

- MLE

  - 평균, 분산 연산 규칙

  - 데이터를 손으로 계산하는 데에 한계가 발생하므로 계산을 적게해서 분포를 찾는 방법

  - 극점을 가장 적합하다고 판단

  - log liklihood 의 미분값의 0을 만족하는 theta를 분포에 넣어보며 적절히 찾는다.

- 몬테카를로 

  - 실제로 계산하기 힘든 내용을 계산하고자 나타난 방법

### 멘토링 시간

매주 목요일 6-7시

### 질문

- [ ] BPTT
- [ ] LLN (Law of Large Number)
- [ ] precision, recall, specificity
- [x] MLE에서 왜 parameter의 극점을 왜 가장 적합하다고 판단하는가?
  - 확률은 기본적으로 다 양수 그 중 단순히 극값을 찾고 싶어서 0인 부분을 확인
  - theta에 대해 가장 많이 겹치는 부분을 찾기위해
  - MLE의 목적은 prior라고 정한 것과 데이터의 격차를 가장 적합하게 찾아주는 파라미터가 뭔지를 찾는 것
  - 오늘 질문에서 theta에 대한 극값을 찾는 이유는, 극값이 단순하게 최대값 후보이기 때문이에요. 만약에 극값이 유일하다면 최대값임을 보장할 수 있어요. (확률은 적분하면 1이고, 0과 1사이의 값만 가진다는 점을 생각하면 조금 자연스러울 거에요.) 하지만 극값이 여러개 나온다면 값을 대입해서 계산해봐야합니다:)

## Frequentist VS Bayesian

- Bayesian은 prior을 가정하고 event 발생을 통해 prior을 업데이트하며 맞춰나가겠다가 목적

  - 모든 경우에 잘 work하는 것은 아님 따라서 제약이 필요한 경우들이 있음

  

  

  

