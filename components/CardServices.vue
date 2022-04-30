<template>
  <div class="flex flex-col gap-4 md:gap-10">
    <div
      v-for="service in services"
      :key="service.name"
      class="flex flex-col w-full gap-4 p-4 transition-all duration-300 md:flex-row md:p-0 group hover:scale-105"
    >
      <div class="flex items-center justify-center w-full md:w-1/12">
        <img class="w-16 h-16" :src="service.svg" :alt="service.name" />
      </div>
      <div class="w-full md:w-11/12">
        <h3
          class="mb-2 text-lg font-semibold text-center md:text-left text-primary-500"
        >{{service.name}}</h3>
        <div class="text-sm text-center md:text-left">{{service.desc}}</div>
      </div>
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