<template>
  <div id="uniform" class="container my-5">
    <h1 class="text-center text-uppercase section__title">Униформа</h1>

    <div class="uniforms mt-4 py-3 row justify-content-center">
      <div class="col-lg-4 col-sm-6 col-10 mb-5 mb-lg-0">
        <div class="card">
          <img
            src="../../assets/uniform/uniform1.png"
            class="mb-2 uniform__img"
            alt="Uniform"
          />
          <div class="d-flex align-items-center">
            <div class="uniform__line"></div>
            <div class="uniform__text">Униформа авиакомпании</div>
          </div>
        </div>
      </div>

      <div class="col-lg-4 col-sm-6 col-10 mb-5 mb-lg-0">
        <div class="card">
          <img
            src="../../assets/uniform/uniform2.png"
            class="mb-2 uniform__img"
            alt="Uniform"
          />
          <div class="d-flex align-items-center">
            <div class="uniform__line"></div>
            <div class="uniform__text">Рабочая униформа</div>
          </div>
        </div>
      </div>

      <div class="col-lg-4 col-sm-6 col-10 mb-5 mb-lg-0">
        <div class="card">
          <img
            src="../../assets/uniform/uniform3.png"
            class="mb-2 uniform__img"
            alt="Uniform"
          />
          <div class="d-flex align-items-center">
            <div class="uniform__line"></div>
            <div class="uniform__text">Униформа для университета</div>
          </div>
        </div>
      </div>
    </div>

    <div class="d-flex justify-content-center mt-4">
      <CustomLink
        link="#"
        className="text-center d-inline-block"
        text="Посмотреть все"
      />
    </div>
  </div>
</template>

<script>
  import CustomLink from "@/components/CustomLink";

  export default {
    name: "Uniform",
    components: {
      CustomLink,
    },
  };
</script>

<style>
</style>