<template>
  <section class="md:h-[125px] h-[90px] flex items-end">
    <Container>
      <ul class="flex items-center gap-1 text-xs text-gray-400 md:gap-2">
        <li class="group">
          <NuxtLink
            to="/"
            class="flex items-center gap-2 text-gray-600 duration-300 transiton-all group-hover:text-primary-500"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-4 h-4 text-gray-400 transition-all duration-300 group-hover:text-primary-500"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              stroke-width="2"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
              />
            </svg>
            <span>Home</span>
          </NuxtLink>
        </li>
        <template v-for="(menu, index) in menus" >
          <li :key="index+'icon'">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-5 h-5 text-gray-300"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                clip-rule="evenodd"
              />
            </svg>
          </li>
          <li :key="index+'menu'">
            <span v-if="menus.length - 1 === index">
              {{ucWords(menu)}}
            </span>
            <span v-else>
              <NuxtLink :to="'/'+menu" class="transition duration-300 hover:text-primary-500">{{ucWords(menu)}}</NuxtLink>
            </span>
          </li>
        </template>
      </ul>
    </Container>
  </section>
</template>

<script>
import "../assets/css/agile.css";

export default {
  name: "Breadcrumb",
  props: ["title"],
  watchQuery: true,
  data() {
    return {
      menus: [],
    };
  },
  watch: {
    "$route.query": "$fetch",
  },
  async fetch() {
    this.getBreadcrumb();
  },
  methods: {
    getBreadcrumb() {
      let path = this.$router.currentRoute.path.substring(1);
      this.menus = path.split("/");
    },
    ucWords(text) {
      text = text.toLowerCase().replace(/\b[a-z]/g, function (letter) {
        return letter.toUpperCase();
      });
      return text.replace(/-/g, " ").replace("And", "and");
    },
  },
};
</script>

<style>
</style>