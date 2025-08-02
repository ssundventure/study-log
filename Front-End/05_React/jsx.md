### 💡 JSX

- JSX(JavaScript XML)의 개념
  JavaScript안에서 XML/HTML 처럼 생긴 코드를 사용할 수 있게 만든 JavaScript에 추가된 문법이다.


- JSX의 실제 동작 방식
1. JSX
`const element = <h1>Hello, world!</h1>`

2. JS
`const element = React.createElement("h1",null,"Hello, world!")`

JSX가 자바스크립트가 이해할 수 있게 **React 요소를 만드는 함수 호출 코드**로 변경된다.
