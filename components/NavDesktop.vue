<template>
  <nav class="hidden lg:block">
    <ul class="flex justify-between w-full">
      <li class="pl-10 " v-for="menu in menus" :key="menu.name">
        <NuxtLink
          :exact="menu.link == '/' ? true : false"
          active-class="text-link-active"
          :to="menu.link"
          class="font-medium text-gray-600 transition duration-300 text-md hover:text-primary-500"
        >{{menu.name}}</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavDesktop",
  props: ["menus"],
};
</script>

<style>
</style>