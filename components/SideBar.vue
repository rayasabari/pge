<template>
  <div
    class="flex flex-col gap-8 md:sticky md:top-24"
    data-aos="fade-up"
    data-aos-delay="300"
    data-aos-duration="1000"
  >
    <nav class>
      <ul class="flex flex-col gap-1">
        <li
          v-for="menu in menus"
          :key="menu.name"
          class="overflow-hidden text-center text-gray-400 bg-gray-100 rounded-lg md:text-left"
        >
          <NuxtLink
            :to="menu.link"
            active-class="link-active-side"
            class="block px-4 py-2 font-medium transition-all duration-500 border-gray-300 text-md hover:bg-gray-50 hover:text-primary-500 hover:border-l-4 hover:border-primary-500"
          >{{menu.name}}</NuxtLink>
          <div v-if="menu.sub">
            <ul class="pb-2">
              <li v-for="sub in menu.sub" :key="sub.link" class="">
                <NuxtLink
                  :to="sub.link"
                  :event="!sub.sub ? 'click': ''"
                  active-class="sub-link-active-side"
                  class="block py-2 text-xs transition-all duration-500 border-gray-300 px-7 hover:bg-gray-50 hover:text-primary-500"
                >{{sub.name}}</NuxtLink>
              </li>
            </ul>
          </div>
        </li>
      </ul>
    </nav>
    <!-- <SideCta></SideCta> -->
  </div>
</template>

<script>
import listMenu from "../services/data/listMenu";
export default {
  name: "Sidebar",
  data() {
    return {
      menus: listMenu,
    };
  },
};
</script>

<style>
</style>