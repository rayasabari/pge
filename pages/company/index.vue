<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Company'"></Breadcrumb>
    <div id="page-content">
      <PageContainer>
        <section
          data-aos="fade-up"
          data-aos-delay="300"
          data-aos-duration="1000"
        >
          <img
            src="https://www.tbsenergi.com/app/sam/assets/images/e511286a99df2c7466aeae8fcca5851b.jpg?v=1623770296"
            alt="about us"
            class="mb-10 rounded-lg md:mb-12"
          />
          <SectionTitle>Company</SectionTitle>
          <p class="leading-relaxed">
            <span class="font-bold">Prodigy Green Energy</span> is an Indonesian green technology company with headquartered in Jakarta. Prodigy Green Energy provides:
          </p>
          <ul class="px-4 py-2 leading-relaxed list-disc">
            <li>end to end green and renewable energy.</li>
            <li>generates green energy from Solar PV plant on land, water and sea.</li>
            <li>provides energy transport and distribution in form of battery and energy storage system</li>
          </ul>
          <p class="leading-relaxed">We do EPC as well as an Investment company. As an engineering, procurement, construction and commission company, Prodigy Green Energy provides innovative electrical energy storages, power quality systems, and services. Scalable and modular power electronics, intelligent software technologies, and electrical engineering expertise are the base of our business.</p>
        </section>
      </PageContainer>
    </div>
  </div>
</template>

<script>
export default {
  name: "CompanyOverview",
};
</script>

<style>
</style>