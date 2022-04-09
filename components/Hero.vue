<template>
  <div class="relative">
    <agile :options="options" class="h-screen">
      <div class="slide" v-for="(image,index) in images" :key="index">
        <div
          class="w-full h-screen bg-center bg-cover"
          :style="`background-image: url(${image.src})`"
        >
          <div class="flex items-center w-full h-screen backdrop-blur backdrop-brightness-75">
            <Container class="flex flex-col items-center justify-center w-full h-full md:w-1/2">
              <div
                data-aos="fade"
                :data-aos-duration="1000"
                :data-aos-delay="500"
                class="mb-2 text-3xl font-medium text-center text-white md:leading-tight md:text-5xl"
              >Lorem ipsum dolor sit amet consectetur</div>
              <div
                data-aos="fade"
                :data-aos-duration="1000"
                :data-aos-delay="1000"
                class="mb-2 text-center text-white md:mb-0 text-md md:text-xl text-opacity-60"
              >Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur iste animi amet tempora soluta dignissimos.!</div>
              <div data-aos="fade" :data-aos-duration="1000" :data-aos-delay="1500">
                <Button>Get Started</Button>
              </div>
            </Container>
          </div>
        </div>
      </div>
    </agile>
    <!-- <div
      class="absolute top-0 flex items-center w-full h-screen backdrop-blur backdrop-brightness-75"
    >
      <Container class="flex flex-col items-center justify-center w-full h-full md:w-1/2">
        <div
          data-aos="fade"
          :data-aos-duration="1000"
          :data-aos-delay="500"
          class="mb-2 text-3xl font-medium text-center text-white md:leading-tight md:text-5xl"
        >Lorem ipsum dolor sit amet consectetur</div>
        <div
          data-aos="fade"
          :data-aos-duration="1000"
          :data-aos-delay="1000"
          class="mb-2 text-center text-white md:mb-0 text-md md:text-xl text-opacity-60"
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur iste animi amet tempora soluta dignissimos.!</div>
        <div data-aos="fade" :data-aos-duration="1000" :data-aos-delay="1500">
          <Button>Get Started</Button>
        </div>
      </Container>
    </div> -->
  </div>
</template>

<script>
import aosMixins from "../mixins/aos";
import '../assets/css/agile.css';
export default {
  name: "Hero",
  props: ["images"],
  mixins: { aosMixins },
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
    };
  },
};
</script>
