<template>
  <div class="products">
    <product-list :products="data.products" />
  </div>
</template>
<script setup lang="ts">
const { data } = await useFetch("https://dummyjson.com/products");

useHead({
  title: "Products",
  meta: [{ name: "description", content: "all products" }],
});
</script>

<style lang="scss" scoped>
.products {
  padding: 1rem 2rem;
}
</style>
