<template>
  <nav class="hidden lg:block">
    <ul class="flex justify-between w-full">
      <li class="pl-10 group" v-for="menu in menus" :key="menu.name">
        <NuxtLink
          :exact="menu.link == '/' ? true : false"
          active-class="text-link-active"
          :to="menu.link"
          class="py-4 font-medium text-gray-600 transition duration-300 md:py-6 text-md hover:text-primary-500"
        >{{menu.name}}</NuxtLink>
        <transition name="page">
          <div
            v-if="menu.sub"
            class="absolute hidden py-2 mt-2 text-sm transition-all duration-300 bg-white border border-gray-100 rounded-lg shadow-lg hover:block group-hover:block bg-opacity-90 font-base w-60 backdrop-blur"
          >
            <ul class="flex flex-col py-1">
              <li v-for="sub in menu.sub" :key="sub.link" class="block">
                <NuxtLink
                  :exact="sub.link == '/' ? true : false"
                  active-class="text-link-active"
                  :to="sub.link"
                  class="block px-5 py-2 font-medium text-gray-600 transition duration-300 text-md hover:bg-primary-500 hover:text-white"
                >{{sub.name}}</NuxtLink>
              </li>
            </ul>
          </div>
        </transition>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavDesktop",
  props: ["menus"],
  mounted() {
    // console.log(this.$router.currentRoute.path.split("/"));
  },
  methods: {},
};
</script>

<style>
</style>