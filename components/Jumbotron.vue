<template>
  <div>
    <agile :options="options">
      <div class="slide" v-for="image in images" :key="image.caption">
        <div
          class="w-full h-screen bg-center bg-cover"
          :style="`background-image: url(${image.src})`"
        >
          <div
            class="flex flex-col items-center justify-center w-full h-full backdrop-blur backdrop-brightness-75"
          >
            <div
              class="text-2xl font-medium leading-loose text-center text-white md:mb-2 md:text-4xl"
            >{{image.caption}}</div>
            <div
              class="leading-loose text-center text-white md:text-lg text-md text-opacity-60"
            >Lorem ipsum dolor sit amet consectetur, adipisicing elit. Optio, reiciendis?</div>
          </div>
        </div>
      </div>
    </agile>
  </div>
</template>

<script>
export default {
  name: "Jumbotron",
  props: ["images"],
  data() {
    return {
      options: {
        autoplay: true,
        autoplaySpeed: 5000,
        pauseOnHover: false,
        fade: true,
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