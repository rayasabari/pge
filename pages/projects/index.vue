<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Our Projects'"></Breadcrumb>
    <div id="page-content">
      <PageContainer>
        <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
          <SectionTitle>Projects</SectionTitle>
          <div
            class="mb-8 leading-relaxed"
          >The list provides a sample listing of past projects and assignments managed and/or conducted by Prodigy Green Energy or other business entities and provides an indication of the types of assignments that match our capability.</div>
          <CardNews :news="news" />
        </section>
      </PageContainer>
    </div>
  </div>
</template>

<script>
export default {
  name: "OurProjects",
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