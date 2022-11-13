## [`sklearn.linear_model`](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.linear_model).[LogisticRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)

1. [`penalty`]()='l2',  {‘l1’, ‘l2’, ‘elasticnet’, ‘none’}, default=’l2’  //norm에 대해 링크
   1. elasticnet : 모두 추가
2. `dual`=False,  
   1. True, False 
   2. liblinear L2일 경우만 True 가능
3. `tol`=0.0001,  {default = 1e-4}
   1. 중지 기준에 대한 허용 오차 
4. `C`=1.0,  
   1. Inverse of regularization strength
   2. 작은 값일수록 더 강한 정규화를 지정한다
   3. 값이 크면 약한 규제 -> 훈련 데이터에 과대적합 가능성
   4. 값이 작으면 강한 규제 -> 훈련 데이터에 과소적합 가능성
5. `fit_intercept`=True,  {**bool, default=True**}
6. `intercept_scaling`=1,  {**float, default=1**}
7. `class_weight`=None,  {**dict or ‘balanced’, default=None**}
   1. 클래스에 대한 가중치들의 값
   2. 지정하지 않으면 클래스들의 모든 가중치가 1이 된다
   3. balenced 이면 클래스 빈도에 반비례하게 자동으로 지정됨  `n_samples / (n_classes * np.bincount(y))`.
   4. 값을 지정하면 지정한 값으로 정해지는듯?
8. `random_state`=None,  seed
9. `solver`='lbfgs',  **{‘newton-cg’, ‘lbfgs’, ‘liblinear’, ‘sag’, ‘saga’}, default=’lbfgs’**
   1. [`lbfgs`](https://ko.wikipedia.org/wiki/L-BFGS) : L2
   2. [`newton-cg`](https://en.wikipedia.org/wiki/Newton%27s_method_in_optimization) :  L2
   3. [‘sag’]() : L2
   4. [`liblinear`]() : L1,L2 모두 지원
   5.  [` saga `]() L1,L2 모두 지원
   6. 참조
      1. [Hessian matrix wiki](https://ko.wikipedia.org/wiki/%ED%97%A4%EC%84%B8_%ED%96%89%EB%A0%AC) , [참조 블로그](https://angeloyeo.github.io/2020/06/17/Hessian.html)
      2. [stack overflow](https://stackoverflow.com/questions/38640109/logistic-regression-python-solvers-definitions)
10. `max_iter`=100, {**int, default=100**} 최대 반복 값
11. `multi_class`='auto',  **{‘auto’, ‘ovr’, ‘multinomial’}, default=’auto’**
    1. ovr : binary problem
    2. liblinear 이면 multinomial 사용 불가
    3. auto 는 이진 데이터 혹은  solver='liblinear' 이면 ovr을 선택 아니면 multinomial 선택
12. `verbose`=0,   0 은 출력하지 않고, 1은 자세히, 2는 함축적인 정보만 출력
13. `warm_start`=False,  
    1. True로 설정하면 초기화에 맞게 이전 호출의 솔루션을 재사용하고, 그렇지 않으면 이전 솔루션을 지웁니다.
    2. liblinear일 경우 불가
14. `n_jobs`=None,   cpu core 수 -1이면 최대
15. `l1_ratio`=None  
    1. 









