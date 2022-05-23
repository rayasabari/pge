<template>
  <div class="grid gap-4 py-5 md:grid-cols-2 lg:grid-cols-3">
    <div
      v-for="(project, index) in projects"
      :key="index"
      data-aos="fade-left"
      data-aos-duration="500"
      :data-aos-delay="600 + (index * 150)"
      class="overflow-hidden transition-all duration-500 shadow-md rounded-xl hover:-translate-y-1 hover:shadow-lg group"
    >
      <img
        :src="project.image"
        class="h-[300px] w-full object-cover group-hover:scale-105 transition-all duration-500 object-center"
        :alt="project.title"
      />
      <div class="p-5">
        <div class="mb-2 text-lg font-semibold text-primary-400">{{ project.title }}</div>
        <div class="text-sm leading-relaxed">{{project.desc}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProjects",
  props: ["projects"],
};
</script>

<style>
</style>