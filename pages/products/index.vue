<template>
  <div>
    <div class="container mx-auto">
      <h1 class="text-lg font-bold">Products</h1>
      <NuxtLink to="/products/product-a">Product A</NuxtLink>
      <NuxtLink to="/products/product-b">Product B</NuxtLink>

      <br />
      <br />

      <div
        v-for="product in products"
        :key="product.id"
        class="border-b border-gray-400 py-3"
      >
        {{ product.title }}
      </div>

      <p>이 문장은 Nuxt.js Version2를 활용한 Products Page입니다.</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "",

  data() {
    return {};
  },

  // asyncData 메서드의 정의
  // asyncData 메서드는 Page Components에서만 사용이 가능하며 비동기 처리에 의해 얻어진 데이터를 SSR(Server Side Rendering)하기 위해 사용되는 훅이다.
  // 첫 번째 Parameter로 context가 온다.
  // asyncData는 컴포넌트에 데이터를 셋팅하는 것을 목적으로 사용된다.
  // 따라서 asyncData에 의해 반환된 값은 컴포넌트의 템플릿에서 접근이 가능하다.
  async asyncData({ $axios }) {
    const products = await $axios.$get(
      "https://jsonplaceholder.typicode.com/posts?_limit=3"
    );

    return {
      products,
    };
  },

  methods: {},
};
</script>

<style></style>
