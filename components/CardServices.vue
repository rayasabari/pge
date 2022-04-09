<template>
  <div class="flex flex-col gap-4 md:gap-10 md:flex-row">
    <div
      v-for="service in services"
      :key="service.name"
      class="p-4 transition-all duration-300 md:p-0 group hover:scale-105"
    >
      <div class="flex justify-center mb-3 md:justify-start">
        <img class="w-16 h-16" :src="service.svg" :alt="service.name" />
      </div>
      <h3 class="mb-4 text-xl font-semibold text-center md:text-left text-primary-500">{{service.name}}</h3>
      <div class="text-sm text-center md:text-left">{{service.desc}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardServices",
  props: ["services"],
};
</script>

<style>
</style>