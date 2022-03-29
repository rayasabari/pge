<template>
  <div class="min-h-screen pb-6">
    <carousel :per-page="1" :mouse-drag="false" :autoplay="true">
      <slide v-for="image in images" :key="image.caption">
        <div class="w-full h-screen bg-center bg-cover" :style="`background-image: url(${image.src})`"></div>
      </slide>
    </carousel>
  </div>
</template>

<script>
import aosMixin from "../mixins/aos";

export default {
  name: "IndexPage",
  mixins: [aosMixin],
  data() {
    return {
      images: [
        {
          src: "https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1772&q=80",
          caption: "Slide 1",
        },
        {
          src: "https://images.unsplash.com/photo-1466611653911-95081537e5b7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80",
          caption: "Slide 2",
        },
        {
          src: "https://images.unsplash.com/photo-1467533003447-e295ff1b0435?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80",
          caption: "Slide 3",
        },
      ],
    };
  },
  methods: {},
};
</script>
