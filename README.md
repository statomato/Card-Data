# Card-Data
> 카드매출 데이터 분석 및 시각화

## 1. 분석 방향, 목표 설정
## 2. EDA
#### (1) 파생변수 생성


|카테고리 | 변수 종류 | 내용 |
|:---|:----|:----|
|store 기본 정보 | n_card, count, total_amount, amount_q25, ... |  |
|시간대별 | t01_05,	t06_10,	t11_14,	t15_17,	t18_20,	t21_24, ...	 |  |
|요일, 공휴일별 | weekend_count, total_amount/n_days, holiday_amount/n_holiday, ... |  |
|고객별 | regular_percent | 일주일에 두번 이상 방문 고객 비중|










##### (2) clustering
![dendrogram](https://user-images.githubusercontent.com/44764167/107139647-40362800-6960-11eb-9b70-93fe40b8aefb.png)

- Wald Clustering
- 군집 9개로 결정

- 군집별 store 개수
![dataframe](https://user-images.githubusercontent.com/44764167/107139646-3f9d9180-6960-11eb-9906-a8f00d773d73.JPG)


#### (3) 시각화
- 레이더 그래프1 : 시간대별
![raderchart1](https://user-images.githubusercontent.com/44764167/107139644-3dd3ce00-6960-11eb-9464-fce9fecdf8d9.png)


- 레이더 그래프2 : amount, card 고객 수 관련 변수(Min-Max Scale)
![raderchart2](https://user-images.githubusercontent.com/44764167/107139645-3f04fb00-6960-11eb-9342-6dd9be6e4f1e.png)



#### (4) 군집 이름 결정
<img width="647" alt="cluster_표2" src="https://user-images.githubusercontent.com/44764167/107140548-17189600-6966-11eb-9444-f94ac8db0778.png">
<img width="927" alt="cluster_표1" src="https://user-images.githubusercontent.com/44764167/107140549-17b12c80-6966-11eb-92bb-730456b9ead9.png">
