<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'News'"></Breadcrumb>
    <div id="page-content">
      <Container class="flex flex-col gap-20 py-5 md:gap-8 md:flex-row md:py-20">
        <div class="w-full md:w-9/12">
          <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
            <SectionTitle class="text-center">News</SectionTitle>
            <CardNews :news="news" />
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
  data() {
    return {
      news: [
        {
          title:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolores, doloribus.",
          excerpt:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Libero alias earum laborum aperiam accusamus quis. Voluptate excepturi error explicabo totam saepe consequatur ullam quos laborum corrupti sed soluta, officia ex?",
          published_at: "23 Maret 2022",
          thumbnail:
            "https://preview.cruip.com/tidy/images/features-home-3-02.jpg",
        },
        {
          title:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolores, doloribus.",
          excerpt:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Libero alias earum laborum aperiam accusamus quis. Voluptate excepturi error explicabo totam saepe consequatur ullam quos laborum corrupti sed soluta, officia ex?",
          published_at: "23 Maret 2022",
          thumbnail:
            "https://preview.cruip.com/tidy/images/features-home-3-02.jpg",
        },
        {
          title:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolores, doloribus.",
          excerpt:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Libero alias earum laborum aperiam accusamus quis. Voluptate excepturi error explicabo totam saepe consequatur ullam quos laborum corrupti sed soluta, officia ex?",
          published_at: "23 Maret 2022",
          thumbnail:
            "https://preview.cruip.com/tidy/images/features-home-3-02.jpg",
        },
        {
          title:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolores, doloribus.",
          excerpt:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Libero alias earum laborum aperiam accusamus quis. Voluptate excepturi error explicabo totam saepe consequatur ullam quos laborum corrupti sed soluta, officia ex?",
          published_at: "23 Maret 2022",
          thumbnail:
            "https://preview.cruip.com/tidy/images/features-home-3-02.jpg",
        },
        {
          title:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dolores, doloribus.",
          excerpt:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Libero alias earum laborum aperiam accusamus quis. Voluptate excepturi error explicabo totam saepe consequatur ullam quos laborum corrupti sed soluta, officia ex?",
          published_at: "23 Maret 2022",
          thumbnail:
            "https://preview.cruip.com/tidy/images/features-home-3-02.jpg",
        },
      ],
    };
  },
};
</script>

<style>
</style>