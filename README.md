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
![dendrogram](https://user-images.githubusercontent.com/44764167/107059873-a82e2680-6819-11eb-9077-4245cd0fbd36.png)

- Wald Clustering
- 군집 9개로 결정

- 군집별 store 개수
![image](https://user-images.githubusercontent.com/44764167/107059436-21794980-6819-11eb-9943-9aa500022412.png)


#### (3) 시각화
- 레이더 그래프1 : 시간대별
![raderchart1](https://user-images.githubusercontent.com/44764167/107059750-8634a400-6819-11eb-9701-c336358e116f.png)


- 레이더 그래프2 : amount, card 고객 수 관련 변수(Min-Max Scale)
![raderchart2](https://user-images.githubusercontent.com/44764167/107059754-86cd3a80-6819-11eb-87ac-a2710331abee.png)
