
Rust는 빠르고 C, C++과 같이 저수준 제어를 도와주는 옵션들을 가지고 있다. 

main.rs
```
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
Rust의 변수는 기본적으로 상수이다. 가변이 가능한 변수로 만들기 위해서 변수 선언 뒤 옵션을 붙인다.

```
let i = 1; // 상수
let mut a = 1; // 가변 변수
```

### 주석
주석은 // 를 이용한다.

```
// 주석
```

