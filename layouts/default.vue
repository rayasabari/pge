<template>
  <div>
    <NavBar></NavBar>
    <Nuxt></Nuxt>
    <Footer></Footer>
  </div>
</template>

<script>
// import aosMixins from "../mixins/aos";
export default {
  name: "DefaultLayout",
  // mixins: [aosMixins],
  head: {
    htmlAttrs: {
      class: "scroll-smooth",
    },
    bodyAttrs: {
      class: "font-poppins text-gray-500",
    },
  },
  mounted() {
    this.setViewHeight();
    window.addEventListener("resize", () => {
      this.setViewHeight();
    });
  },
  methods: {
    setViewHeight: function () {
      const vh = window.innerHeight * 0.01;
      document.documentElement.style.setProperty("--vh", `${vh}px`);
    },
  },
};
</script>
