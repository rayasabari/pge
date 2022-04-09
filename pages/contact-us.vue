<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Contact Us'"></Breadcrumb>
    <section id="page-content">
      <Container
        class="flex gap-8 py-5 md:py-20"
        data-aos="fade-up"
        data-aos-delay="500"
        data-aos-duration="1000"
      >
        <div class="w-9/12">
          <img
            src="https://www.tbsenergi.com/app/sam/assets/images/e511286a99df2c7466aeae8fcca5851b.jpg?v=1623770296"
            alt="about us"
            class="mb-2 rounded-lg"
          />
        </div>
        <div class="w-3/12">
          <SideBar></SideBar>
        </div>
      </Container>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>