<template>
  <div class="flex flex-col gap-6 py-5">
    <div
      v-for="(step, index) in steps"
      :key="index"
      class="leading-relaxed"
      data-aos="fade-left"
      data-aos-duration="500"
      :data-aos-delay="600 + (index * 150)"
    >
      <div class="mb-1">
        <span class="font-medium text-primary-500">Step {{step.no}}:</span>
        <span class="text-gray-500">{{step.title}}</span>
      </div>
      <p class="leading-relaxed">{{step.text}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardSteps",
  props: ["steps"],
};
</script>

<style>
</style>