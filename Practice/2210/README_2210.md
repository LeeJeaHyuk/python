# 2210 npPrac01

##### 깃 오류

---

LF will be replaced by CRLF the next time Git touches it

git config --global core.autocrlf true

---

 pr01-1

- csv파일을 불러오기 pd.read_csv
- 불러온 csv파일을 dataframe으로 앞뒤 n줄 출력하기 .head() .tail()

 pr01-2

- dataframe의 수치 정보를 확인 .describe()
- dataframe 의 size를 확인 .shape
- dataframe을 요약 .info()
  - dtype, null, column 등

pr01-3

- df 특정 열에만 통계함수를 적용
  - .num() .max() .min() .mean() .count()

pr01-4

- df 특정 열에 특성의 개수를 파악할 수 있다 .value_counts()
  - ex)  장르의 개수가 몇 개인지

pr01-5

- 몇몇 개의 열을 골라서 출력할 수 있다
- 몇몇 개의 행을 골라서 추출할 수 있다
  - loc과 iloc
  - range와 slicing 사용
- 특정 행에서 특정 열만 출력할 수 있다
  - 1,3,5,7 행에서 'title' 'genre' 'box_off_num' 열만 출력

pr01-6

- boolean indexing을 통해  특정 데이터를 추출
  - 주제가 공포인 데이터만 추출
  - 주제가 공포인 데이터에서 'title','genre' 만 추출
  - 관객수가 평균 이상인 영화 정보
- boolean indexing조건이 2개일때
  - 주제가 공포이면서 'title','genre' ,'time' 열이면서 시간이 90이하인 데이터 추출

pr01-7 

- groping 
  - 그룹핑 하기 .groupby()
  - 그룹의 개수 리턴 .ngroups
  - 키값 확인 . groups.keys()
  - 특정 키값의 value 전달 .get_group()
- 그룹핑한 후 집계함수 사용
  - df_screenRat['genre'].count()

- GroupBy.agg()를 사용해서 여러 열의 집계함수 동시에 보기
  - .agg('집계함수')[['특정 열 나열']]
  - .agg({'특정 열':통계함수, '특정 열2':통계함수2}) 각각을 다른 통계함수로 지정할 수 있음
- 사용자 정의 함수를 만들어서

\# pr01-8 

- 시계열 데이터 사용

- df 컬럼을 시계열 객체로 변환

  - df['my_date']=pd.to_datetime(df['release_time'])

- 변환한 시계열 객체 분철하기

  - df['year'] = df['my_date'].dt.year

- 연도별 최대 관객수 

  - df.groupby('year')['box_off_num'].max()

  

\# pr01-9

- 누락데이터 확인
  - titanic.isnull().sum()
- 누락데이터 제거 / 삭제
  - titanic.dropna(axis=1,thresh = 400)
  - axis = 1 열 전체 삭제
    - row(891)-thresh(400) = null값이 491보다 많으면 열 삭제
    - res = titanic.dropna(axis=1,thresh = 400)
  - axis = 0 행 전체 삭제
    - column(15)-thresh(14) = 1  널값이 2개이상이면 해당 열 삭
    - res02 = titanic.dropna(axis=0,thresh = 14)
- 누락데이터 치환하기
  - titanic['age'].fillna(titanic['age'].mean(), inplace = True)
  - 최빈값으로 치환히기.idxmax()
    - titanic['embarked'].value_counts(dropna=False).idxmax()
  - 최소값 .idxmin()
    - titanic['embarked'].value_counts(dropna=False).idxmin()