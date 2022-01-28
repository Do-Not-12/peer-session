# Week2 - Day4  

## Today Peersession

#### 1. Multi GPU(발표자 : 폴라)
- GPU에서 학습 분사를 하는 방법은 모델의 병렬화와 데이터의 병렬화가있다.
- 모델 병렬화 보다는 데이터 병렬화가 더 효율적

#### reference(발표자 : 도리토스)
- DataParallel보다는 Distributed Data Parallel 사용권장
- DP는 GIL로인해 DDP 보다 느리다
    - GIL : Global Interpreter Lock의 약자, 각 스레드를 병렬적으로 일하지 못하게함


#### 2. Hyperparameter Tuning(발표자 : 폴라)
- 모델의 성능을 좋게 만드는 방법은 3가지가 있다.
    - 모델 변경
    - data check
    - hyperparameter tuning
- 병렬처리를 위한 모듈 Ray가 있다. Scheduler를 설정하는 방식에 따라 parameter를 어떻게 만들지가 정해진다.

#### reference(발표자 : 도리토스)
- Ray를 사용하기 위해선 3개의 모듈 import가 필요
- Net(신경망) 클래스를 만들어야한다.
- config는 dict 형태이다.
- scheduler는 성능이이 좋아지지않게 하는 것들을 걸러준다
- get_best_trial로 가장 좋은 성능 모델 불러옴.
- Ray를 활용하면 쉽게 파라미터를 찾고 리턴할 수 있다.

#### 3. PyTorch Troubleshooting(발표자 : 써리)
- GPU util은 비슷한 기능을 하는 nvidia-smi 와 다르게 현재 스냅을 볼 수 있다.
- torch.cuda.empty_cache()를 사용하면 메모리 주소와 변수간에 관계를 끊어준다.
- 끊은 메모리는 중 필요없게 된 영역은 garbage collections로 해제 한다.
- max_memory_allocated는 메모리가 덜 필요한 모델의 경우 최대값을 정해 제한ㅎ 해준다.

#### reference(발표자 : 렉사)
- GPGPU(General Purpose GPU, GPU랑 같다고 볼 수 있다.)
    - 다차원 행렬 같은 병력적 연산처리가 가능
- CUDA
    - Nvidia의 GPU와 호환이 가장 잘 된다.
    - 연산에 CPU와 GPU를 같이 사용할 수 있게 해준다.

멘토링 
- 공부할 때 Tip
    - drawio 라는 프로그램을 활용해 필요한 이미지 생성가능 
        - 수식이 예쁘게 만들 수 있다.
    - overleaf.com
        - 여러 자료들을 오픈소스로 사용가능
        - 허들을 낮춰주는 역할
        - chaper, section 등 자동 분류
        - 텍스트를 템플릿화 해주고, 템플릿을 텍스트화 해줌.
        - {enumerate} 번호가 있는 목차
        - {itemize} 블랫이 있는 목차
        - 수식은 $$보다 \[ \] 권장

    - attention is all you need (Transformer 논문) 예시
        - blog 자료에 오타가 있는 것에 주의
    
    - kocw에서 대학 강의를 들을 수 있다.
    - 시각화 : https://jehyunlee.github.io/
