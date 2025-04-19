<template>
  <div class="home">
    <NuxtImg src="/images/banner.jpg" class="banner" />
  </div>
</template>

<script setup lang="ts">
useHead({
  title: "YenMarket",
  meta: [{ name: "description", content: "My YenMarket site." }],
});
</script>

<style lang="scss" scoped>
/*  */

.home {
  padding: 1rem 2rem;

  .banner {
    width: 100%;
    aspect-ratio: 3/2;
  }
}
</style>
