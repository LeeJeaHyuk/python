## [`sklearn.linear_model`](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.linear_model).[LinearRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)

1. `fit_intercept`= True,  
2. `normalize` = 'deprecated',  
   1. This parameter is ignored when `fit_intercept` is set to False
   2. `fit_intercept`= True,  이면 회귀 전에 정규화해준다
      1. 표준화하고싶으면 미리표준화해주어야한다
3. `copy_X` = True,  **bool, default=True**
   1. True이면 복사된다
4. `n_jobs`= None,  -1이면 가장 빨리 계산함
5. `positive` = False **bool, default=False**
   1. When set to `True`, forces the coefficients to be positive. This option is only supported for dense arrays.