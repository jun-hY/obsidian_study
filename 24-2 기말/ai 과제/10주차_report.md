## 판다스 개요
- **판다스(Pandas)** 는 데이터 조작과 분석을 위한 Python 라이브러리입니다.
- 주요 오브젝트: `Series`와 `DataFrame`.
- `import pandas as pd`로 사용.

## 주요 오브젝트
### Series
- 1차원 데이터 구조로, 배열과 유사.
  ```python
  sr = pd.Series([90, 80, 70], index=['Kim', 'Lee', 'Park'])
  print(sr)
  # 출력:
  # Kim     90
  # Lee     80
  # Park    70
  ```
- **인덱싱 및 슬라이싱**:
  ```python
  print(sr['Kim'])  # 90
  print(sr[:2])  # Kim, Lee의 데이터
  ```

### DataFrame
- 2차원 데이터 구조로, 엑셀과 유사한 테이블 형식.
  ```python
  df = pd.DataFrame({
      'Kor': [90, 85],
      'Eng': [80, 95],
      'Mat': [70, 65]
  }, index=['Kim', 'Lee'])
  print(df)
  # 출력:
  #      Kor  Eng  Mat
  # Kim   90   80   70
  # Lee   85   95   65
  ```
- **데이터 접근**:
  ```python
  print(df['Kor'])  # Kor 컬럼
  print(df.loc['Kim'])  # Kim 행
  ```

## 데이터 확인 및 조작
- **기본 정보 확인**:
  ```python
  print(df.head(3))  # 상위 3개 행
  print(df.describe())  # 기본 통계 정보
  ```
- **데이터 정렬**:
  ```python
  df.sort_values(by='Kor', ascending=False)
  ```

## 데이터 연산
- **기본 연산**:
  ```python
  print(df + 2)  # 모든 값에 2 더하기
  print(df * 2)  # 모든 값에 2 곱하기
  ```
- **행/열 연산**:
  ```python
  print(df.sum(axis=0))  # 열 방향 합
  print(df.mean(axis=1))  # 행 방향 평균
  ```

## 결측치 처리
- **결측 데이터 확인 및 처리**:
  ```python
  df.isnull()  # 결측 데이터 확인
  df.dropna(how='any')  # 결측 데이터 제거
  df.fillna(value=0)  # 결측 데이터를 0으로 대체
  ```

## 데이터 합치기 및 그룹화
- **데이터 합치기**:
  ```python
  df1 = pd.DataFrame({'name': ['Kim', 'Lee'], 'age': [20, 30]})
  df2 = pd.DataFrame({'name': ['Kim', 'Lee'], 'score': [90, 80]})
  result = pd.merge(df1, df2, on='name')
  ```
- **그룹화**:
  ```python
  grouped = df.groupby('Kor').sum()
  ```

## 데이터 필터링
- **조건 필터링**:
  ```python
  print(df[df['Kor'] > 80])  # Kor 점수가 80 이상인 행
  ```
