<template>
  <div class="flex flex-col gap-6 mt-8 md:gap-12">
    <div
      v-for="profile in profiles"
      :key="profile.id"
      class="flex flex-col overflow-hidden transition-all duration-300 shadow md:shadow-none md:flex-row"
    >
      <div class="w-full md:w-3/12">
        <img
          :src="profile.photo"
          :alt="profile.name +`'s photo`"
          class="w-full h-[250px] md:h-[180px] object-cover object-top rounded-lg"
        />
      </div>
      <div class="flex flex-col w-full p-4 md:p-0 md:pl-6 md:w-10/12">
        <div class="mb-1 text-xl font-semibold text-primary-500">{{profile.name}}</div>
        <div class="mb-4 font-medium text-gray-600">{{profile.role}}</div>
        <div class="text-sm leading-relaxed">{{exerpt(profile.body)}}</div>
        <div>
          <div @click="openModal(profile)" class="inline-block mt-4 btn-pge">Read More</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ListProfiles",
  props: ["profiles"],
  methods: {
    exerpt(text) {
      return text.substr(0, 100) + " ...";
    },
    openModal(profile){
      this.$root.$emit('openModal', profile);
    }
  },
};
</script>

<style>
</style>