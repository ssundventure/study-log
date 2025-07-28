### 💡 리액트 시작하기

1. create-react-app

`npx create-react-app my-app --template typescript`
`cd my-app`
`npm start`

- npx
  - npm 패키지들과 라이브러리들을 실행하는 도구 (다운 x)
- npm
  - node 패키지들이라 라이브러리들을 다운받는다.

2. vite 로 시작하는 방식
`npm create vite@latest my-app -- --template react`
`cd my-app`
`npm install`
`npm run dev`



다시 정리하면 ,

🔹 CRA는...

오래된 방식의 “정석 루트”
설정 없이 React를 빠르게 시작할 수 있지만,
느리고 무겁고, 커스터마이징이 어렵다.

🔹 Vite는…

새롭고 빠른 빌드 도구
개발 환경에서 훨씬 빠르며, 설정도 유연하고 가볍다.
최근엔 React, Vue, Svelte 등 많은 프레임워크가 Vite 기반으로 전환 중이다.

