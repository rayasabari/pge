<template>
  <div class="grid grid-cols-1 gap-4 overflow-hidden lg:gap-4 lg:grid-cols-3 lg:col-span-2">
    <div
      v-for="(item,index) in expertise"
      :key="index"
      data-aos="fade-left"
      data-aos-duration="500"
      :data-aos-delay="600 + (index * 150)"
      class="relative overflow-hidden bg-white rounded-2xl group"
    >
      <div
        :style="`background-image: url(${item.image})`"
        class="w-full h-[350px] bg-center bg-cover flex flex-col justify-end group-hover:scale-110 transition duration-500 overflow-hidden"
      ></div>
      <div
        class="absolute inset-x-0 top-0 flex h-[150px] transition-all duration-300 group-hover:h-full flex-col p-4 text-center bg-gradient-to-b from-gray-600  bg-opacity-60 group-hover:bg-opacity-60  lg:text-left"
      >
        <h3 class="mb-2 text-xl font-medium text-white">{{item.text}}</h3>
        <p
          class="hidden text-white transition duration-300 group-hover:flex text-opacity-70 group-hover:text-opacity-90"
        >{{item.desc}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardExpertise",
  props: ["expertise"],
};
</script>

<style>
</style>