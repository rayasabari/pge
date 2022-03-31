<template>
  <div class="min-h-screen pb-6">
    <Jumbotron :images="images" />
    <Container class="py-5">
      <div data-aos="fade">Main Page</div>
    </Container>
  </div>
</template>

<script>
import Jumbotron from "../components/Jumbotron.vue";
import aosMixin from "../mixins/aos";

export default {
  components: { Jumbotron },
  name: "IndexPage",
  mixins: [aosMixin],
  data() {
    return {
      test: [],
      images: [
        {
          src: "https://images.unsplash.com/photo-1451187580459-43490279c0fa?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1772&q=80",
          caption: " Lorem ipsum dolor sit amet.",
        },
        {
          src: "https://images.unsplash.com/photo-1466611653911-95081537e5b7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80",
          caption: " Lorem ipsum dolor sit amet.",
        },
        {
          src: "https://images.unsplash.com/photo-1467533003447-e295ff1b0435?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80",
          caption: " Lorem ipsum dolor sit amet.",
        },
      ],
    };
  },
  mounted() {
    this.fetchSomething();
  },
  methods: {
    async fetchSomething() {
      const res = await this.$axios.$get(
        "https://jsonplaceholder.typicode.com/users"
      );
      this.test = res;
    },
  },
};
</script>
