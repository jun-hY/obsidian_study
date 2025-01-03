### 파이썬 개요

파이썬은 1989년 반 로썸(Guido Van Rossum)에 의해 개발된 인터프리터 언어이며 공동 작업과 유지보수가 매우 쉬운 편이다.

대화식 실행모드와 스크립트 실행모드가 있다.

##### 변수
변할 수 있는 수라는 의미이며 프로그래밍에서는 데이터가 저장된 메모리의 위치를 가리킨다. 사용자가 지정한 이름을 통해 접근할 수 있으며 자유롭게 읽기, 쓰기, 수정하기가 가능하다.

```python
num = 20
res = num + 10

print(res)
```

##### 식별자
사용자가 정의하는 변수나 함수에 대해 서로 구별되는 이름을 부여한다.
하나의 이름이 여러 개의 메모리 위치를 지칭하면 구분이 쉽지 않음으로 다른 메모리 위치에는 다른 이름을 부여하여야 한다.

##### 자료형
python의 자료형은 bool, number, string, list, tuple, set, dictionary 등이 있다.

##### 연산자
덧셈, 뺄셈, 곱셈, 나눗셈과 같은 산술 연산자, 대입하는 할당연산자, 비교연산자 등이 있다.

##### **학습 내용**
- **기본 변수와 연산**:
```python 
num = 20 res = num + 10 print(res)  # 출력: 30
```
    
- **조건문**:
```python
if 배고픔:
	print("밥을 먹는다.")
```
    
- **반복문**:
```python
while 집에 가는 중:
	print("왼발을 내딛는다.")
	print("오른발을 내딛는다.")
```
    
- **함수**:
```python
def 라면끓이기(라면, 물, 대기시간):
	print(f"{라면}을 {물}ml로 {대기시간}분 동안 끓인다.")

라면끓이기("삼양라면", 500, 4)
```
    
- **클래스**:
```python
class 자동차:
	def __init__(self):
		self.속도 = 0
	def 속도올리기(self, 증가속도):
		self.속도 += 증가속도
	def 현재속도(self):
		return self.속도
```