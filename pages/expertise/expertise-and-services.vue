<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Our Expertise'"></Breadcrumb>
    <div id="page-content" class="pt-10 md:pt-0">
      <PageContainer>
        <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
          <SectionTitle class="text-center md:text-left">Our Expertise</SectionTitle>
          <div
            class="mb-8 text-center md:text-left"
          >To meet the renewable energy requirement in Indonesia, Prodigy Green Energy continually innovate to produce sustainable renewable energy, such as:</div>
          <CardExpertise :expertise="expertise" />
          <!-- <CardProducts :products="products" /> -->
        </section>
        <section class="mt-12" data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
          <SectionTitle class="text-center md:text-left">Our Services</SectionTitle>
          <div
            class="mb-8 text-center md:text-left"
          >Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere!</div>
          <CardServices :services="services" />
        </section>
      </PageContainer>
    </div>
  </div>
</template>

<script>
export default {
  name: "OurExpertise",
  data() {
    return {
      expertise: [
        {
          text: "Solar energy from the sun",
          desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere",
          image: require("../../assets/images/expertise/solar.webp"),
        },
        {
          text: "Geothermal energy from heat inside the earth",
          desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere",
          image: require("../../assets/images/expertise/geothermal.webp"),
        },
        {
          text: "Wind energy",
          desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere",
          image: require("../../assets/images/expertise/wind.webp"),
        },
        {
          text: "Biomass from plant",
          desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere",
          image: require("../../assets/images/expertise/biomass.webp"),
        },
        {
          text: "Hydropower from flowing water",
          desc: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere",
          image: require("../../assets/images/expertise/hydropower.webp"),
        },
      ],
      products: [
        {
          name: "Product One",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis accusamus veniam hic.",
          image: "https://preview.cruip.com/tidy/images/features-home-3-01.jpg",
        },
        {
          name: "Product Two",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis accusamus veniam hic.",
          image: "https://preview.cruip.com/tidy/images/features-home-3-02.jpg",
        },
        {
          name: "Product Three",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis accusamus veniam hic.",
          image: "https://preview.cruip.com/tidy/images/features-home-3-03.jpg",
        },
      ],
      services: [
        {
          name: "Investment",
          desc: "Prodigy Green Energy is expanding its business in investment by partnerships and acquiring more assets from property or long-term contract investment projects, through green field projects or merger & acquisition projects.",
          svg: require("@/assets/icons/service1.svg"),
        },
        {
          name: "ECP",
          desc: "Engineering, Procurement and Construction (EPC) Contractor, especially in the field of renewable energies.",
          svg: require("@/assets/icons/service2.svg"),
        },
        {
          name: "Management",
          desc: "With our management team along with an abundant of experts in the related fields, we are able to plan, manage and perform even the most challenging task to adhere to our client’s requirements.",
          svg: require("@/assets/icons/service3.svg"),
        },
      ],
    };
  },
};
</script>

<style>
</style>