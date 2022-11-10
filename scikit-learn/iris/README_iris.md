

1. [iris01](https://github.com/LeeJeaHyuk/python/blob/master/scikit-learn/iris/iris01.ipynb)

   1. 데이터 로드
      1. key값 확인
   2. EDA dataframe 변환
      1. data와 target값 확인 후 dataframe으로 합치기 pd.concat([features, target], axis=1)
      2. 컬럼명에서 공백 지우기 iris.rename({'sepal length (cm)':'sepal_length',}, axis=1, inplace=True)
      3. target값 target_names으로 mapping iris['species']=iris.species.map(lambda x : data.target_names[x])
      4. 결측값 확인 iris.isna().sum(axis=0)
      5. 기초 통계 분석
         1. iris.info()
         2. iris.describe()
      6. [상관 분석](https://github.com/LeeJeaHyuk/python/blob/master/Theory/statistic/correlation%20coefficient.md) iris.corr()
      7. 타겟별 통계 분석 iris.groupby("species").size() 
      8. 이상치 탐지 그래프 그리기 boxplot_iris(feature_names, dataset):
      9. 히스토그램 그리기 - 데이터의 분포 확인
      10. [상관관계](https://github.com/LeeJeaHyuk/python/blob/master/Theory/statistic/correlation%20coefficient.md) 시각화 
          1. iris.corr()
          2. sns.heatmap(corr, cmap = cmap, vmax=1.0, vmin = -1.0, center =0, square= True, linewidths=.5, cbar_kws={'shrink':.5})
      11. [pairplot](https://github.com/LeeJeaHyuk/python/blob/master/Theory/seaborn/sns.pairplot.md) : 열의 모든 데이터에 대한 조합
      12. hold out : 데이터 분리
          1. train, test로 데이터를 나누는 것 train_test_split
   3. 학습
      1. DecisionTreeClassifier 결정트리 분류 사용
         1. 모델을 먼저 만들고 fit한
   
      2. 일반화 (과대적합되지 않는다는 것을 의미하는듯)
         1. train set 이외에도 validation set을 활용하여 과적합이 되어있는지 확인한다
         2. cross validation : validation set을 여러 개 만들어서 모든 데이터가 한 번씩 학습되게 한다
         3. 코드 from sklearn.model_selection import cross_val_score, KFold
         4. 클래스를 균등하게 교차 검증 : StratifiedKFold
   
      3. 소규모 데이터 그래프(sklearn에서 제공) import scikitplot as skplt
      4. 모델 최적화 전략
         1. 하이퍼파라미터 튜닝
         2. [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html#sklearn.model_selection.GridSearchCV)를 사용하여 파라미터를 자동으로 튜닝
            1. GridSearchCV로 최적화 파라미터 찾으면 저장해서 다음에는 바로 볼수 있게 하기(아직 안함)
   
         3. 최적화를 여러가지 모델로 튜닝
            1. DecisionTreeClassifier
            2. RandomForestClassifier (하이퍼파라미터 더 확인해보기)
            3. 서포트 벡터 머신(아직 안함)
   
   4. 최종 평가
      1. 예측과 정답 확인
      2. [**Confusion Matrix**]()
   
   
   
