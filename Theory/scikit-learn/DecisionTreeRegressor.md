[`sklearn.tree`](https://scikit-learn.org/stable/modules/classes.html#module-sklearn.tree).[DecisionTreeRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeRegressor.html)

1. `criterion`='squared_error',  **{“squared_error”, “friedman_mse”, “absolute_error”, “poisson”}, default=”squared_error”**
   1. `squared_error` = Mean squared error
   2. `friedman_mse` = 
   3. `absolute_error` = Mean absolute error
   4. `poisson` = Poisson distribution
2. `splitter`='best',  **{“best”, “random”}, default=”best”** 분할 선택 방법
3. `max_depth`=None,  **int, default=None** 트리의 최대 깊이
4. `min_samples_split`=2,  **int or float, default=2** 노드 분할하는 최소 샘플 수
   1. 정수이면 최소 개수이고
   2. float 이면 분수로 생각한다 `ceil(min_samples_split * n_samples)` 올림 하는듯
5. `min_samples_leaf`=1,  **int or float, default=1**
   1. 리프 노드에 있어야 하는 최소 샘플 수
   2. 정수이면 최소 개수이고
   3. float 이면 분수로 생각한다 `ceil(min_samples_split * n_samples)`
6. `min_weight_fraction_leaf`=0.0,  **float, default=0.0**
   1. 가중치 합계 지정하지 않으면 샘플은 동일한 가중치를 가진다
7. `max_features`=None,  **int, float or {“auto”, “sqrt”, “log2”}, default=None**
   1. 최상의 분할을 찾을 때 고려해야 할 feature의 수
   2. If int, then consider `max_features` features at each split.
   3. If float, then `max_features` is a fraction and `max(1, int(max_features * n_features_in_))` features are considered at each split.
   4. If “auto”, then `max_features=n_features`.
   5. If “sqrt”, then `max_features=sqrt(n_features)`.
   6. If “log2”, then `max_features=log2(n_features)`.
   7. If None, then `max_features=n_features`.
8. `random_state`=None,  
9. `max_leaf_nodes`=None,  **int, default=None**  leaf node 개수 제한
10. `min_impurity_decrease`=0.0,   **float, default=0.0**
11. `ccp_alpha`=0.0  