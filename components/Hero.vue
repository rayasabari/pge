<template>
  <section>
    <agile :options="options">
      <div class="slide" v-for="(image,index) in images" :key="index">
        <div
          class="w-full h-screen bg-center bg-cover"
          :style="`background-image: url(${image.src})`"
        >
          <div class="w-full h-full backdrop-blur backdrop-brightness-75">
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
  </section>
</template>

<script>
import aosMixins from "../mixins/aos";
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

<style>
.agile__nav-button {
  background: transparent;
  border: none;
  color: #fff;
  cursor: pointer;
  font-size: 24px;
  height: 100%;
  position: absolute;
  top: 0;
  transition-duration: 0.3s;
  width: 80px;
}
.agile__nav-button:hover {
  /* background-color: rgba(0, 0, 0, 0.5); */
  opacity: 1;
}
.agile__nav-button--prev {
  left: 0;
}
.agile__nav-button--next {
  right: 0;
}
.agile__dots {
  bottom: 50px;
  left: 50%;
  position: absolute;
  transform: translateX(-50%);
}
.agile__dot {
  margin: 0 10px;
}
.agile__dot button {
  background-color: transparent;
  border: 1px solid #fff;
  border-radius: 50%;
  cursor: pointer;
  display: block;
  height: 10px;
  font-size: 0;
  line-height: 0;
  margin: 0;
  padding: 0;
  transition-duration: 0.3s;
  width: 10px;
}
.agile__dot--current button,
.agile__dot:hover button {
  background-color: #fff;
}

.slide {
  display: block;
  /* height: 500px; */
  -o-object-fit: cover;
  object-fit: cover;
  width: 100%;
}
</style>