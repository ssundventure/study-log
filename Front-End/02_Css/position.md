### 💡 position 속성정리
1. static

- 기본 값. 문서의 흐름을 따라 배치되며 top, left 등의 위치속성을 적용할 수 없다.

2. relative(자기 자신을 기준)

- 자신의 원래 위치를 기준으로 이동. 자리(space)는 그대로 유지됨.

3. absolute (부모를 기준)

- 부모 요소중 position: relative|absolute|fixed 요소를 기준으로 배치된다.
- 만약 부모요소가 static이라면 body를 기준으로 위치가 결정된다.
- **원래의 자리에서 완전히 분리됨**
- absolute의 너비는 0. 안보이면 지정해주기

4. fixed

- 브라우저 창(viewport)을 기준으로 위치가 고정된다.
- 스크롤해도 위치가 고정된다.

5. sticky

- 스크롤하다가 특청 위치에 도달되면 고정된다.
- 원래 relative처럼 작동하다가 특정위치에 도달하면 fixed처럼 작동한다.