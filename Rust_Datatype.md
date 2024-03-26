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
