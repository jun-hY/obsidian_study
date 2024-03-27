##### 정수타입

| Length | Signed | Unsigned |
| ------ | ------ | -------- |
| 8-bit  | i8     | u8       |
| 16-bit | i16    | u16      |
| 32-bit | i32    | u32      |
| 64-bit | i64    | u64      |
| arch   | isize  | usize    |

##### 정수 리터럴

| Number literals     | Example               |
| ------------------- | --------------------- |
| Decimal             | ```98_222 = 98,222``` |
| Hex                 | ```0xff```            |
| Octal               | ```0o77```            |
| Binary              | ```0b111_0000```      |
| Byte(```u8``` only) | ```b'A'```            |

##### 부동 소주점 타입

기본 부동 소주점 타입은 ```f32, f64```가 있다. 기본타입은 ```f64```
```rust
fn main() {
	let x = 2.0; // f64
	let y: f32 = 3.0 // f32
}
```

##### 연산 기호
```rust
fn main() {
	// addition
	let sum = 5 + 10;
	
	// subtraction
	let difference = 95.5 - 4.3;
	
	// multiplication
	let product = 4 * 30;
	
	// division
	let quotient = 56.7 / 32.2;
	
	// remainder
	let remainder = 43 % 5;
}
```

##### Boolean 타입
```true, false```의 값을 갖는 타입.
```rust
fn main() {
	let t = true;
	let f:bool = false; //with explicit type annotation
}
```

##### 문자 타입
Rust의 ```char``` 타입은 Unicode Scalar를 표현한다. ( C는 ASCII다. )
```rust
fn main() {
	let c = 'z';
	let z = 'ℤ';
	let heart_eyed_cat = '😻';
}
```


## 복합타입

##### 튜플(tuple)
다양한 타입의 숫자를 집합시켜 하나의 복합 타입으로 만드는 일반적인 방법
```rust
fn main() {
	let tup: (i32, f64, u8) = (500, 6.4, 1);
}
```

```rust
fn main() {
	let tup = (500, 6.4, 1);
	let (x, y, z) = tup;
	println!("The value of y is: {}", y);
}
```
위와 같은 방법으로 튜플에 각 변수를 매칭시켜 튜플을 해체할 수 있다.
( 구조해체 )

```rust
fn main() { 
	let x: (i32, f64, u8) = (500, 6.4, 1);
	let five_hundred = x.0; // 튜플이름.index
	let six_point_four = x.1;
	let one = x.2;
}
```

##### 배열(Array)
