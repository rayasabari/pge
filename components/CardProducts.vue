<template>
  <div class="flex flex-col w-full gap-6 md:gap-4 md:flex-row">
    <div
      v-for="product in products"
      :key="product.name"
      class="flex-col overflow-hidden transition-all duration-300 bg-white rounded-lg shadow group hover:shadow-lg"
    >
      <div class="w-full h-[300px] overflow-hidden">
        <img :src="product.image" :alt="product.name" />
      </div>
      <div class="p-4 h-[130px]">
        <h3 class="mb-4 text-xl font-semibold text-primary-500">{{ product.name }}</h3>
        <div class="text-sm">{{ product.desc }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProduct",
  props: ["products"],
};
</script>

<style>
</style>