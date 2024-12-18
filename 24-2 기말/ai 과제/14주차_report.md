### **K-최근접 이웃 (KNN) 분류**

- KNN은 가장 가까운 K개의 이웃을 찾아 다수결 원칙으로 분류합니다.

**코드 예시**:

```python
from sklearn.neighbors import KNeighborsClassifier
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(iris_dataset['data'], iris_dataset['target'], random_state=0)

clf = KNeighborsClassifier(n_neighbors=3)
clf.fit(X_train, y_train)
print("테스트 세트 정확도:", clf.score(X_test, y_test))
```

- **결과**:
    - 테스트 세트 정확도: **0.86**

### **K-최근접 이웃 회귀**

- 회귀에서는 이웃의 평균값을 예측값으로 사용합니다.

**코드 예시**:

```python
from sklearn.neighbors import KNeighborsRegressor
X_train, X_test, y_train, y_test = train_test_split(X, y, random_state=0)

reg = KNeighborsRegressor(n_neighbors=3)
reg.fit(X_train, y_train)
print("테스트 세트 예측:", reg.predict(X_test))
print("테스트 세트 정확도:", reg.score(X_test, y_test))
```

- **결과**:
    - 테스트 세트 정확도: **0.83**

---

## **선형 모델**

### **선형 회귀 (Linear Regression)**

- 데이터를 선형 방정식 형태로 학습합니다: y^=w0x0+w1x1+⋯+b\hat{y} = w_0x_0 + w_1x_1 + \dots + b

**코드 예시**:

```python
from sklearn.linear_model import LinearRegression
lr = LinearRegression().fit(X_train, y_train)
print("훈련 세트 점수:", lr.score(X_train, y_train))
print("테스트 세트 점수:", lr.score(X_test, y_test))
```

- 결과 예시:
    - 훈련 세트 점수: **0.67**
    - 테스트 세트 점수: **0.66**

### **릿지 회귀 (Ridge Regression)**

- 모델의 가중치(ww)에 규제를 추가하여 과적합을 방지합니다.

**코드 예시**:

```python
from sklearn.linear_model import Ridge
ridge = Ridge().fit(X_train, y_train)
print("릿지 회귀 테스트 세트 점수:", ridge.score(X_test, y_test))
```

- 결과 예시:
    - **Alpha 값**에 따라 성능이 달라집니다.

### **라쏘 회귀 (Lasso Regression)**

- 불필요한 특성의 가중치를 0으로 만들어 특성 선택을 수행합니다.

**코드 예시**:

```python
from sklearn.linear_model import Lasso
lasso = Lasso(alpha=0.01, max_iter=100000).fit(X_train, y_train)
print("테스트 세트 점수:", lasso.score(X_test, y_test))
print("사용한 특성의 개수:", np.sum(lasso.coef_ != 0))
```

- 결과 예시:
    - 테스트 세트 점수: **0.77**
    - 사용한 특성 개수: **33**

---

## **선형 이진 분류**

### **로지스틱 회귀 (Logistic Regression)**

- 이진 분류에 사용되는 선형 모델입니다.

**코드 예시**:

```python
from sklearn.linear_model import LogisticRegression
logreg = LogisticRegression().fit(X_train, y_train)
print("테스트 세트 점수:", logreg.score(X_test, y_test))
```

- 결과 예시:
    - 테스트 세트 점수: **0.857**

### **규제 적용**:

- **C** 파라미터를 조정해 모델의 규제를 설정합니다.
    - **C=0.01**: 낮은 규제 → 복잡한 모델
    - **C=100**: 높은 규제 → 단순한 모델

**코드 예시**:

```python
logreg100 = LogisticRegression(C=100).fit(X_train, y_train)
print("테스트 세트 점수:", logreg100.score(X_test, y_test))
```

- 결과 예시:
    - 테스트 세트 점수: **0.965**
