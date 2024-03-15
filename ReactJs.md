
### create-react-app(CRA) 설치법

1. nodeJs 설치(재부팅)
2. cmd에서 밑의 명령 실행
```
cd 원하는 경로 이동
npx create-react-app 프로젝트폴더명
cd 프로젝트 폴더 이동
npm run start(or npm start)
```

### CRA 구조

src -> 소스코드 경로
css -> module별로 작성
btn.js에 css를 적용 시킬때 btn.module.css를 작성해 btn.js에 import

분할 정의 구조

### Component
React는 Component를 작성하여 UI의 재사용을 쉽게 한다.
간단히 사용자 함수형태로 정의된 html코드 뭉치라 보면 되겠다.

Btn.js
```
function Btn() {
	return <button></button>
}

export defalut Btn;
```
App.js
```
import Btn from "./Btn.js"

function App() {
	return (
		<div>
			<Btn />
		</div>
	)
}
```

##### Props
Component를 호출할 때  props와 같이 호출할 수 있다.
Props는 Component의 속성을 나타내는 데이터이다.
위 예제에서는 Props를 활용하여 버튼별 클릭 이벤트 리스너를 다르게 하거나 하는 동작을 수행할 수 있다.

btn.js
```
function Btn(props) {
	return <button
		onClick={prop.onClick}
	></button>
}

export defalut Btn;
```
App.js
```
import Btn from "./Btn"

function App() {
	const onClick= () => {
		console.log("clicked");
	}
	return (
		<div>
			<Btn onClick={onClick} />
		</div>
	)
}
```
사용할 때 HTML태그와 비슷하다고 하여 Component에 props.onClick 에 대한 기능을 작성하지 않고 event listener로 사용하면 안된다. 위 onClick은 event Listener가 아닌 props로 동작하기 때문이다. 물론 btn.js에서의 onClick은 정상적인 event Listener로 동작한다.
### render
React는 Dom에 root를 만들어 직접 render 한다.

index.js
```
import App from "./App"

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
	<App />
);
```

### State
기본적으로 상수이며 setState를 사용하여 값을 변경할 수 있다.
State는 State의 데이터가 변경되었을 때 DOM을 Rerender한다.

App.js
```
import { useState } from "react"

function App() {
	// State
	cosnt [ counter, setCounter ] = useState(0);

	const onClick= () => {
		setCounter((prev) => prev + 1)
	};
	return (
		<div>
			<h2>{counter}</h2>
			<button onClick={onClick}>click<button/>
		</div>
	)
}
```

### Effect

Effect는 기본적으로 Component가 생성될 때 동작하는 function이다.
이외의 상황에 다른 object의 변화를 trigger로 하여 동작할 수 있다.
###### how to import Effect
```
import { useEffect } from "react"
```

##### how to use 'useEffect'
```
useEffect(function, [trigger1, trigger2, ...]);
```

ex)
```
const [location, setLocation] = useState(true);

const imHere = () => {
	console.log("Im here");
};

useEffect(imHere, [location]);
```
or 
```
useEffect(() => {
	console.log("Im here");
}, [location]);
```

##### Cleanup Function
Component가 제거될 때 Effect의 동작을 원하면 사용하는 function이다.

How to use Cleanup Function
```
function Hello() {
	useEffect(() => {
		console.log("i Created");
		return () => console.log("i destroyed");
	}, []);
	return <h1>Hello!</h1>
}
```
or
```
function Hello() {
	useEffect(function() {
		console.log("i Created");
		return function() { 
			console.log("i destroyed");
		}
	}, []);
	return <h1>Hello!</h1>
}
```
or
```
function Hello() {
	function ByFn() {
		console.log("i destroyed");
	}
	function HiFn() {
		console.log("i Created");
		return ByFn;
	}
	useEffect(HiFn, []);
	return <h1>Hello!</h1>
}
```
위 3가지의 타입으로 작성할 수 있다. 본인이 원하는 코드 스타일에 맞게 작성하도록 하자.


### JS의 API 요청

fetch로 요청
```
fetch(`address to get api`)
	.then((response) => reponse.json())
	.then((json) => setVariabel(json.)) // ex)json.data.movies etc...
```

Async로 요청
```
const getApi = async () => {
	const responce = await fetch(`address to get api`);
	const json = await response.json();
	setVariable(json...); // ex)json.data.movies etc...
}
```

### Route
Route는 ReactJs의 대표적인 기능 중 하나로 새로고침없이 화면을 전환할 수 있는 기능이다.

cmd
```
npm i react-router-dom
```

App.js
```
import {
	BrowserRouter as Router,
	Switch,
	Route
} from "react-router-dom";
import Home from "./routes/Home";

function App() {
	return (
		<Router>
			<Switch>
				// "/"는 파라매터가 없는 기본 URL상태를 뜻한다.
				<Route path="/">
					<Home />
				</Route>
			</Switch>
		</Router>
	)
}
```
./routes/Home.js
```
function Home() {
	return <div></div>
}

export default Home;
```

#### Link
Route 기능 중 하나로 <a href=""></a> 태그와는 다르게 Route 특징 그대로 새로고침 없이 페이지를 로드한다.

./routes/Home.js
```
function Home() {
	return <Link to="/detail">read Detail</Link>
}

export default Home;
```
./routes/Detail.js
```
function Detail() {
	return <div></div>
}

export default Detail;
```

