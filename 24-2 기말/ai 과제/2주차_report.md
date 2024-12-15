### **변수 관련 요약**
#### **변수 개념**
- **정의**: 데이터를 저장하는 공간.
- **예제**:
```python
num = 20 print(num)  # 출력: 20
num = 30 print(num)  # 출력: 30
```
    

#### **변수 할당**

- 단일 할당:
```python
num = 200 
num = num + 100 
print(num)  # 출력: 300
```
    
- 다중 할당:
```python
num1 = num2 = num3 = 200
print(num1, num2, num3)  # 출력: 200 200 200
```
    
- 동시 할당:
```python
num4, num5 = 300, 400
print(num4, num5)  # 출력: 300 400
```
    

#### **변수 식별자**

- 규칙:
    - 알파벳, 숫자, 밑줄(_) 사용 가능.
    - 숫자로 시작 불가.
    - 예약어 사용 불가 (`sum`, `if` 등).
    
- **주의점**:
```python
sum = 100  # 내장 함수명과 동일
lst = [10, 20, 30] 
total = sum(lst)  # 오류 발생
```

#### **동적 타이핑**

- 변수의 데이터 타입은 할당된 값에 따라 동적으로 변경.
```python
foo = 100 
print(type(foo))  # 출력: <class 'int'> 
foo = "Hello" 
print(type(foo))  # 출력: <class 'str'>`
```

#### **변수 활용**

- 원의 면적과 둘레 계산:
```python
radius = 4.0
print('원의 반지름:', radius)
print('원의 면적:', 3.14 * radius * radius)  # 50.24
print('원의 둘레:', 2 * 3.14 * radius)  # 25.12
```

#### **화면 입출력과 변수**

- **입력**:
```python
name = input('이름을 입력하세요: ')
print('이름:', name)
age = int(input('나이를 입력하세요: '))
print('10년 후 나이:', age + 10)
```

- **출력**:
```python
print('나의 이름은:', '홍길동')
print('나이는:', 27)
```