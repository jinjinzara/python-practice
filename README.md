# 데이터 분석을 위한 Python

## Lecture 4: Datatype
<details>
<summary>실습 내용</summary>
<div markdown="1">

1. **키워드(예약어)**
    1. 키워드 이름은 변수 이름으로 사용할 수 없고, 만약 사용한다면 에러 출력됨
       
2. **변수와 상수**
    1. 한 변수에 다른 변수를 할당했을 때, 즉 상수 자리에 변수를 넣었을 때 일어나는 일 살펴보기
    2. 두 변수에 들어있는 값을 서로 바꾸는 방법은?
       
3. **기본 자료형**
    1. 숫자형: int 와 float 타입의 차이
    2. 문자형: 문자열의 덧셈과 곱셈 활용하기, 줄바꿈 개행문자 \n
    3. 논리형: 3개 이상의 조건, and와 or 그리고 &와 |
    4. 자료형 변환 응용 문제
        1. int와 bool, str과 bool 변환하기: boolean 자료형 변환을 통해 int의 경우 0인지 아닌지, str의 경우 문자열이 비어있는지 아닌지 검사
        2. int와 float 변환하기: 정수에서 실수로 변환할 때, 실수에서 정수로 변환할 때 소수점 자리수의 변화 살펴보기
           
4. **시퀀스 자료형**
    1. String: 인덱싱에서 start, end, step 활용하기, 포함 여부 확인하는 in과 not in 활용하기
    2. Tuple: 튜플 값이 하나일 때는 반드시 뒤에 콤마(,) 추가, 인덱싱과 슬라이싱
    3. List
        1. 리스트의 값 수정, 추가, 삭제
        2. 리스트 값 삭제 함수 remove와 del의 차이
        3. 두 리스트 합치기
    4. Dictionary
        1. 딕셔너리의 새로운 key, value 추가
        2. key 값으로 value 찾는 2가지 방식
        3. 딕셔너리의 함수 keys(), values()
    5. Set: set은 중복을 허락하지 않는 자료형이므로 리스트 자료형의 중복 제거에 활용 가능

</div>
</details>

## Lecture 5: Python Basic
<details>
<summary>실습 내용</summary>
<div markdown="1">

1. **파이썬 연산자**
    1. 산술 연산자의 순서는 일반적인 사칙연산과 동일한 규칙을 따름 (곱셈, 나눗셈이 먼저)
    2. 비교 연산자를 여러 개 쓰면 and 조건이 있는 것처럼 취급됨
    3. 논리 연산자를 여러 개 이어서 쓰면 왼쪽으로부터 오른쪽으로 묶임
       
2. **파이썬 입출력 명령어**
    1. format 함수를 사용하여 출력 가능
       1. 중괄호를 앞에서부터 순서대로 채우며, 소수점 자리수 등을 format 함수로 표현할 수 있음
    3. input 함수의 기본 형식은 String 이므로, 문자열이 아닌 숫자 등을 입력받을 때는 type을 지정해줘야 함

3. **파이썬 제어문**
    1. if 문 (조건문)
        1. 1-line으로 표현하는 코드는 파이썬이라는 언어의 가장 큰 강점 중 하나임
        2. 간결한 코드를 위해 복잡하지 않은 if 문은 1-line 코드로 설계하는 것을 권장
        3. 예제 1: 두 숫자 중에 더 큰 수를 구하기 (일반적인 코드, 1-line 코드 모두 해보기)
        4. 예제 2: 둘 중에 더 큰 수를 구하고, 두 수가 같을 때는 0을 출력하게 하기

4. **for 문 (반복문)**
    1. 1-line for 문
    2. for, if를 1-line으로 동시에 함께 사용할 수도 있음.
    3. 예제 1: 리스트에서 50이 넘는 수는 몇개? 
    4. 예제 2: 소수 찾기

</div>
</details>

## Lecture 6: Pandas
<details>
<summary>실습 내용</summary>
<div markdown="1">

1. **데이터 살펴보기**
    1. head(), info(), describe() 함수 사용해보기
    2. 세 함수의 차이점 비교
       
2. **데이터 합치기**
    1. 행 기준으로(위아래로) 합치기: concat() 함수 사용
    2. 열 기준으로(옆으로): concat() 함수로 합치기, merge() 함수로 합치기
       1. merge() 함수는 SQL 의 JOIN 연산과 동일한 동작을 수행
       
