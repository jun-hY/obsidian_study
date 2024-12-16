

## 부울 자료형
- **True / False**를 나타내는 자료형
- 주요 예제:
  ```python
  bool(-1)  # True
  bool(0)   # False
  bool('')  # False
  bool('hi')  # True
  ```

## 연산자
- **비교 연산자**:
  ```python
  x, y = 10, 20
  print(x > y)  # False
  print(x <= y)  # True
  ```
- **논리 연산자**:
  ```python
  x, y = True, False
  print(x and y)  # False
  print(x or y)   # True
  ```
- **멤버십 연산자**:
  ```python
  print(10 in [10, 20, 30])  # True
  print('a' not in 'apple')  # False
  ```

## 조건문
### if 문
- 기본 구조:
  ```python
  if 조건:
      실행할 코드
  ```
- 예제:
  ```python
  age = 18
  if age < 20:
      print('청소년 할인')
  ```

### if-else 문
- 기본 구조:
  ```python
  if 조건:
      실행할 코드
  else:
      다른 코드
  ```
- 예제:
  ```python
  num = -5
  if num < 0:
      print('음수입니다.')
  else:
      print('양수입니다.')
  ```

### if-elif-else 문
- 여러 조건을 처리할 때 사용
  ```python
  score = 85
  if score >= 90:
      grade = 'A'
  elif score >= 80:
      grade = 'B'
  else:
      grade = 'C'
  print(grade)
  ```

## 반복문
### while 문
- 조건이 참일 동안 코드 블록을 반복 실행
  ```python
  i = 0
  while i < 5:
      print(i)
      i += 1
  ```

### for 문
- 컬렉션의 요소를 하나씩 순회하며 실행
  ```python
  for i in range(5):
      print(i)
  ```

### break와 continue
- **break**: 반복문을 즉시 종료
- **continue**: 현재 반복을 건너뛰고 다음 반복으로 이동
  ```python
  for i in range(5):
      if i == 3:
          break
      print(i)

  for i in range(5):
      if i == 3:
          continue
      print(i)
  ```

