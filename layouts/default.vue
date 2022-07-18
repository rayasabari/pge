<template>
  <div>
    <NavBar></NavBar>
    <Nuxt></Nuxt>
    <Footer></Footer>
  </div>
</template>

<script>
import { Loading } from "notiflix/build/notiflix-loading-aio";

export default {
  name: "DefaultLayout",
  head: {
    htmlAttrs: {
      class: "scroll-smooth",
    },
    bodyAttrs: {
      class: "font-poppins text-gray-500",
    },
  },
  mounted() {
    Loading.arrows({ backgroundColor: "#fff" });
    setTimeout(() => {
      Loading.remove();
    }, 700);

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
