<template>
  <div>
    <h1 class="text-lg font-bold">About</h1>
    <p>이 문장은 Nuxt.js Version2를 활용한 예제 코드입니다.</p>
  </div>
</template>

<script>
export default {
  name: "",
  // middleware의 정의
  // middleware는 레이아웃, 페이지가 렌더링 되기 전에 실행되는 파일이 정의되는 폴더이다.
  // middleware는 클라이언트 뿐만 아니라 서버에서도 쓰이는 개념이므로 개념 자체를 알아두면 도움이 된다.
  middleware: "auth",
};
</script>

<style></style>
