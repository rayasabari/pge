<template>
  <nav class="absolute w-full h-screen py-2 bg-white border-t rounded-t-2xl top-96 md:hidden">
    <Container>
      <ul class="flex flex-col justify-between">
        <li v-for="menu in menus" :key="menu.name" @click="hideMenu">
          <NuxtLink
            :exact="menu.link == '/' ? true : false"
            active-class="text-link-active"
            :event="!menu.sub ? 'click':''"
            :to="menu.link"
            class="block py-3 font-medium text-gray-500 transition duration-300 border-b text-md hover:text-primary-500"
          >{{menu.name}}</NuxtLink>
          <div v-if="menu.sub">
            <ul>
              <li v-for="sub in menu.sub" :key="sub.link">
                <NuxtLink
                  active-class="text-link-active"
                  :to="sub.link"
                  class="block py-3 pl-3 font-light text-gray-500 transition duration-300 border-b text-md hover:text-primary-500"
                >{{sub.name}}</NuxtLink>
              </li>
            </ul>
          </div>
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