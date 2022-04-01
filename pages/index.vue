<template>
  <div class="min-h-screen pb-8">
    <Hero :images="images" />
    <section>
      <Container class="py-5">
        <div class="flex flex-col w-full space-y-8 md:space-y-0 md:flex-row md:space-x-12">
          <CardWelcome
            data-aos="fade"
            :data-aos-duration="1000"
            title="Welcome"
            paragraph="Lorem ipsum dolor sit amet consectetur adipisicing elit. Unde est sint et. Dolore unde delectus doloremque laborum! Maiores eos laboriosam perferendis blanditiis mollitia voluptate quam itaque minus deserunt, incidunt delectus nostrum, facilis quidem possimus minima sequi voluptatum libero voluptatem ipsum eius, in modi distinctio! Ea omnis suscipit illo in repudiandae."
            link="/"
          ></CardWelcome>
          <CardWelcome
            data-aos="fade"
            :data-aos-duration="1000"
            title="Business Overview"
            paragraph="Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quibusdam velit aut, ipsum ullam sunt nesciunt praesentium impedit vero accusantium laboriosam commodi illum adipisci odio perspiciatis dolor ex minus iure amet reprehenderit laborum porro veniam cum neque. Voluptatem fugit repellendus error voluptates deleniti, esse minus quaerat."
            link="/"
          ></CardWelcome>
        </div>
      </Container>
    </section>
  </div>
</template>

<script>
import Hero from "../components/Hero.vue";

export default {
  components: { Hero },
  name: "IndexPage",
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
