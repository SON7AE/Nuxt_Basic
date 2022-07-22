<template>
  <div>
    <div class="bg-gray-100">
      <div class="container mx-auto mb-10 flex items-center space-x-4 h-10">
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/services">Services</NuxtLink>
        <NuxtLink to="/products">Products</NuxtLink>
      </div>
    </div>
    <div>
      <div class="container mx-auto">
        <Nuxt />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "",
};
</script>

<style></style>
