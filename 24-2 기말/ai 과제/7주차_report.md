# 함수와 클래스 요약

## 함수

### 함수의 정의와 구조
- 함수는 코드의 재사용성을 높이고 모듈화를 가능하게 함.
- 기본 구조:
  ```python
  def 함수이름(매개변수1, 매개변수2):
      수행할 문장
      return 반환값
  ```

### 인자 전달 방식
1. 기본 인자 전달: 위치 또는 키워드를 이용.
2. 기본값 설정:
   ```python
   def func(a, b=10):
       return a + b
   ```
3. 가변 인자 (`*args`):
   ```python
   def add_many(*args):
       return sum(args)
   ```
4. 키워드 가변 인자 (`**kwargs`):
   ```python
   def print_info(**kwargs):
       for key, value in kwargs.items():
           print(key, value)
   ```

### 반환문
- `return`을 사용해 값 반환:
  ```python
  def add(a, b):
      return a + b
  ```
- 여러 값 반환 가능:
  ```python
  def add_and_multiply(a, b):
      return a + b, a * b
  ```

### 전역 변수와 지역 변수
- `global` 키워드를 사용해 함수 내부에서 전역 변수 수정 가능:
  ```python
  def modify_global():
      global x
      x = 10
  ```

### 람다 함수
- 익명 함수:
  ```python
  add = lambda x, y: x + y
  ```

### 내장 함수
- 대표적인 함수들:
  - 수학 연산: `abs()`, `pow()`, `round()`
  - 형 변환: `int()`, `str()`, `list()`
  - 데이터 처리: `sorted()`, `zip()`

---

## 클래스

### 클래스의 개요
- 객체지향 프로그래밍(OOP)의 기본 단위로, 데이터와 메서드(함수)를 포함.
- 클래스 정의:
  ```python
  class 클래스이름:
      def __init__(self, 매개변수):
          self.속성 = 값
      def 메서드(self):
          수행할 문장
  ```

### 클래스 구성
1. 생성자 (`__init__`): 객체 초기화.
   ```python
   class Car:
       def __init__(self, speed):
           self.speed = speed
   ```
2. 메서드: 클래스 내부에 정의된 함수.
   ```python
   def speed_up(self, increment):
       self.speed += increment
   ```
3. 접근자와 설정자:
   - 속성 값 가져오기:
     ```python
     def get_speed(self):
         return self.speed
     ```
   - 속성 값 설정:
     ```python
     def set_speed(self, speed):
         self.speed = speed
     ```

### 상속
- 기존 클래스의 기능을 확장하는 데 사용:
  ```python
  class Truck(Car):
      def __init__(self, speed, load):
          super().__init__(speed)
          self.load = load
  ```
- 메서드 오버라이딩 가능.

### 클래스 변수
- 모든 객체가 공유하는 변수.
  ```python
  class Circle:
      PI = 3.14
      def __init__(self, radius):
          self.radius = radius
      def area(self):
          return Circle.PI * self.radius ** 2
  
```
