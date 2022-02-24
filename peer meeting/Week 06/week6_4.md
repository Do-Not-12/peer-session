Week 6 - Day 1

----

Today's PeerSession

----
# 모델 진행사항에 대한 얘기.
- 폴라 : wandb 연결, 파라미터 조정, 모델 구체화 중. 리더보드 순위 상승 기여.
- 렉사 : baseline code 참고하여 모델링 중
- 피터 : 이미지 augmentation 진행 중. 리더보드 순위 상승 기여.
- 써리 : baseline code 참고하여 모델링 중
- 도리토스 : 폴라 코드 참고하여 baseline 코드 구성 중

# 오피스 아워
- baseline code에 대한 설명, PyCharm 꿀팁.

# 멘토링

## 사전 질문

1. 한 가지 모델로 한꺼번에 학습하지 않고, `마스크 착용 여부 모델`, `연령을 판단하는 모델`, `성별을 판단하는 모델` 처럼 여러 모델로 나눠서 하는 것이 의미가 있을까요?

2. 제공받은 데이터셋 모두가 정면을 바라보고 있는 사진으로 데이터의 질이 상당히 좋은 편인데, 이런 상황에서도 이미지 전처리를 하는 게 의미가 있을까요?

3. 리더보드에 제출된 모델의 성능들을 보면  F1 Score와 Accuracy의 차이가 많이 나는 팀도 있고, 얼마 차이가 나지 않는 팀도 있는데 이런 현상을 수학적으로 어떻게 해석을 할 수 있을까요?
----
- 질문 1번 : 나눠서 실험을 해봐야 안다.(아마 비슷할 것)

- 질문 2번 : 밸런스 비중을 맞춰주기 위해 augmentation을 해줘야 한다.
    - augmentation할만한 것 : [Image Data Augmentation Overview](https://hoya012.github.io/blog/Image-Data-Augmentation-Overview/) => RandAugment, UniformAugment
- 질문 3번 : 평가지표에 대해 강의자료 첨부.
    - F1 Score는 imbalance를 잘 잡아낸다.


## 작년 score
- 0.7858이 작년 1등.
- 0.7849가 4등
- 0.78 정도 나오면 상위권이다.

## 추가 질문
- Augmentatino한 데이터를 어떻게 추가할 것인가?
- 과제 프로젝트별로 팀에 따라 wandb와 tensorboard 중에 쓴다.

## 선형대수학 remind
- Matrix decomposition
    - *Matrix Factorization*

- 미적분
    - 멘토님은 고3 때부터 마음 잡고 공부를 시작해서 서울대 박사과정까지 왔다.