# Nuxt Basic

## 1. Page Routing

- Vue.js에서 페이지 라우팅을 관리하는 것처럼 폴더 안에서 페이지들을 관리하는 것이 아니라 Nuxt에서는 페이지 라우팅 작업을 Pages 폴더에 생성하면 파일 이름 그대로 페이지가 완성된다. 이 부분은 .nuxt 폴더 안 router.js를 확인해보면 동적으로 관리되는 것을 살펴볼 수 있다.

## 2. Dynamic Routing

- 동적라우팅(Dynamic Routing)은 동일한 페이지를 여러 개 만드는 경우(예를 들어 사용자의 이름만 다른 중복된 페이지를 여러 개 만드는 경우) 사용자 마다 모든 페이지를 하나하나 만드는 것은 사실상 불가능하기 때문에 이런 경우 우리는 URL을 동적으로 생성해주어야 한다. 그렇기때문에 `동적 URL을 만들기 위해서는 이름 앞에 언더바 키워드(_)를 사용`한다.

## 3. AsyncData

- asyncData 메서드의 정의
  asyncData 메서드는 Page Components에서만 사용이 가능하며 비동기 처리에 의해 얻어진 데이터를 SSR(Server Side Rendering)하기 위해 사용되는 훅이다.
  첫 번째 Parameter로 context가 온다. asyncData는 컴포넌트에 데이터를 셋팅하는 것을 목적으로 사용된다.
  따라서 asyncData에 의해 반환된 값은 컴포넌트의 템플릿에서 접근이 가능하다.

- `npm install @nuxtjs/axios`
- nuxt.config.js 파일 안에 `modules: ['@nuxtjs/axios']`를 추가한다.
