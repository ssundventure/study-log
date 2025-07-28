### 💡 익명함수

- 이름이 없는 함수

`function(){ console.log("hello");}`

- 예시 1. 변수에 담아서 쓴다.
`const sayHi = function() {console.log("hello");}`
변수 이름이 역할을 하니까 별도 함수 이름이 필요 없다.



- 예시 2. 콜백함수로 쓴다.
`setTimeout(function(){ console.log("3초 후 실행");},3000)` 
함수를 따로 선언해서 이름을 붙이면 더 길어지고 복잡해진다.
흐름상 이름 없이 전달하는 익명함수를 쓴다. 