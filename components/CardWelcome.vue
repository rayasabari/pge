<template>
  <div class="w-full p-5 bg-white rounded-xl">
    <SectionTitle>{{title}}</SectionTitle>
    <p class="mb-3 leading-relaxed">{{paragraph}}</p>
    <!-- <a
      :href="link"
      class="font-semibold transition duration-500 text-md text-primary-400 hover:text-primary-500"
    >Read More</a> -->
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