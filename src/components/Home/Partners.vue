<template>
  <div id="partners" class="py-5">
    <div class="container py-4">
      <h1 class="text-center text-uppercase section__title">Наши Партнеры</h1>

      <PartnersSlider className="mt-3 pt-4 pb-5 px-5" />
    </div>
  </div>
</template>

<script>
  import PartnersSlider from "@/components/Home/PartnersSlider";

  export default {
    name: "Partners",
    components: {
      PartnersSlider,
    },
  };
</script>

<style>
</style>