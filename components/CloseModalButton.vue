<template>
  <div
    @click="closeModal"
    class="absolute flex items-center justify-center w-8 h-8 text-white border-2 border-white rounded-full cursor-pointer -top-3 -right-3 bg-rose-500"
  >
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="w-5 h-5"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      stroke-width="2"
    >
      <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
    </svg>
  </div>
</template>

<script>
export default {
  name: "CloseModalButton",
  methods:{
    closeModal(){
      this.$root.$emit('closeModal');
    }
  }
};
</script>

<style>
</style>