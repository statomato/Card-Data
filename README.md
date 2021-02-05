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
![dendrogram](https://user-images.githubusercontent.com/44764167/107056802-11ac3600-6816-11eb-9a73-7d4d7daeb0ea.png)

- Wald Clustering
- 군집 8개로 결정

- 군집별 store 개수
![image](https://user-images.githubusercontent.com/44764167/107057286-a151e480-6816-11eb-9805-9744b8ad1733.png)


#### (3) 시각화
- 레이더 그래프1 : 시간대별
![raderchart1](https://user-images.githubusercontent.com/44764167/107056793-107b0900-6816-11eb-8918-af96fb337c31.png)

- 레이더 그래프2 : amount, card 고객 수 관련 변수(Min-Max Scale)
![raderchart2](https://user-images.githubusercontent.com/44764167/107056800-11ac3600-6816-11eb-9d3d-d993ce4f6175.png)
