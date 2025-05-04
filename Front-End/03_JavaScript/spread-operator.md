1. Spread Operator로 사용될 때

- 배열이나 객체를 **펼칠 때**

```
// 배열 펼치기
const arr1 = [1, 2, 3];
const arr2 = [...arr1, 4, 5]; // [1, 2, 3, 4, 5]

// 객체 펼치기
const obj1 = { name: "John" };
const obj2 = { ...obj1, age: 30 }; // { name: "John", age: 30 }
```

2. Rest Parameter로 사용될 떄

- 여러 값을 하나의 배열로 **모을 때**

```
// 함수 매개변수로 사용
function introduce(name, ...hobbies) {
    console.log(`제 이름은 ${name}입니다.`);
    console.log(`취미는 ${hobbies.join(', ')}입니다.`);
}

introduce('John', '축구', '게임');

// 배열 구조분해할당에서 사용
const [first, second, ...rest] = [1, 2, 3, 4, 5];
console.log(rest); // [3, 4, 5]
```
