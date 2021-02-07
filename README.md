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

- 0번 : 백화점? (단골비율 높고, 1인당 결제 금액이 높음, 금요일 결제가 제일 많음)
- 1번 : 편의점 (방문고객 많고, 단골 비율 낮고, 1인당 평균 결제 금액 낮고, 공휴일 영업일수 많음)
- 2번 : 서비스업 (주중보다 주말 결제 금액이 크고, 단골 비율이 낮음)
- 3번 : 큰 금액 규모 행사매장 (이상치, 며칠 열지 않았으나, 1인당 결제 금액이 큼, 할부 많이 함)
- 4번 : 쇼핑몰? (이상치, 0번과 비슷하나, 방문고객 수가 압도적으로 많고 영업일수에 있어서 2배 가량 차이를 보임)
- 5번 : 술집 (밤, 새벽에 집중되어 있으며, 주중보다 주말 매출액이 높음)
- 6번 : 저녁 식당 or 회사 근처 술집 (저녁, 밤 집중되어 있으며, 주중이 주말보다 훨씬 매출액이 높음)
- 7번 : 식당 (식사 시간에 집중, 주말 평균 판매액이 평일보다 높음, 공휴일 평균 매출액이 평소보다 낮음)
- 8번 : 야식 (배달) 식당 (5번과 비슷하나, 새벽보다는 저녁시간에 더 집중되어 있음)


- 0번과 4번의 경우 한 군집으로 묶어도 될 듯하다.
