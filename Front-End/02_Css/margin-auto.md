### 💡 가운데 정렬 margin:auto

margin: auto는 부모 요소보다 작을 때 남는 공간을 자동으로 균등하게 분배해서 가운데 정렬되도록 한다.

#### ✅ 동작조건

1. 정렬하려는 방향의 크기(width 또는 height)가 명시되어 있어야한다.

   - 가로 가운데 정렬 -> width
   - 세로 가운데 정렬 -> height (실제로 flex, grid 사용)

2. 부모 요소가 display: block 이어야한다.

   - 또는 flex/grid도 가능하다.
