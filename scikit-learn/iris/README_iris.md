

1. [iris01]()

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
      6. [상관 분석]() iris.corr()
      7. 타겟별 통계 분석 iris.groupby("species").size() 
      8. 이상치 탐지 그래프 그리기 boxplot_iris(feature_names, dataset):
      9. 히스토그램 그리기 - 데이터의 분포 확인
      10. [상관관계]() 시각화 
          1. iris.corr()
          2. sns.heatmap(corr, cmap = cmap, vmax=1.0, vmin = -1.0, center =0, square= True, linewidths=.5, cbar_kws={'shrink':.5})
      11. [pairplot]() : 열의 모든 데이터에 대한 조합
   
   