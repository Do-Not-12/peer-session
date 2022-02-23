Week 6 - Day 1

----

Today's PeerSession

----
# 1. 9강 Ensemble  - 렉사
- Ensemble(앙상블) : 여러 모델을 합쳐서 좋은 모델을 만들자!
    - 계산 코스트가 많이 든다.(Trade-off)
    - Model Averaging(Voting)
    - Cross Validation
        - K-fold => K개의 검증셋을 나눠서 반복
    - TTA(Test Time Augmentation)
        - 테스트 이미지를 Augmentation 후 모델 추론, 출력된 여러가지 결과를 앙상블
    - Grid Search vs. Random Search

# 2. 9강 further reading - 폴라
## 1. Optuna github
- 깃허브 주소 참고(하이퍼파라미터 튜닝할 때 참고)
- [github](https://github.com/optuna/optuna)
## 2. Hyperparameter
- 하이퍼 파라미터 튜닝 방식과 하는 이유 설명.
- searching하는 과정에서 코스트가 높아서 어떻게 해야할지에 대한 연구가 많다.
- [FLOYDHUB](https://blog.floydhub.com/guide-to-hyperparameters-search-for-deep-learning-models/)
## 3. AutoML 관련 포스팅
- [AutoML이란 무엇일까?](https://medium.com/daria-blog/automl-%EC%9D%B4%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C-1af227af2075)
- [Coding Gallery](https://cow-coding.github.io/posts/cousera3_2/)

# 3. 10강 Experiment Toolkits & Tips - 써리
- 텐서보드와 wandb에 대해서 얘기함.
- 텐서보드의 장점
    - 이미지의 샘플과 결과를 볼 수 있다.
    - 베이스라인 코드를 텐서보에서 볼 수 있다?

- wandb
    - 하이퍼 파라미터 중요도 지표를 측정해주는 기능이 있다.

- Python IDLE의 장단점
- Tips
    - 분석 코드보다는 설명글을 유심히보자.

# 4. 10강 further reading - 피터
- Wandb 사용해보기
- [devchopin](https://devchopin.com/blog/217/)