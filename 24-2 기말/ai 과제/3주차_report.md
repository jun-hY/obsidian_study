## 문자열 기본 개념
- **정의**: 문자열은 문자들의 나열이며, 작은따옴표(`'`) 또는 큰따옴표(`"`)로 감쌉니다.
- **예시**:
  ```python
  text = "Hello, Python!"
  multiline = """여러 줄로 구성된
  문자열입니다."""
  ```

## 문자열 연산
- **문자열 연결**: `+` 연산자를 사용하여 문자열을 연결할 수 있습니다.
  ```python
  head = "Python"
  tail = " is fun!"
  print(head + tail)  # 출력: Python is fun!
  ```
- **문자열 반복**: `*` 연산자를 사용하여 문자열을 반복합니다.
  ```python
  print("Python" * 2)  # 출력: PythonPython
  ```

## 문자열 인덱싱과 슬라이싱
- **인덱싱**: 문자열의 특정 위치에 접근할 수 있습니다.
  ```python
  text = "Python"
  print(text[0])   # 출력: P
  print(text[-1])  # 출력: n
  ```
- **슬라이싱**: 부분 문자열을 추출할 수 있습니다.
  ```python
  print(text[0:3])  # 출력: Pyt
  print(text[::-1]) # 출력: nohtyP
  ```

## 문자열 포매팅
- **기본 포매팅**:
  ```python
  name = "Alice"
  age = 25
  print("%s은 %d살입니다." % (name, age))  # 출력: Alice은 25살입니다.
  ```
- **`format` 메서드**:
  ```python
  print("{}은 {}살입니다.".format("Alice", 25))
  ```
- **f-문자열 (Python 3.6 이상)**:
  ```python
  print(f"{name}은 {age}살입니다.")
  ```

## 문자열 메서드
- 문자열 조작을 위한 다양한 메서드:
  - `text.upper()`, `text.lower()`
  - `text.strip()`, `text.rstrip()`, `text.lstrip()`
  - `text.replace("old", "new")`
  - `text.split(delimiter)`
- **예시**:
  ```python
  text = "  Hello, Python!  "
  print(text.strip())  # 출력: Hello, Python!
  ```

## 연습 문제
1. **문자열 반복**:
   ```python
   repeat = "Hi "
   print(repeat * 6)  # 출력: Hi Hi Hi Hi Hi Hi
   ```
2. **문자열 포매팅**:
   ```python
   name = "홍길동"
   age = 30
   print(f"{name}의 나이는 {age}살입니다.")
   ```
3. **문자열 분리와 결합**:
   ```python
   alphabet = "a:b:c:d"
   print(alphabet.split(":"))  # 출력: ['a', 'b', 'c', 'd']
   ```
