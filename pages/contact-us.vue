<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Contact Us'"></Breadcrumb>
    <section id="page-content">
      <PageContainer>
        <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
          <SectionTitle class="text-center md:text-left">Contact Us</SectionTitle>
          <iframe
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3966.6664669606753!2d106.82496411487965!3d-6.17538706223319!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e69f5d2e764b12d%3A0x3d2ad6e1e0e9bcc8!2sNational%20Monument!5e0!3m2!1sen!2sid!4v1649536699571!5m2!1sen!2sid"
            class="w-full"
            height="450"
            style="border:0;"
            allowfullscreen
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
          <div class="w-full p-4 mt-4 rounded-lg bg-primary-50 text-primary-800">
            Jl. Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iure, eligendi!
          </div>
        </section>
        <section class="mt-4" data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
          <SectionTitle class="text-center md:text-left">Contact Form</SectionTitle>
          <div class="flex flex-col gap-4 md:gap-8 md:flex-row">
            <div class="w-full md:w-1/2">
              <div class="mb-5">
                <label class="block mb-2" for="fullname">Fullname</label>
                <input id="fullname" type="text" class="form-pge" required />
              </div>
              <div class="mb-4">
                <label class="block mb-2" for="email">Email</label>
                <input id="email" type="email" class="form-pge" required />
              </div>
              <div class="mb-4">
                <label class="block mb-2" for="phone">Phone</label>
                <input id="phone" type="tel" class="form-pge" required />
              </div>
            </div>
            <div class="w-full md:w-1/2">
              <div class="mb-4">
                <label class="block mb-2" for="message">Message</label>
                <textarea name="message" id="message" cols="30" rows="5" class="form-pge" required></textarea>
              </div>
              <div class="mt-7">
                <Button class="py-3">Submit</Button>
              </div>
            </div>
          </div>
        </section>
      </PageContainer>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>