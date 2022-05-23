<template>
  <div class="min-h-screen">
    <Hero :images="images" />
    <section class="bg-gray-50 md:bg-white">
      <Container class="py-5 md:py-14">
        <div class="grid grid-cols-1 gap-4 md:grid-cols-2">
          <CardWelcome
            data-aos="fade"
            data-aos-delay="300"
            data-aos-duration="1000"
            title="Welcome"
            :paragraph="welcome"
            link="/"
          ></CardWelcome>
          <CardWelcome
            data-aos="fade"
            data-aos-delay="300"
            data-aos-duration="1000"
            title="Business Overview"
            :paragraph="businessOverview"
            link="/"
          ></CardWelcome>
        </div>
      </Container>
    </section>
    <section data-aos="fade-up" data-aos-duration="800" class="bg-downloadable-section bg-conver">
      <div class="w-full h-full md:bg-gradient-to-r md:from-white md:to-transparent">
        <Container class="py-5 md:py-16">
          <div class="grid grid-cols-1 gap-4 md:grid-cols-2">
            <div
              data-aos="fade"
              data-aos-delay="300"
              data-aos-duration="1000"
              class="p-5 bg-white bg-opacity-30 rounded-2xl backdrop-blur-lg"
            >
              <SectionTitle>Downloadable Content</SectionTitle>
              <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Inventore aut fugit pariatur obcaecati sapiente perferendis repellat eligendi laborum, consectetur suscipit voluptas quo reprehenderit distinctio sit quos eius nostrum? Harum, expedita?</p>
            </div>
            <div
              data-aos="fade"
              data-aos-delay="300"
              data-aos-duration="1000"
              class="flex justify-center"
            >
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

    <!-- Latest News -->
    <!-- <section class="bg-gray-100">
      <Container class="py-12 md:py-20">
        <SectionTitle class="text-center">Latest News</SectionTitle>
        <div class="grid grid-cols-1 gap-4 mx-auto mt-5 mb-2 lg:mt-10 lg:gap-5 lg:grid-cols-4">
          <div
            v-for="(item,index) in latestNews"
            :key="index"
            data-aos="fade-up"
            data-aos-duration="500"
            :data-aos-delay="300 + (index * 150)"
            class="group"
          >
            <div
              class="w-full h-full overflow-hidden transition duration-300 shadow-md group-hover:shadow-xl group-hover:-translate-y-1 rounded-xl"
              :style="`background-image: url(${item.image})`"
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
    </section> -->
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
      welcome:
        "Switching to Prodigy Energy would eliminate air pollution annually, while first slowing and then reversing the effects of global warming and stabilizing the global energy sector.",
      businessOverview: `We're proud to say all our energy is generated in renewable and sustainable ways.
Renewables were the only energy source for which demand increased in 2020 despite the pandemic, while consumption of all other fuels declined. Rapid technology improvements and decreasing costs of renewable energy`,
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
      ourBusiness: {
        text: "Prodigy Green Energy is facilitating the Energy Transition, as an independent renewable energy company. We are developing and operating first-class renewable energy. Our strategic focus is to facilitate the Renewable Energy Transition: we are developing the infrastructure needed for our customers to move towards ever more sustainable and low carbon energy use. Our development efforts are focused on establishing expandable platforms located at key crossroads of energy flows. We will continue to expand our network to facilitate our customers’ renewable energy development.",
        type: [
          {
            name: "Power Plant",
            desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque, quisquam reiciendis labore illo dolorem commodi?",
            image:
              "https://www.tbsenergi.com/app/sam/assets/images/f07d3a35cdaccc8ccbff57dae5f22bb7.jpg?v=1632196062",
          },
          {
            name: "Mining Coal",
            desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Neque, quisquam reiciendis labore illo dolorem commodi?",
            image:
              "https://www.tbsenergi.com/app/sam/assets/images/0ecbec8935e06b14a5bba736f0344586.jpg?v=1632196422",
          },
          {
            name: "Plantation PKU",
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
