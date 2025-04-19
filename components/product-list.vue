<template>
  <div class="product-list">
    <div
      v-for="product in props.products"
      :key="product.id"
      class="product-item"
    >
      <NuxtImg :src="product.images[0]" loading="lazy" />

      <div class="content">
        <div class="price">{{ product.price }}$</div>
        <h3>{{ product.title }}</h3>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  products: {
    type: Array,
    default: () => [],
  },
});
</script>

<style lang="scss" scoped>
.product-list {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  column-gap: 2rem;
  row-gap: 2rem;

  @media screen and (max-width: 992px) {
    grid-template-columns: 1fr 1fr 1fr;
  }
}

.product-item {
  max-width: 30rem;
  width: 100%;
  height: max-content;
  border: 0.1px solid #333;
  border-radius: 0.5rem;

  img {
    width: 100%;
    height: 100%;
    aspect-ratio: 3/2;
  }
  .content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 1rem;
    padding: 1rem;

    .price {
      font-size: 1.6rem;
      font-weight: bold;
    }
  }
}
</style>
