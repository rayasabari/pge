<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Projects and Achievments'"></Breadcrumb>
    <div id="page-content">
      <PageContainer>
        <section
          data-aos="fade-up"
          data-aos-delay="300"
          data-aos-duration="1000"
        >
          <SectionTitle>Projects and Achievements</SectionTitle>
          <p
            class="leading-relaxed"
          >Lorem ipsum dolor sit amet consectetur adipisicing elit. Exercitationem ipsa accusamus nesciunt debitis dicta quaerat illum, quae qui quia consequuntur eligendi quo doloribus. Numquam quibusdam accusamus, provident sapiente vero modi.</p>
          <CardProjects :projects="projects" />
        </section>
      </PageContainer>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectsAndAchievements",
  data() {
    return {
      projects: [
        {
          title: `Sidoarjo PV Plant`,
          desc: `1 MWp pilot to 100 MWp Solar PV plant project`,
          image: `https://radarsurabaya.jawapos.com/wp-content/uploads/2021/04/pemkot-segera-tambah-rusun-dilengkapi-dengan-solar-cell_m_256557.jpg`,
        },
        {
          title: `Jakarta Utility Propertindo`,
          desc: `300 MWp Solar PV plant project`,
          image: `https://img.jakpost.net/c/2020/02/14/2020_02_14_86674_1581671669._large.jpg`,
        },
        {
          title: `South and East Kalimantan Clean Technology and Industrial Park`,
          desc: `Provide Solar Power for Green Industrial and Technology Park`,
          image: `https://cdn-2.tstatic.net/kaltim/foto/bank/images/dukung-penerapan-clean-energy-melalui-pengembangan-energi-baru-terbarukan-pt-pupuk-kalimantan-timur.jpg`,
        },
      ],
    };
  },
};
</script>

<style>
</style>