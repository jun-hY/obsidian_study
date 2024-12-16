# 넘파이 요약

## 넘파이 개요
- **넘파이(Numpy)**는 대규모 다차원 배열과 행렬 연산을 지원하는 Python 라이브러리
- 과학적 계산 및 데이터 분석에 주로 사용된다

## ndarray (N-dimensional Array)

- **ndarray 생성**:
  ```python
  import numpy as np
  a = np.array([1, 2, 3])
  print(a)  # 출력: array([1, 2, 3])
```

- **ndarray 속성**:
  - `shape`: 배열의 형태 (행, 열 등)
  - `ndim`: 배열의 차원
  - `dtype`: 배열 원소의 데이터 타입
  - `size`: 배열의 원소 수
  - `itemsize`: 각 원소의 메모리 크기(byte)

## 주요 함수

- **배열 생성**:
  ```python
  np.zeros((2, 3))  # 0으로 채워진 배열 생성
  np.ones((2, 3))   # 1로 채워진 배열 생성
  np.full((2, 3), 100)  # 특정 값으로 채워진 배열 생성
  np.eye(3)  # 단위 행렬 생성
  ```
  
- **랜덤 데이터 생성**:
  ```python
  np.random.rand(3, 3)  # 0~1 사이의 난수 배열 생성
  np.random.randint(0, 10, size=5)  # 0~10 사이의 정수 난수 생성
  ```

## 배열 연산

- **기본 연산**:
  ```python
  a = np.array([1, 2, 3])
  b = np.array([4, 5, 6])
  print(a + b)  # 배열의 덧셈: [5, 7, 9]
  print(a * b)  # 배열의 곱셈: [4, 10, 18]
  ```
  
- **브로드캐스팅**:

  - 배열과 스칼라(숫자)의 연산이 가능.
  ```python
  print(a + 10)  # [11, 12, 13]
  ```
  
  - **행렬 곱**:
  ```python
  a = np.array([[1, 2], [3, 4]])
  b = np.array([[10, 20], [30, 40]])
  print(np.matmul(a, b))  # 행렬 곱
  ```

## 인덱싱과 슬라이싱

- **1차원 배열**:
  ```python
  a = np.array([10, 20, 30, 40])
  print(a[1:3])  # [20, 30]
  ```
  
- **다차원 배열**:
  ```python
  a = np.array([[1, 2], [3, 4], [5, 6]])
  print(a[0, 1])  # 1행 2열 원소
  print(a[:, 0])  # 모든 행의 1열 원소
  ```

## 배열 변형

- **배열 재구성**:
  ```python
  a = np.arange(6).reshape(2, 3)
  print(a)
  ```
  
- **배열 평탄화**:
  ```python
  a.flatten()  # 다차원 배열을 1차원으로 변환
  ```

## 축(axis) 연산

- **축 방향 지정**:
  ```python
  a = np.array([[1, 2], [3, 4]])
  print(a.sum(axis=0))  # 열 방향 합
  print(a.sum(axis=1))  # 행 방향 합
  ```

