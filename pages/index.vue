<template>
  <div class="min-h-screen">
    <Hero :images="images" />
    <section class="bg-gray-50 md:bg-white">
      <Container class="py-5 md:py-14">
        <div class="grid grid-cols-1 gap-4 md:grid-cols-2">
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
    <section class="bg-downloadable-section bg-conver">
      <div class="w-full h-full bg-gradient-to-r from-white to-transparent">
        <Container class="py-5 md:py-16">
          <div class="grid grid-cols-1 gap-4 md:grid-cols-2">
            <div data-aos="fade" class="p-5 bg-white bg-opacity-30 rounded-2xl backdrop-blur-lg">
              <SectionTitle>Downloadable Content</SectionTitle>
              <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Inventore aut fugit pariatur obcaecati sapiente perferendis repellat eligendi laborum, consectetur suscipit voluptas quo reprehenderit distinctio sit quos eius nostrum? Harum, expedita?</p>
            </div>
            <div data-aos="fade" class="flex justify-center">
              <iframe
                class="overflow-hidden rounded-2xl"
                width="560"
                height="315"
                src="https://www.youtube.com/embed/aYBGSfzaa4c"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
          </div>
        </Container>
      </div>
    </section>
    <section class="md:bg-white bg-gray-50">
      <Container class="py-5 lg:py-14">
        <div class="grid gap-5 lg:gap-8 lg:grid-cols-3">
          <div
            data-aos="fade"
            class="p-5 text-center bg-white shadow-lg rounded-xl lg:shadow-none lg:text-left"
          >
            <SectionTitle>Our Business</SectionTitle>
            <p>{{ ourBusiness.text }}</p>
          </div>
          <div class="grid grid-cols-1 gap-4 overflow-hidden lg:gap-8 lg:grid-cols-3 lg:col-span-2">
            <NuxtLink
              v-for="(item,index) in ourBusiness.type"
              :key="index"
              to="/"
              data-aos="fade-left"
              data-aos-duration="500"
              :data-aos-delay="600 + (index * 150)"
              class="relative overflow-hidden bg-white rounded-2xl group"
            >
              <div
                :style="`background-image: url(${item.image})`"
                class="w-full h-[550px] bg-center bg-cover flex flex-col justify-end group-hover:scale-110 transition duration-500"
              ></div>
              <div
                class="absolute inset-x-0 bottom-0 flex flex-col p-4 text-center transition duration-300 bg-gray-700 group-hover:bg-primary-600 bg-opacity-60 group-hover:bg-opacity-60 backdrop-blur lg:text-left"
              >
                <h3 class="mb-2 text-xl font-semibold text-white">{{item.name}}</h3>
                <p
                  class="text-white transition duration-300 text-opacity-70 group-hover:text-opacity-90"
                >{{item.desc}}</p>
              </div>
            </NuxtLink>
          </div>
        </div>
      </Container>
    </section>
    <section class="bg-gray-100">
      <Container class="py-12 md:py-20">
        <SectionTitle class="text-center">Latest News</SectionTitle>
        <div class="grid grid-cols-1 gap-4 mx-auto mt-5 mb-2 lg:mt-10 lg:gap-5 lg:grid-cols-4">
          <div
            v-for="(item,index) in latestNews"
            :key="index"
            data-aos="fade-up"
            data-aos-duration="500"
            :data-aos-delay="600 + (index * 150)"
            class="group"
          >
            <div
              class="w-full h-full overflow-hidden transition duration-300 shadow-md group-hover:shadow-xl group-hover:-translate-y-1 rounded-xl"
              :style="`background-image: url(${item.image}${index})`"
            >
              <div
                class="p-5 duration-300 bg-white transitino bg-opacity-90 group-hover:backdrop-blur"
              >
                <NuxtLink :to="item.link">
                  <div
                    class="text-lg h-[70px] transition duration-300 text-primary-500 group-hover:text-primary-600 font-medium border-b"
                  >{{ item.title }}</div>
                  <div
                    class="h-[120px] text-gray-700 transition duration-300 text-opacity-70 group-hover:text-opacity-100 py-4"
                  >{{item.body}}</div>
                  <div class="pt-4 text-gray-400">{{ item.date }}</div>
                </NuxtLink>
              </div>
            </div>
          </div>
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
      ourBusiness: {
        text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Cumque dolore nemo nulla non reprehenderit ullam nostrum repudiandae distinctio ea accusantium? Libero earum atque, dicta blanditiis repudiandae, hic nulla unde reiciendis ab ipsam inventore, ullam enim magnam quidem incidunt? Optio cupiditate, ea totam quasi et molestias soluta! Mollitia doloribus a magnam iusto quas! Quam incidunt dolor optio. Nemo magni molestiae neque iure praesentium reprehenderit dicta tenetur omnis animi, porro vitae ut, corrupti quidem itaque doloribus nisi.",
        type: [
          {
            name: "Power Plant",
            desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque, quisquam reiciendis labore illo dolorem commodi?",
            image:
              "https://www.tbsenergi.com/app/sam/assets/images/f07d3a35cdaccc8ccbff57dae5f22bb7.jpg?v=1632196062",
          },
          {
            name: "Minig Coal",
            desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque, quisquam reiciendis labore illo dolorem commodi?",
            image:
              "https://www.tbsenergi.com/app/sam/assets/images/0ecbec8935e06b14a5bba736f0344586.jpg?v=1632196422",
          },
          {
            name: "Plantatin PKU",
            desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque, quisquam reiciendis labore illo dolorem commodi?",
            image:
              "https://www.tbsenergi.com/app/sam/assets/images/a931aa9e1337d218818ff703bf7bf4b5.jpg?v=1623770296",
          },
        ],
      },
      latestNews: [
        {
          date: "10 Maret 2022",
          title: "Lorem ipsum dolor sit amet consectetur.",
          body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio impedit sunt ratione...",
          link: "/",
          image: "https://source.unsplash.com/random/200x200",
        },
        {
          date: "24 Maret 2022",
          title: "Lorem ipsum dolor sit amet consectetur.",
          body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio impedit sunt ratione...",
          link: "/",
          image: "https://source.unsplash.com/random/200x200",
        },
        {
          date: "29 Maret 2022",
          title: "Lorem ipsum dolor sit amet consectetur.",
          body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio impedit sunt ratione...",
          link: "/",
          image: "https://source.unsplash.com/random/200x200",
        },
        {
          date: "1 April 2022",
          title: "Lorem ipsum dolor sit amet consectetur.",
          body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio impedit sunt ratione...",
          link: "/",
          image: "https://source.unsplash.com/random/200x200",
        },
      ],
    };
  },
  mounted() {
    // this.fetchSomething();
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
