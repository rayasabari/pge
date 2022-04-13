<template>
  <div
    class="flex flex-col gap-8 md:sticky md:top-24"
    data-aos="fade-up"
    data-aos-delay="300"
    data-aos-duration="1000"
  >
    <nav class>
      <ul class="flex flex-col gap-1">
        <li
          v-for="menu in menus"
          :key="menu.name"
          class="overflow-hidden text-center text-gray-400 bg-gray-100 rounded-lg md:text-left"
        >
          <NuxtLink
            :to="menu.link"
            active-class="link-active-side"
            class="block px-4 py-3 font-medium transition-all duration-500 border-gray-300 hover:bg-gray-50 hover:text-primary-500 hover:border-l-4 hover:border-primary-500"
          >{{menu.name}}</NuxtLink>
        </li>
      </ul>
    </nav>
    <div class="p-5 text-center text-white rounded-lg bg-primary-700 md:text-left">
      <h3 class="mb-2 text-lg font-semibold">How can we help you?</h3>
      <p
        class="text-sm text-primary-50"
      >Contact us at the Prodigy Green Energy office nearest to you or submit a business inquiry online.</p>
      <div class="mt-5 mb-2">
        <NuxtLink to="/contact-us" class="btn-pge">Contact Us</NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Sidebar",
  data() {
    return {
      menus: [
        {
          name: "Company Overview",
          link: "/company-overview",
        },
        {
          name: "Management Profiles",
          link: "/management-profiles",
        },
        {
          name: "Products & Services",
          link: "/products-and-services",
        },
        {
          name: "News",
          link: "/news",
        },
        {
          name: "Contact Us",
          link: "/contact-us",
        },
      ],
    };
  },
};
</script>

<style>
</style>