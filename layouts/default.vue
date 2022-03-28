<template>
  <div>
    <NavBar></NavBar>
    <Container class="min-h-screen py-6 mt-12 md:mt-14">
      <Nuxt></Nuxt>
    </Container>
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
      class: "font-poppins text-gray-500",
    },
  },
};
</script>
