



## sklearn.tree.[**DecisionTreeClassifier**](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)

1. *criterion={“gini”, “entropy”, “log_loss”}, default=”gini”
   1. `Criterion`: 노드 분할 결과 품질을 평가하기 위한 기준. Gini와 Entropy 중에서 선택할 수 있으며 기본값은 Gini이다.

2. *splitter*={“best”, “random”}, default=”best”
   1. `Splitter`: 노드를 분할하기 위한 기준값 설정법. Best와 Random 중에서 선택할 수 있으며 기본값은 Best이다.
3.  *max_depth* = int, default=None
   1. `Max Depth`: 모델(나무) 성장 제한 기준. 몇 단계(깊이) 까지 성장시킬지 지정
   2. 트리가 깊어질수록 더 잘게 분류를 시키므로 일반적으론 정확도가 높아진다
4. *min_samples_split*= int or float, default=2
   1. `Min Samples Splits`: 노드 분할에 필요한 최소 표본 수. 이 숫자가 매우 작으면 과적합, 반대의 경우 과소적합이 발생
5. *min_samples_leaf* = int or float, default=1
   1. `Min Samples Leaf`: 잎사귀(말단) 노드가 되기 위한 최소 표본 수. 지정 숫자보다 노드에 더 많은 표본이 있을 경우 노드 분할 가능성이 있음
6. *min_weight_fraction_leaf* = float, default=0.0
   1. `Min Weight Fraction Leaf`: 잎사귀(말단) 노드에 필요한 가중치 합계의 최소 가중치 비율
7. *max_features* = int, float or {“auto”, “sqrt”, “log2”}, default=None
   1. `Max Features`: 최적 분할(best split)시 고려하는 변수의 개수. 입력 누락시 훈련에 사용하는 변수 개수로 자동 설정
8. *random_state=None*, 
   1. `random_state`: 결과를 고정하기 위해 지정하는 자연수
9. *max_leaf_nodes = int, default=None
   1. `Max Leaf Nodes`: 모델(나무) 성장시 최우선으로 고려하는 기준. 최적 잎사귀(말단) 노드 개수는 불순도의 상대적인 감소로 정의. 입력 누락시 무한대로 설정
10. *min_impurity_decrease* = float, default=0.0
    1. `Min Impurity Decrease`: 여기에 설정한 값 이상으로 불순도가 감소할 경우 노드를 분할
11. *class_weight* = dict, list of dict or “balanced”, default=None
    1. `Class Weights`: 종속변수 각 수준에 부여되는 가중치. 입력 누락시 균등 가중치. 가중치 부여는 사전식 순서
12. *ccp_alpha* = non-negative float, default=0.0
    1. *ccp_alphanon*-negative=float, default=0.0 #값이 커지면 tree가 단순해진다.

-`Feature Columns`: 독립변수 지정
-`Label Column`: 종속변수 지정
-(lexicographical order)를 따름
-`Group By`: 특정 변수를 기준으로 연산을 별도로 실시

-`Prediction Column Name`: 예측값이 들어갈 변수 명
-`Probability Column Prefix`: 예측값의 확률값이 들어갈 변수의 접두사
-`Suffix Type`: 예측값의 확률값이 들어갈 변수의 접미사.



