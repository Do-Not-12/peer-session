# Week 7 - Day3

## Today peersession

### 각자 한 것들

- 도리토스
  - transform 여러가지 진행해봤으나 성능 향상은 없었음
  - REsNet34로 변경해서 learning rate 낮춰서 진행할 듯
  - 커널 7X7 -> 3X3 변경

- 렉사
    - learning rate 1e-5로 낮추니까 성능향상
    - learning rate 감소가 의미가 있는 것으로 보임
    - 나이를 따로 예측한 것만 추가로 덧데어 보는 방식 추가

- 피터
    - learning rate 1e-3 -> 1e-5 했더니 0.5766 -> 0.6671로 향상

- 써리
  - augmentation 데이터 추가해서 진행
  - 60세이상 마스크 안 쓴 사람만 증강 (6배 증강)
  - 성능 차이는 크게 없는 것으로 보임

- 폴라
  - Efficient Net b5로 이미지 상반신 부근만 처리
  