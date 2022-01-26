# Week2 - Day3  

## Today Peersession

#### 1. 모델 불러오기 (발표자 : 도리토스)
- 모델 구조를 출력 할 때 torchsummary를 활용하면 가독성이 좋게 나온 것이 인상 깊다.
- checkpoint 는 model을 학습하면서 저장

#### reference(발표자 : 써리)
- cv model
    - image model
    - Fine Tuning만 하면 되게 만들어 놓은 모델
- segmentation model
    - segmentation은 각 영역이 어떤 의미를 가지는지 분리하는 방법

#### 2. Monitoring tools for PyTorch (발표자 : 렉사)
- wandb 사이트는 무료로 쓸수 있는 사이트
- Tensorboard의 좋은 기능
    - 넣은 데이터셋의 변형을 코드를 수정하지않고 보여준다.
    - 시각적으로 보여주는 기능이 좋다.


#### reference(발표자 : 폴라)
- PyTorch Lightning Logging
    - PyTorch를 케라스 처럼 단순화 시켜 쓸 수 있다.
    - Lightning에도 학습기록 모듈이 있다 (공식 문서에는 Tensorboard를 사용권장)
    - lightning을 상속하면 self.log를 이용해 log를 기록할 수 있다(훈련 진행률을 보여줘서 편리함)

- 질문
1. model.W.data.fill_ 왜 쓰는가?
2. forward, pre_forward 차이?
3. hook, apply를 많이 사용하는지?
4. 현직 연구,기업에서는 어떤 tool을 쓸까?