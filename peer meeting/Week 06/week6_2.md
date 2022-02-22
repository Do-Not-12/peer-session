Week 6 - Day 1

----

Today's PeerSession

----
# 1. 5강 Model 1 - 써리
## 1. pytorch
- 사용자 관점에서는 편함. 변형이나 커스터마이징 힘듬.

## 2. nn.Module
- 모든 nn.module은 child modules를 가진다.
- 모든 nn.Module은 forward함수를 가진다.

## 3. Parameters
- 각 모듈이 갖고 있는 파라미터들을 확인할 수 있다.
- 각 모델 파라미터들은 data, grad, requires_grad 변수 등을 가지고 있어 업데이트 편리

## 4. pythonic
- 파이썬스러운 코드를 통해 여러가지 응용 시도가능.



# 2. 6강 Model 2 - 피터
## Pre-trained Model
- CV의 발전으로 많은 일을 자동화 할 수 있다.
- 좋은 품질, 대용량 데이터로 미리 학습한 모델 -> 이 모델을 바탕으로 내 목적에 맞게 다듬어서 사용.

## torchvision
- 사용할 수 있는 pre-trained Model이 많다.

## Transfer Learning
- 전이학습은 높은 정확도를 비교적 짧은 시간 내에 달성할 수 있는 CV에서 자주 사용되는 방법론.

## CNN base 모델 구조(simple)
- Convolution base
    - 합성곱과 풀링층 여러겹
- Classifier
    - 주로 fully connected layer로 이루어져 있다. 모든 계층의 뉴런이 이전 층의 출력 노드와 하나도 빠짐없이 연결되어 있음.

## ResNet
- ResNet의 구조 중 `out_features` 중요.

----

- Case 1. 전체 모델을 새로 학습
- Case 2. 일부 Convolutional base를 freeze하고, 나머지 계층과 classifier를 새로 학습시키기
- Case 3. Convolutional base를 freeze, classifier만 새로 학습시키기

## Classifier
1. Fully-connected layers
2. Global average pooling
3. Linear support vector machines

# 3. 7강 Training & Inference 1 - 렉사
- Loss와 Optimizer는 따로따로 생각하기. metric은 평가를 어떻게 할 것인가에 대한 것.
- backward()를 할 때 모델의 파라미터의 grad 업데이트가 일어남.
- Focal Loss와 label Smoothing Loss 설명.
- LR scheduler - 동적으로 학습률 조정(여러가지 방법이 있다).
- 모델의 평가
    - Accuracy, F1-score, etc...
    - 학습에 직접적으로 사용되는 것은 아니지만 학습된 모델을 객관적으로 평가할 수 있는 지표가 필요하다.
    - class balance도 중요함!

# 4. 8강 Training & Inference 2 - 폴라
- model.train()
    - 훈련용으로 바꾼다. ex) `Dropout`, `BatchNorm` 활성화.

- optimizer.zero_grad()
    - 이전의 optimizer 계산 값 초기화.

- optimizer.step()
    - 업데이트 해주는 과정.

- model.eval()
    - self.train(False), gradient 관련 파라미터를 동작하지 않게 해줌.

- with torch.no_grad():
    - 모든 텐서의 gradient가 False가 된다. 업데이트가 되지 않도록.

- PyTorch Lightning
    - Keras의 코드처럼 간단하게 구현 가능.
    - 그래도 공부는 PyTorch로 하기