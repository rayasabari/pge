<template>
  <section
    class="fixed top-0 left-0 right-0 z-50 w-full transition duration-300 bg-white shadow-sm bg-opacity-80 backdrop-blur-lg"
  >
    <Container>
      <div class="flex items-center justify-between w-full py-4 md:py-6">
        <div class="flex items-center justify-between w-full lg:w-auto">
          <!-- Brand Logo -->
          <NuxtLink
            exact
            to="/"
            exact-active-class="text-exact-active"
            class="flex items-center gap-3 font-semibold"
          >
            <img src="/pge-logo.webp" class="h-10" alt="Prodigy Green Energy Logo" />
            <div class="flex flex-col uppercase text-primary-800">
              <div class="text-lg leading-4 tracking-extra-wide">Prodigy</div>
              <div class="mt-1 text-sm font-medium leading-3">Green Energy</div>
            </div>
          </NuxtLink>

          <!-- Toggle Menu -->
          <div class="flex items-center lg:hidden">
            <button class="focus:outline-none focus:ring-0" type="button" @click="isOpen = !isOpen">
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

        <!-- Desktop Navigation -->
        <NavDesktop :menus="menus" />
      </div>
    </Container>

    <!-- Mobile Navigation -->
    <transition
      name="custom-classes-transition"
      enter-active-class="animate__animated animate__slideInUp animate__faster"
      leave-active-class="animate__animated animate__slideOutDown animate__faster"
    >
      <NavMobile v-if="isOpen" :menus="menus" />
    </transition>
  </section>
</template>

<script>
import listMenu from "../services/data/listMenu";
export default {
  name: "NavBar",
  data() {
    return {
      isOpen: false,
      brand: "Prodigy Green Energy",
      menus: listMenu,
    };
  },
  mounted() {
    this.$root.$on("hideMenu", () => {
      this.isOpen = false;
    });
  },
  methods: {},
};
</script>

<style>
</style>