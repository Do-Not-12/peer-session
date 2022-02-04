# Week3 - Day5

## Today Peersession

### Data viz

#### 1. Text(발표자 : 도리토스)
- text를 사용하면 오해를 줄일 수 있다.
- va, ha, rotatin으로 text 위치와 각도 조절 가능 
- bbox를 dict 형식으로 주면 여러 옵션을 줄 수 있다.

#### 2. Color(발표자 : 도리토스)
- 화려함이 시각화의 전부는 아니다.
- 명도, 채도, 보색을 활용해 색상 강조, 대비가 가능하다.

#### 3. Facet(발표자 : 폴라)
- facet은 분할하는 것
- sharex, sharey가 인상 깊었다.
- fig, axes를 받아와서 `axes.flatten()` 을 적용 하는 방식 자주 사용

#### 4. More Tips(발표자 : 써리)
- 포켓몬을 예시로 grid를 표현(Attck, Defense)
    - 기울기로 Attack, Defense의 밸런스 표현
    - 유사한 포켓몬을 볼 수 있다.
- axvspan을 사용해 rect를 만들수 있다
- style sheets에서는 default가 가장 깔끔했다

#### 5. Seaborn 기초(발표자 : 렉사)
- matplotlib과의 차이
    - seaborn은 여러 특화적 기능 제공
    - seaborn은 figure가 생성할 때 마다 시간 기록(oom)
    - 사용하기 쉽게 설정이 되어 있다.
- Seaborn API에 가면 자세한 기능 분류를 볼 수 있다.
    - 필요에 할때마다 찾아 쓰는 것이 좋다.

#### 6. Seaborn 심화(발표자 : 폴라)
- 많은 figure를 쓰기 보다는 분할해서 쓰는 것이 좋다
- detail하게 내부 setting이 가능하다
- catplot등의 기능을 사용하여 feature case별로 한눈에 볼 수 있다

### 심화포스팅

#### Magic Method (발표자 : 피터)
- Built-in 함수들이 처리할 연산을 정의함으로써, 마법같다고 하여 매직 메소드라한다.
- `__new__`와 `__init__`의 차이
- 그 밖에 객체 생성과 표현, 속성관리, 연산등 여러 magic method들이 있다.

#### Latex (발표자 : 폴라)
- MathJax Setting을 javascript로 적용
- basic 
    - _{}, ^{} 밑첨자, 윗첨자(중괄호 쓰는 것을 추천)
    - mathbf{} : 굵은 긁씨로 표현
- Vector, Matrix : begin으로 감싼다
- 간격 : quad 사용이 편하다

#### Color(발표자 : 렉사)
- 사람의 눈에는 3개의 망막세포가 있어서 색을 인식한다(rgb)
- 하지만 rgb에서 보이는 영역은 좁다
- 그래서 cmik라는 체계를 만들어냈다

#### PDP : partial dependece plot(발표자 : 써리)
- 기본적으로 tree 기반 모델은 입력과 출력의 관계를 알기힘들다
- PDP는 이런 모델의 입력과 출력의 관계를 볼 수 있게 해주는 시각화 그래프
- marginalizing(marginal effect)을 해준다
- 장점 : 직관적, 구현이 쉽다
- 단점 : 변수의 개수가 한정(2개까지), 해석오류의 여지, 다중공선성 문제가 없어야함

#### 추천시스템 (발표자 : 도리토스)
- 추천시스템 : 아이템을 바탕으로 어떤 추천을 할지 총괄한다
- Collaborative Filtering(협업 필터링)(가장 많이 사용)
    - 비슷한 성향이나 취향을 갖는 유저가 좋아한 아이템을 추천
    - 간단하면서 높은 정확도를 보여줌
- Knowledge-based Recommendation
    - 특정 도메인 지식을 바탕으로 아이템의 features를 활용한 추천    

    
