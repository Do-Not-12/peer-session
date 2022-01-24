# Week2 - Day1

## Today Peersession

#### 1. Introduction to PyTorch
- PyTorch : 연구에서 사용, 상승세, 그래프 나중에 정의
0 TensorFlow는 현업사용, 하락세, 그래프 정의 먼저
- __가장 큰 차이 !__ : PyTorch는 GPU를 tensor에 올려준다.

#### reference
- 딥러닝 프레임워크 성능 비교 : https://en.wikipedia.org/wiki/Comparison_of_deep-learning_software
- PyTorch로 시작하는 딥러닝에 입문하는것을 목표 : https://wikidocs.net/book/2788
- PyTorch를 Tutorial 예제 구현 가능 사이트 : https://pytorch.org/tutorials/

#### 2. PyTorch Basics
- view와 reshape은 contiguity 보장의 차이가 있다.(view 사용을 권장)
- __행렬곱셈 연산은 dot이 아닌 mm__ 사용
- AutoGrad : PyTorch 핵심인 __자동 미분__

#### reference
- pytorch 한국 사용자 모임이 있음ㄴ
- Autograd 튜토리얼 : https://pytorch.org/tutorials/beginner/blitz/autograd_tutorial.html
- Tensor와  Autograd 튜토리얼 : https://pytorch.org/tutorials/beginner/examples_autograd/two_layer_net_autograd.html
- lr을 지정해줘서 반복문으로 가중치를 빼주던 과정을 loss.backward()로 줄일 수 있다.

#### 3. PyTorch 프로젝트 구조 이해하기
- train.py에서 ConfigParser에 의해 팩토리패턴으로 불러온 arg로 객체 생성 $\rightarrow$ config
- parser_config.py 에서 read_json은 Data를 dict 형태로 변환
- main에서 logging을 train으로 설정
- main에서 data_loader : init_obj을 사용해 object에서 config파일 불러옴, module_data로 mnlist dataloader 모듈 불러옴
- Train은 base_trainer에서 train 한다.
- save_checkpoint에서 epoch 마다 저장

#### reference
- template의 큰 틀에서 train, test, data_loader등은 모두 존재
- parser_config에서 from_args가 중요하다
- trainer : 가장 핵심 되는 파일

__Pytorch Lightning__
1. Tensorflow의 keras같은 존재
2. 모델을 상속하는 과정을 간소화해준다.
3. LightningModule을 상속(training_step, configure_optimizers 반드시 구현)
4. forward : 모델 추론 결과 제공
5. training_step : 학습 루프의 body, batch 활용해 loss 계산
6. configure_optimizers : 모델의 최적 파라미터를 찾을 때 사용할 optimizer, scheduler 구현

- 보일러플레이트 : 머신러닝을 하나의 실험과정으로 봤을 때 환경에 따른(batch_size등) 결과의 변화를 시각적으로 보여줌(마이크로소프트 제공)