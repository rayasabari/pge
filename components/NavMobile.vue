<template>
  <nav class="absolute w-full h-screen py-2 bg-white border-t rounded-t-2xl top-96 md:hidden">
    <Container>
      <ul class="flex flex-col justify-between">
        <li v-for="menu in menus" :key="menu.name" @click="hideMenu">
          <NuxtLink
            :exact="menu.link == '/' ? true : false"
            active-class="text-primary-500"
            :to="menu.link"
            class="block py-1 text-lg text-gray-600 transition duration-300 hover:text-primary-500"
          >{{menu.name}}</NuxtLink>
        </li>
      </ul>
    </Container>
  </nav>
</template>

<script>
export default {
  name: "NavMobile",
  props: ["menus", "isOpen"],
  methods: {
    hideMenu() {
      this.$root.$emit("hideMenu");
    },
  },
};
</script>

<style>
</style>