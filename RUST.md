
Rust는 빠르고 C, C++과 같이 저수준 제어를 도와주는 옵션들을 가지고 있다. 

main.rs
```rust
fn main() {
	println!("Hello, world!");
}
```

### Cargo
러스트의 빌드 시스템 및 패키지 매니저.

rustc를 이용하여 빌드할 수 있지만, 관용적인 부분과 프로젝트 사이즈가 커짐에 따라 필요성이 들어나기 때문에 함께 사용한다.

cmd
```
cargo new <your_project_name> <option, normaly --bin>
cd <your_project_name>
```

### 변수
Rust의 변수는 기본적으로 불변이다. 가변이 가능한 변수로 만들기 위해서 변수 선언 뒤 옵션을 붙인다.

```Rust
let i = 1; // 불변 변수
let mut a = 1; // 가변 변수
```

#### 상수
Rust는 모든 변수를 상수처럼 불변하는 특성을 가지고 있지만 라이프 사이클을 포함하고 있다. 일정 주기를 지나면 변수의 메모리가 해제된다는 말이다.
상수는 프로그램이 실행되는 시간동안 항상 유효하고 표현식만 설정될 수 있다.
함수 호출의 결과값이나 그 외 실행시간이 결정되는 값을 설정할 수 없다.

```Rust
const MAX_POINT: u32 = 100_000;
```
Rust의 상수 명명 규칙에 따라 모든 단어는 대문자로 작성한다.

% C의 define과 유사한 것 같네요.

#### shadowing
let으로 변수를 새로 설정할 때 이전 데이터를 숨길 수 있다. 

```Rust
let a = 10;
let a = a + 5; // 15
let a = a * 2; // 30
```

불변이지만 let과 함께 작성하면 변경이 가능하다.
이전 데이터와 관련된 다른 타입의 변수를 선언할 때 사용할 수 있다.
mut 은 같은 타입만 가능하다.

### 주석
주석은 // 를 이용한다.

```Rust
// 주석
```

### [[Rust_Datatype]]

### 함수(Function)

rust에서 함수는 뱀형태(Snake Case)로 작명한다.

```rust
fn main() {
	println!("Hello, World!");

	another_function();
}

fn another_function() {
	println!("Another function");
}
```

```rust
// 함수 매개변수 전달법
fn main() {
	another_function(5);
}

fn another_function(x: i32) { // 변수이름: 타입
	println!("the value is {}", x);
}
```

##### 표현식

구문과 다르게 결과값을 산출함(return)
	구문 : 어떤 명령의 나열

```rust
fn main() {
	let x = 5; // 구문

	let y = {
		let x = 3;
		x + 1 // 결과값 return
	}; // 표현식

	println!("the value of y is: {}", y); // 4출력
}
```

##### 함수의 반환값

```rust
fn five() -> i32 { // -> 리턴 값의 타입
	5 // rust는 리턴값을 ;(세미콜론)으로 마무리하지 않음
}

fn main() {
	let x = five();

	println!("the value of x is: {}", x); // 5 출력
}
```