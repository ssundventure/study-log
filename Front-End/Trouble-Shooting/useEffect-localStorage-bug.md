## 💡 useEffect의 실행시점과, 새로고침 시 localStorage 초기화되는 문제

### 🧠 문제사항
React 앱에서 `useEffect` 를 이용해 `localStorage`에 데이터를 저장하고 불러오려 했지만,
 **새로고침 시 저장된 값이 초기화(`[]`) 되는 문제**가 발생한다.

### ⚠️ 증상
- 새로운 데이터를 추가하면 localStorae에 값을 잘 저장된다.
- 그러나 새로고침하면 값이 `[]` 로 초기화되어 데이터가 사라진다.
- 개발자도구 Application 탭에서도 사라진다. 


### 🔍 원인 분석
- entries 를 빈 배열로 초기화한다.
- `useEffect(() => setEntreis(...))` 보다 `useEffect(()=> localStorage.setItem(...))` 이 먼저 실행된다.
- 그 결과 빈 배열이 localStorage에 저장되어 기존 데이터가 덮어쓰기된다.

```tsx
const [entries, setEntries] = useState<DiaryEntry[]>([]); // ← 기본값이 []

useEffect(() => {
  const saved = localStorage.getItem("diary-entries");
  if (saved) {
    setEntries(JSON.parse(saved));
  }
}, []);

useEffect(() => {
  localStorage.setItem("diary-entries", JSON.stringify(entries));
}, [entries]);
```


#### ✅ 해결 방법

```tsx
 const [entries, setEntries] = useState<DiaryEntry[]>(() => {
    const saved = localStorage.getItem("diary-entries");
    return saved ? JSON.parse(saved) : [];
  });
```
- useState 초기값을 함수로 설정하여 localStorage에서 값을 먼저 불러오도록 수정한다.
- 이제 컴포넌트 마운트 시점에 localStorage에서 값을 먼저 불러오므로, 
  빈 배열이 덮어쓰이는 문제 없이 안전하게 초기값 설정이 가능하다.