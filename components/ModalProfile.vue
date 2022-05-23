<template>
  <div
    class="fixed top-0 left-0 z-50 flex items-center justify-center w-full h-screen bg-gray-900 bg-opacity-60 backdrop-blur-sm"
    id="modalBackdrop"
  >
    <div
      class="relative flex flex-col md:flex-row w-11/12 p-6 h-[90vh] md:h-auto bg-white rounded-lg md:w-7/12 gap-4 md:gap-0"
      data-aos="fade-down"
    >
      <div class="flex flex-col w-full md:w-3/12">
        <div>
          <img
            :src="data.photo"
            :alt="data.name"
            class="w-full object-cover object-top rounded-lg max-h-[190px] md:h-auto"
          />
        </div>
        <div class="mt-3 text-xl font-semibold text-primary-500">{{ data.name }}</div>
        <div class="font-medium">{{ data.role }}</div>
      </div>
      <div class="w-full overflow-y-scroll text-sm leading-relaxed md:w-9/12 md:pl-6">{{ data.body }}</div>
      <CloseModalButton />
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalProfile",
  props: ["data"],
  mounted() {
    const backdrop = document.querySelector("#modalBackdrop");
    window.addEventListener("click", (e) => {
      if (e.target == backdrop) {
        this.$root.$emit("closeModal");
      }
    });
  },
};
</script>

<style>
</style>