3. **행, 열 삭제하기**
    1. 행 삭제: drop() 함수로 인덱스 직접 지정하여 삭제, drop_duplicates()로 중복되는 행 삭제
    2. 열 삭제: drop(axis=1) 함수로 칼럼 name 지정하여 삭제, 한 번에 여러 칼럼도 삭제 가능
       
4. **결측값 처리하기**
    1. 칼럼별 결측값 개수 확인하기
    2. 결측값 처리 방법 1) 결측값 존재하는 데이터(행)를 삭제
    3. 결측값 처리 방법 2) 결측값을 새로운 값으로 대체 (사용자가 지정한 임의의 값 또는 평균, 중앙값 등 대표값)

5. **그룹화**
    1. 칼럼의 값에 따라 데이터를 그룹화하는 함수 groupby()
    2. 그룹 객체 만들기
    3. 특정 그룹만 출력하기
    4. 그룹별 통계량 계산하기: sum(), mean() 등
6. **칼럼 변경하기**
    1. rename() 함수로 칼럼 이름 변경하기
    2. astype() 함수로 칼럼 type 변경하기
7. **apply 함수**
    1. 행 단위로 반복 작업을 수행할 때, 함수를 만든 뒤 apply()를 사용해 일괄 적용시킬 수 있음
8. **문자열 처리 함수 str**
    1. type이 문자열인 칼럼에 대해서만 사용 가능
    2. str.contains(): 특정 문자열의 포함 여부
    3. str.upper(), str.lower(): 문자열을 대문자 또는 소문자로 바꾸기
    4. 그 외에도 split(), strip(), replace() 등의 기능이 존재
    5. 텍스트 데이터를 pandas로 다룰 때 편리하게 쓰이는 함수

</div>
</details>

## Lecture 7: EDA
<details>
<summary>실습 내용</summary>
<div markdown="1">

1. **데이터 불러오기**
    1. marathon_results_2015.csv, marathon_results_2016.csv, marathon_results_2017.csv
    2. 보스턴에서 개최한 마라톤의 3년간의 참가자 기록 데이터
    3. 데이터 불러온 후, 병합 가능한지 살펴보기 위해 칼럼 확인
       
2. **데이터 전처리**
    1. 연도 데이터 보존 위해 새로운 칼럼인 Year 생성
    2. 2015, 2016, 2017 세 데이터셋을 병합
    3. 결측치 확인
    4. 결측치가 많거나, 분석에 의미가 없는 칼럼(예: 참가자 ID, Index 등) 제거
    5. 파이썬 시간 데이터 전처리: String을 timedelta 객체로 변환, timedelta 객체를 분 단위의 시간으로 변환.

3. **EDA - Table 요약**
    1. describe() 함수: 데이터의 요약 통계량 확인
    2. 참가자 나이(Age), 출신 도시(City), 국적(Country)에 따른 마라톤 기록 차이 비교
    3. 평균값, 중앙값, 최빈값 보기: mean(), median(), mode()
    4. EDA 시 주의사항: 대표값이 무엇인지에 따라, 표본의 크기에 따라 편향된 결과가 발생
    5. 예) Country에 따른 마라톤 기록 차이
    6. 국가 별로 기록에 차이가 있는 것처럼 보였지만, 참가자 수 기준 상위 20개국 기준으로 살펴봤을 때 기록에 큰 차이가 없음
    7. 작은 표본에서 몇몇 outlier들이 대표값에 영향을 미쳐 차이가 발생한 것처럼 보였던 것

4. **EDA - Graphic 시각화**
    1. 마라톤 기록(Official Time) 분포표 시각화
    2. 마라톤 기록(Official Time)과 생물학적 성별(M/F) 간의 Boxplot 시각화
    3. 마라톤 기록(Official Time)과 국가(Country) 간의 Barplot 시각화
    4. 마라톤 기록(Official Time)과 나이(Age) 간의 scatterplot 및 density 시각화
    5. 시각화에서는 각 변수들이 마라톤 기록과 큰 관련이 있는 것으로 보이지는 않음
    6. 마라톤 기록 상위 10퍼센트에 대해 scatterplot 시각화 시도하니, 연령과 기록 간의 관계 드러남
    7. 변수 간의 상관관계 분석 후 Heatmap 시각화: City, Country와 마라톤 기록 간의 낮은 상관관계 드러남

