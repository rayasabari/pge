<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Products & Services'"></Breadcrumb>
    <div id="page-content" class="pt-10 md:pt-0">
      <Container class="flex flex-col gap-20 py-5 md:gap-8 md:flex-row md:py-20">
        <div class="flex flex-col w-full gap-16 md:gap-24 md:w-9/12">
          <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
            <SectionTitle class="text-center">Our Products</SectionTitle>
            <div class="mb-8 text-center">Lorem ipsum dolor sit amet consectetur adipisicing.</div>
            <CardProducts :products="products" />
          </section>
          <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
            <SectionTitle class="text-center">Our Services</SectionTitle>
            <div
              class="mb-8 text-center"
            >Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facere!</div>
            <CardServices :services="services" />
          </section>
        </div>
        <div class="w-full md:w-3/12">
          <SideBar></SideBar>
        </div>
      </Container>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductsAndServices",
  data() {
    return {
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
          name: "Service One",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis accusamus veniam hic.",
          svg: require('../assets/icons/service1.svg'),
        },
        {
          name: "Service Two",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis accusamus veniam hic.",
          svg: require('../assets/icons/service2.svg')
        },
        {
          name: "Service Three",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis accusamus veniam hic.",
          svg: require('../assets/icons/service3.svg')
        },
        {
          name: "Service Four",
          desc: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis accusamus veniam hic.",
          svg: require('../assets/icons/service4.svg')
        },
      ],
    };
  },
};
</script>

<style>
</style>