
## 모듈
- **정의**: 코드를 재사용할 수 있도록 함수와 클래스들을 모아 놓은 파일.
- **모듈 불러오기**:
  ```python
  import 모듈명  # 전체 모듈 불러오기
  from 모듈명 import 함수명  # 특정 함수만 불러오기
  import 모듈명 as 별칭  # 모듈에 별칭 부여
  ```
- **표준 라이브러리 사용 예시**:
  ```python
  import datetime
  today = datetime.date.today()
  print(today.year, today.month, today.day)  # 출력: 2023 10 24

  import random as rd
  print(rd.randint(1, 10))  # 1부터 10 사이의 정수
  ```

## 예외 처리
- **정의**: 실행 중 발생할 수 있는 오류를 처리하여 프로그램이 중단되지 않도록 함.
- **구문**:
  ```python
  try:
      오류 발생 가능 코드
  except 오류타입 as 변수:
      오류 처리 코드
  else:
      오류가 없을 때 실행되는 코드
  finally:
      항상 실행되는 코드
  ```
- **사용 예시**:
  ```python
  try:
      a, b = map(int, input('두 수를 입력하세요: ').split())
      result = a / b
      print(result)
  except ZeroDivisionError:
      print('0으로 나눌 수 없습니다.')
  except ValueError:
      print('숫자를 입력하세요.')
  finally:
      print('프로그램 종료.')
  ```

## 파일 처리
- **파일 열기 모드**:
  - `r`: 읽기 모드
  - `w`: 쓰기 모드 (기존 내용 삭제)
  - `a`: 추가 모드
- **파일 쓰기**:
  ```python
  with open('file.txt', 'w') as f:
      f.write('Hello, Python!\n')
  ```
- **파일 읽기**:
  ```python
  with open('file.txt', 'r') as f:
      lines = f.readlines()  # 모든 줄 읽기
      for line in lines:
          print(line.strip())
  ```
- **추가 쓰기**:
  ```python
  with open('file.txt', 'a') as f:
      f.write('추가 내용\n')
  ```
