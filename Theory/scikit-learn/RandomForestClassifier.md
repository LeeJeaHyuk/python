## [`sklearn.ensemble`](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.ensemble).[RandomForestClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

[DicisionTreeClassifier](https://github.com/LeeJeaHyuk/python/blob/master/Theory/scikit-learn/DecisionTreeRegressor.md) 와 비슷하다

### HyperParameter

1. *n_estimators* = **int, default=100**
   1. The number of trees in the forest.
   2. 
2. *criterion* = **{“gini”, “entropy”, “log_loss”}, default=”gini”**
3. *max_depth*=**int, default=None**
4. *min_samples_split*=**int or float, default=2**
5. *min_samples_leaf*=**int or float, default=1**
6. *min_weight_fraction_leaf*=**float, default=0.0**
7.  *max_features*=**int, float or {“auto”, “sqrt”, “log2”}, default=None**
8. *max_leaf_nodes*=**int, default=None**
9. *min_impurity_decrease*=**int, default=None**
10. *bootstrap*=**float, default=0.0**
11. *oob_score*=**bool, default=False**
12. *n_jobs*=**int, default=None**
13. *random_state*=None, 
14. *verbose*=**int, default=0**
15. *warm_start*=**bool, default=False**
16. *class_weight*=**{“balanced”, “balanced_subsample”}, dict or list of dicts, default=None**
17. *ccp_alpha*=**non-negative float, default=0.0**

### 이론

배깅 또는 페이스팅을 사용한 결정 트리의 앙상블



