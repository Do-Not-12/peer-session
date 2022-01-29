# Week2 - Day5

## Today Peersession

- study 
- 심화 포스팅 : 수업을 다 듣고 과제를 다한 금요일에 각자 정한 심화 주제로 포스팅을 하고 발표를 하는 시간

- 심화 포스팅 주제
    1. 폴라 : [torch.nn.Module 뜯어보기](https://cow-coding.github.io/posts/module/)
    2. 써리 : [p-value](https://westshine-data-analysis.tistory.com/133)
    3. 렉사 : PCA
    4. 도리토스 : [Backpropagation](https://blog.naver.com/axe_knife/222633639093)
    5. 피터 : Overview of PyTorch Autograd Engine
    

## torch.nn.Module 뜯어보기
- init : 거의 attribute로 구성
- forward : forward를 선언하지 않으면 _forward_unimplemented 함수가 error를 일으킨다
- apply : 생각보다 간단한 식이다. function을 재귀식으로 넣어준다.
- dump_pathes,_version : module 변화 상태를 기록
- eval,train : 모델의 훈련 상태 설정
- extra_repr : 비어있는 문자열을 return 해준다. repr 함수에서 extra_repr에 내용을 채워준다.
- register_forward(_pre)hook : forward_hooks에 hook을 저장, pre_hook은 input을 수정 가능해진다.
- register_full_backward_hook :  is full backward를 true로 설정, back_ward_hooks에 hook을 등록, grad_input을 대신할 new_input 반환input과 ouput을 수정하면 error 발생
- call : 객체가 호출 될 때 수행되는 magic method 함수. 단순 객체가 call되도 forward가 실행. 

## Backpropagation
- 딥러닝은 위 X 값을 입력층으로 받아서 은닉층과 출력층을 거쳐 출력된 값(A(3))이 원하는 값과 가까워 질 때(E가 작을 때) 까지 학습을 한다.
- 각각의 층은 교차되는 가중치 값으로 연결되어 있는데 이 가중치(weight, W)를 조금씩 수정해 가면서 최종 출력값에 영향을 주어 오차를 줄여나간다. 
- 이 때 이 가중치를 수정할 때 역전파(backpropagation) 방법을 사용한다.
- 맨 마지막 층의 값으로부터 출발하여 차례차례 역으로 원하는 곳 까지의 결과를 얻어내는 과정이기 때문에 이를 '역전파(backpropagation)'이라고 부른다

## Overview of PyTorch Autograd Engine
- 역전파는 수학적으로 야코비안 행렬로 표현할 수 있다.
- PyTorch의 Autograd역시 원리는 야코비안 행렬이지만 실제로는 연산 그래프를 활용한다.
- forward에서 편미분들을 그래프에 저장하고 backward 입력시 한번에 곱해진다.
- 이 과정에서 Pytoh c api를 통해 C++언어를 이용해 계산한다.

## p-value
- p-value에 대해 명확히 알고 해석할때 무엇이 중요하고 요즘에도 유효한지
- 귀무가설 : 통계에서의 가정에서 디폴트로 맞다는 전제로 진행, 내 데이터의 통계량이 귀무가설을 지지할 확률을 p-value라고 정의할 수 있다.
- p-value는 어떤사건이 우연히 발생할 확률이라고 할 수 있다.(통계적으로 0.05보다 크면 인과관계가 없다고 해석)
- p-value는 통계량을 0~1사이로 나타낸다.
- 정리 : p-value가 작으면 귀무가설에서 주장하는 바와 관측데이터의 차이가 커 귀무가설이 유의미하지 않고 크면 유의미 하다고 본다.
- 해석시 주의점 : 하지만 미국통계학회에서는 p-value에 대한 이러한 정의가 꼭 올바르다는 것은 아니라고 한다. 즉 p 값은 어떤 가설이 참이라거나 실험결과가 중요한지와 같은 여부를 결정할 수 없다고한다. 
- ASA의 해석 : 귀무가설의 확률 분포에서 이러한 실험 데이터가 나올 확률이 얼마나 낮은지로 해석
- 믿을만한 지표인가? : 통계적 유의성확보를 위한 도구, 올바른 적용과 해석을 위해 유의수준과 실험 규모등의 다른 요소들을 적절히 고려한 실험 설계가 필요. 

## PCA(Principal Component Analysis)
- eigen value(스칼라), eigen vector
- diagonalization : 임의의 matrix A, P^(-1)AP 가 대각행렬이면 P가 A를 diagonalize한다고 한다.
- 공분산이란? covariance matrix는?
- PCA analysis 란? 큰 그룹을 나누는 방법 중 하나(축의 감소)