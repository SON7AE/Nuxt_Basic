<template>
  <!-- <div>
    <h1 class="text-lg font-bold">Main</h1>
    <p>이 문장은 Nuxt.js Version2를 활용한 Main Page 코드입니다.</p>
  </div> -->

  <div>
    <pre>
      {{ $store.state.user }}
    </pre>

    <pre>
      {{ user }}
    </pre>
  </div>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "IndexPage",

  computed: {
    ...mapState({
      user: (state) => state.user,
    }),
  },
};
</script>
