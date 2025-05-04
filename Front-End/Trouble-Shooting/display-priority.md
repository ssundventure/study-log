### 💡 display:flex|hidden 우선순위

- 문제사항
  `.hidden{display: none}` 으로 정의한 class 가 상위 요소의 style display:flex 에 우선순위가 밀려 동작하지않음.

#### ✅ 해결방법

1. **!important** 추가하여 우선순위 강제로 높인다.
2. 상위 요소에 적용된 display 속성을 설정된 조건에따라 동적으로 변경하는 방식을 쓴다.
3. `visibility: hidden;` 을 사용한다. 단, 요소가 공간을 차지해 layout에 영향을 줄 수 있으므로 상황에 맞게 사용한다.