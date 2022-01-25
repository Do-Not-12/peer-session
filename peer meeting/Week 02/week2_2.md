# Week2 - Day2

## Today Peersession

#### 1. AutoGrad & Optimizer (발표자 : 폴라)
- 논문 : 논문이 제공하는 모델은 레이어들의 연속체이다.
- 레이어는 일종의 블록이다.
- torch.nn.Module을 이용해 구현
- 필요한 모듈들을 오버라이딩해서 사용한다.
- nn.Module : input, output은 선택적 정의 / forward, backward는 직접 정의, backward과정에서 AutoGrad를 통해 weight에 대한 미분 진행
- nn.Parameter : Tensor 객체의 상송 객체, 직접 지정할일은 잘 없다.
    - nn.Parameter의 역할은 torch.Tensor와 출력자체는 동일하다
    - 하지만 requires_grad=True로 자동 지정해주고 Parameters로 과정을 볼 수 있다는 차이가 있음.
    - 단순 객체 호출만해도 self.forward가 수행된다
- Backward : layer에 있는 Parameter의 미분 수행

#### reference(발표자 : 도리토스)
- Pytorch로 Linear Regression하기
    - nn.Module을 상속받아 LinearRegressionModel 생성
    - 상세과정 : wikidocs.net/60036
    - torch.optim.SGD를 사용
    
- Pytorch로 Logistic Regression하기 
    - 일정 값을 넘기냐에 따라 True or False 분류    
    - 상세과정 : wikidocs.net/57805
    - lr을 1로 설정한 이유(?)

#### 2. Data Set & Data Loader(발표자 : 렉사)
- Data set과 Data loader를 분리해야 가독성이 좋다
- underscore 의 의미는?
    - underscore의 위치와 갯수에 따라 private등 다양한 뜻을 가진다.(pep8 참고)
    - init, len, get_time 등
- CPU에서 Data loader를 만들고 전처리를 다하면 GPU로 옮겨준다
- batch size와 iteration의 개념 차이에 유의
- 흥미로운 데이터 : NotMNIST


#### reference(발표자 : 써리)
Fasion MNIST 
출처 : westshine-data-analysis.tistory.com/131
- 60,000개의 train과 10,000개의 test 데이터로 이뤄져있다
- 예제는 28x28의 흑백이미지로 구성된다. 라벨은 총 10개의 클래스로 이뤄져있다. 

- 난수로 이미지를 뽑는다
- Custom data set : 데이터 변환
- DataLoader : Dataset에서 변환한 데이터를 모델에 전달해줌

#### study 토의

스터디 투표

간프로젝트 2 3 3 3

코딩테스트 3 2 2 2

인터뷰지식 1 1 1 1

결론 : 인터뷰지식

- 날짜를 정하자(일주일에 1,2번) 
- 블로그에 배운걸 정리해서 각자 특이하게 느낀 부분을 정리해보자.
- 그외 : 코드리뷰,영어공부, 캐글대회, 논문구현 등등
- 강의 리뷰 시간을 더 줄이자(5-7분) 대신 그시간에 심화 포스팅을 하자.
- 남는 시간에 심화 포스팅 주제를 정해보자.
- 중간 중간 심화 포스팅 브리핑

- 부스트캠프 주차에 맞춰서 소소한 프로젝트를 하나 하자(기각 : 부캠 과제도 충분히 퀄리티가 좋음)
- 문제를 (5~6개)정도 정해서 각자 정답을 공부해온 다음 이야기 해보자.(기각 : 심화 포스팅에 집중하자)

- 심화 포스팅 주제
1. 폴라 : nn 모듈을 자세히 뜯어보자
2. 써리 : AB 테스트
3. 렉사 : dimension 차원에 대하여
4. 도리토스 : backpropagation