<template>
  <div class="flex flex-col gap-6 mt-8 md:gap-6">
    <div
      v-for="item in news"
      :key="item.title"
      class="flex flex-col w-full gap-1 overflow-hidden transition-all duration-300 border border-gray-200 rounded-lg shadow md:flex-row group hover:shadow-lg"
    >
      <div
        class="w-full h-[200px] md:h-auto overflow-hidden bg-center bg-cover md:w-4/12"
        :style="`background-image: url(${item.thumbnail})`"
      ></div>
      <div class="flex flex-col justify-between w-full p-4 md:w-8/12">
        <div>
          <h2
            class="mb-2 text-xl font-semibold text-primary-500 group-hover:text-primary-600"
          >{{item.title}}</h2>
          <div class="text-sm">
            Published at:
            <span class="text-gray-400">{{item.published_at}}</span>
          </div>
        </div>
        <div>
          <div class="pt-4 pb-2">{{ item.excerpt }}</div>
          <div>
            <NuxtLink to="/" class="font-medium text-primary-500 hover:text-primary-600">Read More</NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardNews",
  props: ["news"],
};
</script>

<style>
</style>