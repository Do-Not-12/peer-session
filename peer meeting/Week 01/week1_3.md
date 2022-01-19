# Week1-Day3

## Today Peersession

### 강의 리뷰 및 질문정리

#### 1. Numpy

- tensor 개념은 바로 와닿지 않기때문에 그림 참고하는 것이 좋음
- `numpy.empty()`로 생성하는 경우 임의의 주소를 할당하여 `ndarray`를 생성
- broadcasting도 그림과 함께 이해하는 것이 좋음
- `np.where(condition, True_val, False_val)`을 사용하면 조건에 True면 `True_val`로 False면 `False_val` 

#### 2. Matrix

- 행렬의 성분곱은 `x*y`, 행렬곱은 `x@y`
- `np.inner`는 i번째 행벡터와 j번째 열벡터 사이의 내적을 구함 -> 행개수, 열개수가 동일해야 함
- 의사/유사 역행렬(psuedo-inverse) = 무어-펜로즈 역행렬
  - 축소된 SVD를 참고하면 좋음 [이론부터 구현까지 링크](https://westshine-data-analysis.tistory.com/127)

#### 3. 경사하강법 (순한맛)

- 시각화 자료를 찾아봄 [링크1](https://towardsdatascience.com/a-visual-explanation-of-gradient-descent-methods-momentum-adagrad-rmsprop-adam-f898b102325c) [링크2](https://bl.ocks.org/EmilienDupont/aaf429be5705b219aaaf8d691e27ca87)
- 유튜브 "뉴턴 vs 라이프니츠의 미적분 이야기"
- 단일 변수일때는 `abs`, 벡터 (다변수)일때는 `norm`을 활용

#### 4. 경사하강법 (매운맛)

- norm = 벡터공간에 존재하는 함수 --> 전개식 자체로 계산하는 것이 맞음
  - $L_{0}-norm$: 0이 아닌 것의 개수
  - $L_{infinite}-norm$ : $max(x_k)$
- 차원이 증가할수록 기존의 선형회귀와 다르게 handling이 어려움
  - 각 차원별로 계수값이 곧 $\beta$
  - 따라서 각 차원별로 편미분을 진행함
- 경사하강법 공식 전개시 $\beta_{k}$가 존재하는 부분을 제외한 속미분 값은 다 0으로 됨
  - 추가로$ L_{2}-norm$은 루트를 갖는 식으로 미분을 진행해도 역수를 취한 값으로 처리됨
  - 따라서 편미분 결과의 분자에 있는 값이 나오게 됨

### 멘토님 미팅 시간 정하기

- 월목