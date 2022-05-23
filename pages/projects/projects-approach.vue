<template>
  <div class="min-h-screen">
    <Breadcrumb :title="'Projects Schema'"></Breadcrumb>
    <div id="page-content">
      <PageContainer>
        <section data-aos="fade-up" data-aos-delay="300" data-aos-duration="1000">
          <SectionTitle>Projects Approach</SectionTitle>
          <p
            class="leading-relaxed"
          >Most on-site renewable energy projects follow a common project development pathway from a project's conception to its completion.</p>
          <CardSteps :steps="steps"/>
        </section>
      </PageContainer>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectsApproach",
  data() {
    return {
      steps: [
        {
          no: 1,
          title: `Establish a renewable energy project development`,
          text: `Establishing a publicly available renewable energy project development and/or renewable energy usage goal helps bring clarity and focus to the process of developing project development.`,
        },
        {
          no: 2,
          title: `Develop a project development plan`,
          text: `One of the best indicators of project development success includes use of a renewable energy project development plan. The plan will detail the organization's specific set of circumstances and design a pathway from start to finish towards realizing the development of the renewable energy project.`,
        },
        {
          no: 3,
          title: `Assess your renewable energy site opportunities`,
          text: `Collect site information and utility data. This information becomes critical when seeking renewable energy project proposals from developers and is the basis for conducting site assessments to identify the most suitable sites.`,
        },
        {
          no: 4,
          title: `Develop and issue a Request for Proposals`,
          text: `Once Prodigy Green Energy has collected the necessary information and data regarding your renewable energy site opportunities, the next step is to develop a renewable energy request for proposals (RFP). An RFP is a solicitation for products and services that outlines the general terms and conditions of request from market suppliers.`,
        },
        {
          no: 5,
          title: `Review and evaluate the renewable energy project proposals`,
          text: `An RFP will generally result in one or more renewable energy project proposals from developers. Evaluating these renewable energy project proposals objectively can be challenging, yet is critical for selecting the best project that meets the client's goals.`
        },
        {
          no: 6,
          title: `Select a project proposal and sign a contract`,
          text: `After Prodigy Green Energy identify the best project opportunity, it is time to sign a contract. Once selected signed the contract, Prodigy Green Energy would consider issuing a press release to publicize the future project more broadly.`
        },{
          no: 7,
          title: `Build and commission your project`,
          text: `Once the renewable energy project is built and generating the power, the client would be excited to share the experience of developing renewable energy project success.`
        }
      ],
    };
  },
};
</script>

<style>
</style>