<template>
  <div>
    <h1 class="text-lg font-bold">Services</h1>
    <NuxtLink to="/services/desenvolviment-de-sites">
      desenvolviment de sites
    </NuxtLink>
    <NuxtLink to="/services/marketing-digital"> marketing digital</NuxtLink>

    <div v-if="$fetchState.pending">Carregando ...</div>
    <div v-else>
      <div
        v-for="service in services"
        :key="service.id"
        class="border-b border-gray-400 py-4"
      >
        {{ service.username }}
      </div>
    </div>

    <br />

    <NuxtChild />
  </div>
</template>

<script>
export default {
  name: "",

  data() {
    return {
      services: [],
    };
  },

  // fetch 정의
  // 모든 컴포넌트에서 사용 가능하며, fetch는 비동기 처리에 의해 얻어진 데이터를 SSR을 하기 위해 사용되는 훅이다.
  // asyncData와 달리 this에 접근 가능하다. 대신 parameter는 넘기지 못한다는 점이 차이점이다. (v2.12이후 deprecated되었다.)
  // Deprecated 되었다는 소리는 어떤 기능이 아직까지 사용되고는 있지만, 신기능이 나왔기 때문에 조만간 사라지게 될 상태를 말한다.
  async fetch() {
    this.services = await this.$axios.$get(
      "https://jsonplaceholder.typicode.com/users?_limit=3"
    );
  },
};
</script>

<style></style>
