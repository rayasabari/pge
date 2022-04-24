<template>
  <div>
    <div class="min-h-screen">
      <Breadcrumb :title="'Services'"></Breadcrumb>
      <div id="page-content" class="pt-10 md:pt-0">
        <PageContainer>
          <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
            <SectionTitle class="text-center md:text-left">Independent Power Producer</SectionTitle>
            <div
              class="mb-8 text-center md:text-left"
            >Lorem ipsum dolor sit amet consectetur adipisicing.</div>
          </section>
          <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
            <SectionTitle class="text-center md:text-left">EPC/Projects</SectionTitle>
            <div
              class="mb-8 text-center md:text-left"
            >Lorem ipsum dolor sit amet consectetur adipisicing.</div>
          </section>
        </PageContainer>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Services'
};
</script>

<style>
</style>