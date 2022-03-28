<template>
  <header class="fixed top-0 left-0 right-0 w-full py-3 transition duration-300 bg-white shadow-md">
    <Container>
      <div class="flex items-center justify-between w-full">
        <div class="z-50 flex items-center justify-between w-full md:w-auto">
          <!-- Brand Logo -->
          <NuxtLink event to="/" class="text-lg font-semibold text-gray-400">{{brand}}</NuxtLink>

          <!-- Toggle Menu -->
          <div class="static md:hidden">
            <button type="button" @click="isOpen = !isOpen">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-6 h-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  v-if="isOpen"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M6 18L18 6M6 6l12 12"
                />
                <path
                  v-else
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M4 6h16M4 12h16m-7 6h7"
                />
              </svg>
            </button>
          </div>
        </div>

        <!-- Navigation -->
        <nav class="hidden md:block">
          <ul class="flex justify-between w-full">
            <li class="px-3" v-for="menu in menus" :key="menu.name">
              <NuxtLink
                :exact="menu.name == 'Home' ? true : false"
                :to="menu.link"
                class="text-sm font-medium text-gray-400 transition duration-300 hover:text-gray-600"
              >{{menu.name}}</NuxtLink>
            </li>
          </ul>
        </nav>
      </div>
    </Container>

    <!-- Mobile Navigation -->
    <nav v-if="isOpen" class="absolute w-full bg-white md:hidden">
      <Container>
        <ul class="flex flex-col justify-between pt-4">
          <li class="py-2" v-for="menu in menus" :key="menu.name" @click="isOpen = false">
            <NuxtLink
              :to="menu.link"
              class="text-xl font-medium text-gray-400 transition duration-300 hover:text-gray-600"
            >{{menu.name}}</NuxtLink>
          </li>
        </ul>
      </Container>
    </nav>
  </header>
</template>

<script>
export default {
  name: "NavBar",
  data() {
    return {
      isOpen: false,
      brand: "Prodigy Green Energy",
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
          name: "Products & Services",
          link: "/products-and-services",
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
  methods: {
    isActiveClass(link) {},
  },
};
</script>

<style>
a.nuxt-link-active {
  color: rgb(156 163 175 / var(--tw-text-opacity));
}
/* exact link will show the primary color for only the exact matching link */
a.nuxt-link-exact-active {
  color: rgb(14 165 233 / var(--tw-text-opacity));
}
</style>