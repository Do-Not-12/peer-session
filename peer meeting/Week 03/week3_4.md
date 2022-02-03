# Week3 - Day4

## Today Peersession

#### 1. Introduction to Visualization (발표자 : 도리토스)
- 시각화는 단순히 예쁘게 그리는것이 아니다.
- 데이터의 종류
    - 수치형(연속형, 이산형)
    - 범주형(명목형, 순서형)
    - 정형, 시계열, 지리/지도, 관계. 계층 등등
- 시각화 이해
    - 마크와 채널
    - 전주의적 속성 : 기울기,길이, 너비 등 크기가 다르면 한 눈에 알아챌수 있는 속성
- Matplotlib
    - Figure라는 큰틀에 ax를 그린다.
    - text와 annotate의 차이
        - annotate는 화살표와 텍스트의 위치를 입력가능

#### 2. Bar Plot 사용하기 (발표자 : 써리)
- Principle of Proportion
    - 시각화 방법에 따라 인지오류가 많다.
    - 예시) [기사](http://www.ohmynews.com/NWS_Web/View/at_pg.aspx?CNTN_CD=A0002543684&CMPT_CD=TAG_PC) : 실업률 그래프에서 y축을 통일해서 보면 시작점에서 차이가 크다.
- stack bar
    - bottom인자에는 하나의 data만 넣어야한다.
- grid
    - zorder : grid를 bar 뒤에 둘지 앞에 둘지 결정(낮을 수록 뒤에 나타난다.)    

#### 3. Line Plot 사용하기 (발표자 : )
- line()이 아닌 plot() 사용 (Line이라고 특수취급 하는것이 아님)
- 이동평균 : 부분적으로 그래프에서 튀는 요소를 평균을내서 줄임
- 이중 축 : 그래프가 서로 다른 내용일 때는 주의해서 사용

#### 4. Scatter Plot 사용하기 (발표자 : )
- 책 추천 : 팩트풀리스(통계적 오류에 관해)
- grid 사용은 지양한다
- 군집화에 많이 사용

#### 심화포스팅 주제 논의
- 폴   라 : Latex
- 피   터 : 
- 렉   사 : loss 함수 오류?
- 써   리 : partial dependece plot
- 도리토스 : 