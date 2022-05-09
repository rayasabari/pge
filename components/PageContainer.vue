<template>
  <Container class="flex flex-col gap-20 py-5 md:gap-8 md:flex-row md:py-8">
    <div class="flex flex-col w-full gap-8 md:w-9/12">
      <slot></slot>
    </div>
    <div class="w-full md:w-3/12">
      <SideBar></SideBar>
    </div>
  </Container>
</template>

<script>
export default {
  name: 'PageContainer'
};
</script>

<style>
</style>