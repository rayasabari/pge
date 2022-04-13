<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Management Profiles'"></Breadcrumb>
    <div id="page-content">
      <PageContainer>
        <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
          <SectionTitle class="text-center md:text-left">Management Profiles</SectionTitle>
          <ListProfiles :profiles="profiles" />
        </section>
      </PageContainer>
    </div>
    <transition
      name="custom-classes-transition"
      enter-active-class="animate__animated animate__fadeIn animate__faster"
      leave-active-class="animate__animated animate__fadeOut animate__faster"
    >
      <ModalProfile v-if="showModal" :data="dataModal" />
    </transition>
  </div>
</template>

<script>
export default {
  name: "ManagementProfiles",
  data() {
    return {
      showModal: false,
      dataModal: "",
      profiles: [
        {
          id: 1,
          name: "Imam P. Agustino",
          role: "Founder & CEO",
          photo: require("../assets/images/photos/management-ceo.webp"),
          body: `34 years experience in energy and technology sector. Former CEO of PT Energi Mega Persada Tbk. a Leading Public Oil & Gas upstream Company in Indonesia, from 2008 to 2020. Founder and chairman in few energy and technology companies. He had experienced in various large scale business and company development and operation, in depth knowledge in financial and capital market. He had experienced in working with international company Trafalgar House UK, Kvaerner Norway, Global Trade Network Singapore. He received his bachelor degree and engineer degree in Civil Engineer from Parahyangan University, Bandung Indonesia in 1988.`,
        },
        {
          id: 2,
          name: "Didit A. Ratam",
          role: "TBA",
          photo: require("../assets/images/photos/management-tba.webp"),
          body: `32 years experienced in upstream and downstream energy sector. Former CFO of PT Energi Mega Persada Tbk. a Leading Public Oil & Gas upstream Company in Indonesia, from 2008 to 2017. 1990 – 1991 Mobil South Inc. (Mobil Oil Corp) – Fairfax, VA. Treasury Dept, Risk Management. 1992 Gas Venture Advisers – Boston, MA. Independent Power Producer.Project Team. 1992 –  now , Founder and manage a factories making parts for Oil & Gas production plant, Refineries. He  received his bachelor and engineer degree in gas and petrochemical from University Indonesia in 1987. Master in Business Adm – international business from George Washington University – Washington, DC. School of Government and Business Administration in 1989. Finance/Economics – Doctor in Business Adm from Boston University – Boston, MA. Graduate School of Management in 2000`,
        },
        {
          id: 3,
          name: "Hillman Akil",
          role: "Senior Advisor",
          photo: require("../assets/images/photos/management-sa.webp"),
          body: `36 years experience in technology and energy sector. He had experienced in working with several projects and organizations on Engineering and Management with country experience in USA with HIID for World Bank project; France with Sofresid S.A. for EPC at Sofresid Engineering; Spain - Morocco with John Brown Middle East Engineering LLC for Enagas, S.A.; Sultanate of Oman with Itochu Corporation for Barka Desalination Company; Greece with Kvaerner Engineering & Construction Limited for Optimizing Pre-flash for Light Tight Oil Processing Unit; Hong Kong for Seven Seas Oil (Hongkong) Limited; Malaysia for Sustainable Energy Development Authority; Singapore for Global Trade Network Pte. Ltd.; Timor-Leste with Sinclair Knight Merz, Pty Limited for Government of Timor-Leste Projects; and several projects in Indonesia. He received his bachelor degree and engineer degree in Engineering Science from ITB in 1986. He was joining a Program Investment Appraisal and Management at Harvard University. He was Research Fellow of Center for Advance Engineering Studies of Massachusetts Institute of Technology (MIT), a master degree from Columbia University, “Maitrise de Commerce International” (French MBA degree) from “l'Université du Littoral-Côte d'Opale (ULCO), Institut Superieur de Commerce International (ISCID)”, France. He received British Chevening Award from British Government for Advanced Management Programme at Green Templeton College, University of Oxford; European Union Fellowship for European Energy Policy and Awareness Programme, Institute of Public Administration Ireland and Irish Institute for European Affairs, Leuven, Belgium, and Leadership Award from Bandung Institute of Technology. Also, he certified from Lembaga Ketahanan Nasional Republik Indonesia (LEMHANNAS-RI) / National Resilience Institute of the Republic of Indonesia for strategic assessment of national security and stabilization of national values.`,
        },
      ],
    };
  },
  mounted() {
    this.$root.$on("openModal", (profile) => {
      this.dataModal = profile;
      this.showModal = true;
    });
    this.$root.$on("closeModal", () => {
      this.dataModal = "";
      this.showModal = false;
    });
  },
};
</script>

<style>
</style>