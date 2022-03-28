<template>
  <div class="py-3 bg-white shadow-md">
    <div class="container mx-auto">
      <div class="flex justify-between">
        <div class="font-semibold text-lg">Brand</div>
        <nav class="flex justify-between">
          <ul class="px-3" v-for="menu in menus" :key="menu.name">
            <li>{{menu.name}}</li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      menus: [
        {
          name: "Home",
          link: "/",
        },
        {
          name: "About Us",
          link: "/about-us",
        },
        {
          name: "Product & Services",
          link: "/product-and-services",
        },
        {
          name: "News",
          link: "/news",
        },
        {
          name: "Contact Us",
          link: "/contact-us",
        },
      ],
    };
  },
};
</script>

<style>
</style>