<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Our Values'"></Breadcrumb>
    <div id="page-content">
      <PageContainer class="leading-relaxed">
        <section
          data-aos="fade-up"
          data-aos-delay="300"
          data-aos-duration="1000"
        >
          <SectionTitle>Vision</SectionTitle>
          <p
            class="pb-6 leading-relaxed"
          >To be the leading renewable energy provider in Indonesia for the benefits of Indonesia and its shareholders</p>
        </section>
        <section
          data-aos="fade-up"
          data-aos-delay="300"
          data-aos-duration="1000"
        >
          <SectionTitle>Mission</SectionTitle>
          <p
            class="pb-6 leading-relaxed"
          >Transforming opportunities into realities; discovering, developing and producing renewable energy with more efficiency and productivity, safety and environmental friendly operation, respecting people, maintaining good relation with all stakeholders.</p>
        </section>
        <section
          data-aos="fade-up"
          data-aos-delay="300"
          data-aos-duration="1000"
        >
          <SectionTitle>Values</SectionTitle>
          <p class="pb-2 text-xl font-medium tracking-widest">CRIFER</p>
          <ul>
            <li class="tracking-widest"><span class="text-lg font-bold">C</span>ollaboration</li>
            <li class="tracking-widest"><span class="text-lg font-bold">R</span>eliability</li>
            <li class="tracking-widest"><span class="text-lg font-bold">I</span>nnovation</li>
            <li class="tracking-widest"><span class="text-lg font-bold">F</span>airness</li>
            <li class="tracking-widest"><span class="text-lg font-bold">E</span>xcellence</li>
            <li class="tracking-widest"><span class="text-lg font-bold">R</span>esourceful</li>
          </ul>
        </section>
      </PageContainer>
    </div>
  </div>
</template>

<script>
export default {
  name: "CorporateInformation",
};
</script>

<style>
</style>