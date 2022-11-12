## real estate

1. [RealEstate01]() // 링크 추가
   1. **데이터 로드**
      1. execl(xlsx) 파일 불러오기 pd.read_excel(, engine='openpyxl')
         1. [real estate valuation data 원본 링크](https://archive.ics.uci.edu/ml/datasets/Real+estate+valuation+data+set)
      2. 불러왔을 때 타입 <class 'pandas.core.frame.DataFrame'>
      3. key값 확인
   2. EDA  - DataFrame 변환
      1. no 값(index값) 제거 .drop("No", axis ='columns')
      2. rename({'column': 'rename column',...},axis=1, inplace=True)
      3. 결측값 확인 .isna().sum(axis=0)
      4. 상관 분석 .corr()
      5. 이상치 확인 - boxplot
      6. 히스토그램 - 각 특성의 성향 분석
      7. 상관관계 시각화
         1. target feature을 제외하고 특성을 살펴보아서 상관관계가 높은 특성이 존재하면 제외을 생각해보아야 한다 - [**다중공선성**]() 문제 회피하기 위해 //다중공선성 추가하기
      8. pairplot - 전체 feature 사이의 관계 확인
      9. 데이터 분리 from sklearn.model_selection import train_test_split
      10. 데이터 정규화 from sklearn.preprocessing import StandardScaler
          1. X_train_scale = std_scaler.fit_transform(X_train)
          2. X_test_scale = std_scaler.transform(X_test) test에는 fit을 하지 않는다는 것을 기억하기
   3. 학습
      1. 회귀로 훈련 from sklearn.tree import DecisionTreeRegressor
         1. score 확인 model.score(X_test,y_test) 
      2. 일반화 작업
         1. from sklearn.model_selection import cross_val_score, KFold
         2. skplt으로 그림 그리기 import scikitplot as skplt
      3. 각 모델의 Hyperparameter
         1. [**LogisticRegression**]() //링크 추기
         2. [**DecisionTreeRegressor**]() // 링크 추가
         3. [**LinearRegression**](*) // 링크 추가
      4. [GridSearchCV]() 를 사용해서 최적의 Hyperparameter 찾아내기 // 링크 추가
         1. 최적값 확인
         2. 