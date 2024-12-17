## **지도학습 개요**

- **정의**: 지도학습은 입력 데이터와 정답 데이터(타겟)를 활용해 모델을 학습시키는 방법입니다.
- **사용 분야**: 분류(Classification)와 회귀(Regression)
- **주요 데이터셋**:
    - **Iris 데이터셋**
        - 특성: 꽃받침 길이/너비, 꽃잎 길이/너비
        - 클래스: setosa, versicolor, virginica (0, 1, 2)

## **데이터셋**

- **데이터셋 구성**
    
    - 데이터의 타입: `numpy.ndarray`
    - 데이터의 크기: `(150, 4)`
    - 특성 이름: `['sepal length', 'sepal width', 'petal length', 'petal width']`
    - 타겟 클래스: `[0, 1, 2]`
- **데이터셋 예제 코드**:
    
    ```python
from sklearn.datasets import load_iris
iris_dataset = load_iris()
print("키:", iris_dataset.keys())
print("특성의 이름:", iris_dataset['feature_names'])
print("데이터의 타입:", type(iris_dataset['data']))
print("데이터의 크기:", iris_dataset['data'].shape)
    ```
    
- **타겟 데이터**:
    
    ```python
print("타겟:", iris_dataset['target'])
print("타겟 크기:", iris_dataset['target'].shape)
    ```
    
    - 출력 예시: `[0, 0, 0, ... 1, 1, 2, 2]`

## **시각화**

- **산점도 시각화**:
    
    ```python
import matplotlib.pyplot as plt
import mglearn

X, y = mglearn.datasets.make_forge()
mglearn.discrete_scatter(X[:, 0], X[:, 1], y)
plt.legend(["클래스 0", "클래스 1"], loc=1)
plt.xlabel("첫 번째 특성")
plt.ylabel("두 번째 특성")
    ```
    
- **결과**: 특성 간 분포를 통해 데이터의 패턴을 확인할 수 있습니다.
    

## **데이터 나누기**

- **훈련 데이터와 테스트 데이터**:
    
    - 훈련 데이터: 모델 학습용
    - 테스트 데이터: 성능 평가용
    - 예시 코드:
        
        ```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(
	iris_dataset['data'], iris_dataset['target'], random_state=0)
print("훈련 데이터 크기:", X_train.shape)
print("테스트 데이터 크기:", X_test.shape)
        ```
        
- **산점도 행렬 시각화**:
    
    ```python
import pandas as pd
iris_dataframe = pd.DataFrame(X_train,
	columns=iris_dataset.feature_names)
pd.plotting.scatter_matrix(
	iris_dataframe, 
	c=y_train, 
	figsize=(15, 15), 
	marker='o'
)
    ```
