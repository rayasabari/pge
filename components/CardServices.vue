<template>
  <div class="flex flex-col gap-10">
    <div
      v-for="service in services"
      :key="service.name"
      class="flex flex-col w-full gap-4 transition-all duration-300 md:flex-row md:p-0 group"
    >
      <div class="items-center hidden w-full md:flex md:justify-center md:w-1/12">
        <img class="w-16 h-16" :src="service.svg" :alt="service.name" />
      </div>
      <div class="w-full md:w-11/12">
        <h3 class="flex items-center gap-2 mb-2 text-lg font-semibold text-primary-500">
          <img class="w-6 h-6 md:hidden" :src="service.svg" :alt="service.name" />
          {{service.name}}
        </h3>
        <div class="text-sm leading-relaxed">{{service.desc}}</div>
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