## 딕셔너리 자료형

### 생성
- Key-Value 형태로 데이터를 저장하는 자료형.
- 예시:
  ```python
  person = {'name': '홍길동', 'age': 26, 'weight': 82}
  students = {2019001: '이순신', 2019002: '김유신', 2019003: '강감찬'}
  ```

### 조회
- 특정 키 값으로 데이터 접근 가능:
  ```python
  person['name']  # '홍길동'
  ```
- 키, 값, 또는 키-값 쌍을 조회:
  ```python
  person.keys()      # dict_keys(['name', 'age', 'weight'])
  person.values()    # dict_values(['홍길동', 26, 82])
  person.items()     # dict_items([('name', '홍길동'), ('age', 26), ('weight', 82)])
  ```

### 추가 및 수정
- 새로운 항목 추가: `person['job'] = '학생'`
- 기존 항목 수정: `person['age'] = 27`

### 삭제
- 특정 키 삭제: `del person['age']`
- 전체 삭제: `person.clear()`

### 연산
- 키 존재 여부 확인:
  ```python
  'name' in person  # True
  'hobby' not in person  # True
  ```
- 딕셔너리 길이: `len(person)`

---

## 집합 자료형

### 생성
- 중복을 허용하지 않으며, 순서가 없는 데이터 저장.
- 예시:
  ```python
  set1 = {10, 20, 30, 40}
  days_set = set(['Mon', 'Tue', 'Wed', 'Thu'])
  ```

### 추가 및 삭제
- 원소 추가:
  ```python
  s.add(500)  # 단일 원소 추가
  s.update([600, 700])  # 여러 원소 추가
  ```
- 원소 삭제:
  ```python
  s.remove(100)  # 삭제할 원소가 없으면 오류 발생
  s.discard(100)  # 삭제할 원소가 없어도 정상 실행
  s.clear()  # 모든 원소 삭제
  ```

### 집합 연산
- 합집합:
  ```python
  s1 | s2  # 또는 s1.union(s2)
  ```
- 교집합:
  ```python
  s1 & s2  # 또는 s1.intersection(s2)
  ```
- 차집합:
  ```python
  s1 - s2  # 또는 s1.difference(s2)
  ```
- 대칭 차집합:
  ```python
  s1 ^ s2  # 또는 s1.symmetric_difference(s2)
  ```
- 부분집합/상위집합 여부 확인:
  ```python
  s2.issubset(s1)
  s1.issuperset(s2)
  ```
- 서로소 여부 확인:
  ```python
  s1.isdisjoint(s2)
  ```

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

