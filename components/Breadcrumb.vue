<template>
  <section class="min-h-screen realtive">
    <agile :options="options">
      <div class="slide" v-for="(image,index) in images" :key="index">
        <div class="w-full bg-center bg-cover" :style="`background-image: url(${image.src})`">
          <div class="flex items-center w-full h-screen backdrop-blur backdrop-brightness-75">
            <Container class="flex flex-col items-center justify-center w-full h-full md:w-1/2">
              <div
                class="mb-1 text-3xl text-center text-white md:leading-tight md:text-5xl"
              >{{title}}</div>
              <a href="#page-content" class="flex items-center gap-2 text-white">
                <span>Scroll Down</span>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="w-6 h-6"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    d="M17 13l-5 5m0 0l-5-5m5 5V6"
                  />
                </svg>
              </a>
            </Container> </div>
        </div>
      </div>
    </agile>
  </section>
</template>

<script>
import "../assets/css/agile.css";

export default {
  props: ["title"],
  data() {
    return {
      options: {
        autoplay: true,
        autoplaySpeed: 5000,
        pauseOnHover: false,
        fade: true,
        dots: false,
        speed: 2000,
        navButtons: false,
        pauseOnHover: false,
        pauseOnDotsHover: true,
      },
      images: [
        {
          src: "https://www.tbsenergi.com/app/sam/assets/images/e511286a99df2c7466aeae8fcca5851b.jpg?v=1623770296",
          caption: " Lorem ipsum dolor sit amet.",
        },
        {
          src: "https://www.tbsenergi.com/app/sam/assets/images/5c2c816d4d55b68e65e26359f1e3a940.png?v=1632725589",
          caption: " Lorem ipsum dolor sit amet.",
        },
        {
          src: "https://www.tbsenergi.com/app/sam/assets/images/8ba7c0967969ab511686523693854cf8.jpg?v=1623770297",
          caption: " Lorem ipsum dolor sit amet.",
        },
      ],
    };
  },
};
</script>

<style>
</style>