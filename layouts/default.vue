<template>
  <div>
    <NavBar></NavBar>
    <Nuxt></Nuxt>
    <Footer></Footer>
  </div>
</template>

<script>
export default {
  name: "DefaultLayout",
  head: {
    htmlAttrs: {
      class: "scroll-smooth",
    },
    bodyAttrs: {
      class: "font-poppins text-gray-400",
    },
  },
  data() {
    return {
      loading: true,
    };
  },
  mounted() {
    // Loading.dots({
    //   backgroundColor: "#fff",
    //   svgColor: "#14b8a6",
    // });
    // setTimeout(() => {
    //   this.loading = false;
    //   Loading.remove();
    // }, 700);
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
