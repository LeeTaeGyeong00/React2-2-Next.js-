# 202230229 이태경

# 0828

# 1장

## Pages Router vs. App Router

- react로 개발하다 처음 Next를 사용하면 제일먼저 놀라는 기능이 Router 입니다.
- 교재의 코드는 Next.js 13.1을 사용하고 있기 때문에 Pages Router로 작성되어 있습니다.

### [Pages Router]

- pages 디렉토리가 root이고, index.js가 index page가 됩니다.
- about.js /about, team.js는 /team의 경로로 라우팅 됩니다.
- 클라이언트 중심의 라우팅입니다.

### [App Router]

- app 디렉토리가 root이고, page.js가 index page가 됩니다.
- /about/page.js는 /about, /login/page.js는 /page의 경로로 라우팅 됩니다.
- 서버 중심의 라우팅입니다.
- 번들 사이즈가 작습니다.

## Next.js 13 vs 14

- Pages Router -> App Router
- Data Fetching : 13까지는 getServerSideProps, getStaticProps 메소드를 이용해서 구현 했으나, 14에서는 SSG(정적 사이트 생성), SSR(서버측 렌더링) 및 ISR(증분적 정적 재생성)에서 하나의 API만을 사용해서 구현할 수 있게 되었습니다.

- Turbopack : Rust 기반으로 개발된 새로운 번들러 사용으로 webPack보다 100배 빠르다고 발표 했습니다
- 이미지 최적화 : 13까지는 도구를 사용하였으나, 14부터는 자체적으로 지원하기 시작했습니다.
- 보안강화 : XSS 공격에 대한 보호 기능이 강화 되고, 보안 관련 헤더 설정을 더욱 쉽게 만들었습니다.

# 01 Next.js 알아보기

## Next.js 알아보기

- Next.js는 리액트를 위해 만든 오픈소스 자바스크립트 웹 프레임 워크입니다.
- 리액트에는 없는 다양한 기능을 제공합니다
- - 서버사이드 렌더링 (SSR : Server Side Rendering)
- - 정적 사이트 생성 (SSG : Static Site Generation)
- - 증분 정적 재생성 (ISR : Incremental Static Regeneration)

### [Next.js가 제공하는 새로운 기능들]

- 코드 분할
- 파일 기반 라우팅
- 경로 기반 프리페칭
- 서버사이트 렌더링
- 정적 사이트 생성
- 증분 정적 콘텐츠 생성
- 타입 스크립트 기본 지원
- 자동 폴리필

## Next.js와 비슷한 프레임 워크

### [Gatsby]

- 정적 웹사이트를 만들수 있는 프레임 워크입니다
- 정적 사이트 생성만 지원합니다.
- 클라이언트 사이드 렌더링만 지원합니다.
- 동적으로 변하는 복잡한 웹사이트는 만들 수 없습니다.

### [Razzle]

- 서버 사이드 랜더링이 가능한 자바스크립트 애플리케이션 개발이 가능합니다.
- CRA와 유사하게 프로젝트를 구성 할 수 있다는 장점이 있습니다(create-razzle-app)
- React, Preact, Reason-React, Angular및 Vue와 함께 사용할 수 있습니다

### [Nuxt.js]

- Vue.js를 사용한 웹 애플리케이션 개발에서 리액트의 Next.js에 해당하는 프레임워크입니다.
- Nuxt.js나 Next.js 모두 같은 목표를 갖는 프레임워크지만 Nuxt.js는 더 많은 설정이 필요합니다.
- 만약 Vue 개발자가 서버사이트 렌더링이 필요하다면 Nuxt.js를 사용해보는것 추천

### [Angular Universal]

- 정적 사이트 생성과 서버사이드 랜더링을 지원합니다.
- Nuxt나 Next와는 달리 대기업인 구글에서 만듦

## 리액트에서 Next.js로

- Next.js의 기본 철학은 React와 거의 같습니다.
- "설정보다 관습" 이라는 리액트의 철학을 계승합니다.
- Next.js는 fetch, window, document와 같은 웹 브라우저에서 제공하는 전역 객체나 canvas 같은 HTML 요소에서는 접근 할 수가 없습니다.

## Next.js 시작하기

- 개발환경에는 Node.js와 npm만 설치 하면 됩니다.
- Node.js만 설치하면 npm은 함께 설치됩니다.
- 설치되어있는지 확인 하려면 버전을 확인해봅니다.
- 예제는 버전에 크게 영향을 받지 않을 것으로 판단됩니다.
- 만일 다른 버전을 이미 사용하고 있다면 그대로 사용해도 됩니다.
- 사용중 의존성에 문제가 있다고 판단될때 변경하면 됩니다.
