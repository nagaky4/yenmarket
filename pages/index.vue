<template>
  <div class="home">
    <img class="banner" src="~/assets/images/banner.jpg" alt="logo" />
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
