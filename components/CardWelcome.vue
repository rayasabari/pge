<template>
  <div class="w-full text-center p-7 rounded-xl md:w-1/2 md:text-left">
    <h2 class="mb-1 text-2xl font-semibold md:mb-3 text-primary-700">{{ title }}</h2>
    <p class="py-4 text-lg">{{paragraph}}</p>
    <a
      :href="link"
      class="text-lg font-semibold transition duration-500 text-primary-400 hover:text-primary-500"
    >Read More</a>
  </div>
</template>

<script>
export default {
  name: "CardWelcom",
  props: ["title", "paragraph", "link"],
};
</script>

<style>
</style>