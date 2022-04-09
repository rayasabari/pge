<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'News'"></Breadcrumb>
    <div id="page-content">
      <Container class="flex flex-col gap-20 py-5 md:gap-8 md:flex-row md:py-20">
        <div class="flex flex-col w-full gap-8 md:w-9/12">
          <section
            class="text-center md:text-left"
            data-aos="fade-up"
            data-aos-delay="300"
            data-aos-duration="1000"
          >
            <img
              src="https://www.tbsenergi.com/app/sam/assets/images/e511286a99df2c7466aeae8fcca5851b.jpg?v=1623770296"
              alt="about us"
              class="mb-10 rounded-lg md:mb-12"
            />
            <SectionTitle>Company Overview</SectionTitle>
            <p
              class="pb-6"
            >Lorem, ipsum dolor sit amet consectetur adipisicing elit. Labore expedita molestiae natus, voluptatem provident suscipit, doloribus consequuntur debitis ullam nemo nulla velit aliquid distinctio nisi assumenda ducimus quam delectus omnis ab? Suscipit odit nulla magni numquam cupiditate sit harum incidunt quam debitis? Sunt eum officiis dignissimos cum explicabo dolore quos labore atque molestiae aspernatur perferendis necessitatibus repellendus odit quia debitis quo libero reiciendis velit aut voluptas, laborum soluta. Inventore ut quam cupiditate quasi libero, illum ab quis ducimus quod fugit incidunt voluptate placeat dolore excepturi enim reprehenderit, corrupti praesentium iusto eligendi necessitatibus quibusdam officia eaque! Harum modi in ducimus quaerat?</p>
            <p
              class="pb-6"
            >Lorem ipsum dolor sit, amet consectetur adipisicing elit. Beatae odio voluptatem id molestiae nulla cumque, dolore quisquam praesentium natus quia possimus nesciunt eius autem laborum obcaecati ipsum, velit repudiandae sequi a fugit? Accusamus, magni odio. Voluptates velit natus ipsum magni eos impedit alias, veritatis id tempora porro assumenda autem quas, quae similique corrupti eligendi sapiente? Dignissimos placeat quo alias repellat quisquam. Placeat, doloremque soluta beatae eos fugiat debitis repellendus adipisci?</p>
          </section>
          <section class="flex flex-col gap-8 md:flex-row">
            <div
              class="w-full text-center md:w-1/2 md:text-left"
              data-aos="fade-up"
              data-aos-delay="100"
              data-aos-duration="1000"
            >
              <SectionTitle>Our Vision</SectionTitle>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Officia quam ea at voluptatem sequi accusamus rerum dignissimos nihil ullam, porro praesentium quia accusantium alias itaque vel sapiente facilis aut maiores!</p>
            </div>
            <div
              class="w-full text-center md:w-1/2 md:text-left"
              data-aos="fade-up"
              data-aos-delay="300"
              data-aos-duration="1000"
            >
              <SectionTitle>Our Vision</SectionTitle>
              <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Distinctio, natus repudiandae modi quasi sed excepturi consectetur quos. Reprehenderit, corporis ratione.</p>
            </div>
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
  name: "News",
};
</script>

<style>
</style>