</div>
</details>

## Lecture 8: Data Visualization with Boston Marathon dataset
<details>
<summary>실습 내용</summary>
<div markdown="1">

**Kaggle의 “Boston Marathon 2015, 2016 & 2017” 데이터를 이용한 데이터 시각화 실습을 수행**  
  https://www.Kaggle.com/datasets/rojour/boston-results
  https://pandas.pydata.org/pandas-docs/stable/user_guide/visualization.html#visualization  

**데이터 불러오기 및 전처리는 이전 회차와 거의 동일**  
- State 데이터 사용을 위한 USA, CAN (미국, 캐나다) 외의 데이터 drop

- 시각화 실습의 진행 과정
1. **Bar plot**
    1. 캐나다 국적 참가자들의 출신 State 분포 시각화
    2. figure 사이즈 변경, 분류 기준 추가, x축과 y축의 label 텍스트 지정, 범례 변경, 차트 제목 지정
       
2. **Histogram**
    1. 2015-2017 전체 마라톤 기록 데이터 분포 시각화
    2. 집계 방식 변경, bar 너비 변경, KDE 추가
       
3. **Box plot**
    1. 연도에 따른 마라톤 기록 데이터 분포 시각화
    2. 분류 기준 추가, box 너비 변경

4. **Area plot**
    1. 연도별 winner의 각 Stage 기록을 시각화 (실습영상 오타, 원고가 맞습니다.)
    2. 범례 변경, x축 눈금의 text label 변경, 범례 위치 지정

5. **Scatter plot**
    1. 첫 번째 Stage의 기록과 최종 마라톤 기록 간의 관계 시각화
    2. 데이터 범위 변경(하위 10%), 마커 size와 color 변경

6. **Pie chart**
    1. 마라톤 참가자들의 나이 시각화
    2. 연령이 너무 다양하므로 구간별 데이터로 변경하여 pie chart 시각화
    3. 소수점 첫째자리까지 반올림하여 비율 % 표기

</div>
</details>

## Lecture 12: Prediction with Marathon Dataset
<details>
<summary>실습 내용</summary>
<div markdown="1">

**참고 실습 코드**  
  https://www.kaggle.com/code/yardenlevy94/data-science-test-boston-marathon-15-17

1. **데이터 적재**
    1. Boston marathon 데이터 2015-2017 병합

2. **데이터 탐색 및 전처리**
    1. 불필요한 칼럼 제거
    2. 시간 데이터 파이썬의 time 객체로 변환 후 분 데이터로 변환
    3. Country(국가) 데이터를 Continent(대륙) 데이터로 변환
    4. 결측치 제거
    5. 범주형 변수에 대해 인코딩 수행

3. **학습 데이터와 시험 데이터 준비**
    1. train, test 데이터를 70%와 30%로 나눠서 준비

4. **지도 학습 모델 학습**
    1. Linear regression Lasso and Ridge Regression, Random Forest, XGBoost (파이썬 패키지에 존재)

5. **성능 평가 및 시각화**
    1. MSE, MAE: 예측값과 실제값 사이의 차이를 계산하여 모델의 분류 성능을 계산
    2. R square: 회귀 모델의 적합도를 계산
    3. Feature importance 시각화
       1. 가장 중요한 변수는 5K

</div>
</details>


## Lecture 13: Clustering with Iris dataset
<details>
<summary>실습 내용</summary>
<div markdown="1">

1. **데이터 적재**
    1. scikit-learn의 load_iris 함수에서 데이터 가져오기

2. **데이터 탐색**
    1. Pair plot 시각화로 각 변수들 간 관계를 파악

3. **비지도학습 모델 학습**
    1. K-means clustering, DBSCAN, Hierarchal clustering

4. **학습 결과 평가 및 시각화**
    1. 비지도학습은 지도학습과 달리 정답이 없는 문제로, 성능을 직접적으로 평가할 수 없음
    2. 대신, 군집화 결과를 시각화하여 분석가가 직접 판단하거나 inertia(within cluster sum of squares)와 지표로 같은 군집화의 품질을 평가할 수는 있음
    3. scatter plot 시각화
    4. dendrogram 시각화
    5. 분류 범주 결과 시각화

</div>
</details>

