<template>
  <div id="uniform" class="container my-5">
    <h1 class="text-center text-uppercase section__title">Униформа</h1>

    <div class="uniforms row justify-content-center">
      <div class="col-lg-4 col-sm-6 col-12">
        <b-card class="card">
          <img
            src="../../assets/uniform/uniform1.png"
            class="mb-2 uniform__img"
            alt="Uniform"
          />
          <b-card-text class="d-flex align-items-center">
            <div class="uniform__line"></div>
            <div class="uniform__text">Униформа авиакомпании</div>
          </b-card-text>
        </b-card>
      </div>
      <div class="col-lg-4 col-sm-6 col-12">
        <b-card class="card">
          <img
            src="../../assets/uniform/uniform2.png"
            class="mb-2 uniform__img"
            alt="Uniform"
          />
          <b-card-text class="d-flex align-items-center">
            <div class="uniform__line"></div>
            <div class="uniform__text">Рабочая униформа</div>
          </b-card-text>
        </b-card>
      </div>
      <div class="col-lg-4 col-sm-6 col-12">
        <b-card class="card">
          <img
            src="../../assets/uniform/uniform3.png"
            class="mb-2 uniform__img"
            alt="Uniform"
          />
          <b-card-text class="d-flex align-items-center">
            <div class="uniform__line"></div>
            <div class="uniform__text">Униформа для университета</div>
          </b-card-text>
        </b-card>
      </div>
    </div>

    <div class="d-flex justify-content-center mt-3">
      <CustomButton
        className="text-center d-inline-block"
        text="Посмотреть все"
      />
    </div>
  </div>
</template>

<script>
  import CustomButton from "@/components/CustomButton";

  export default {
    name: "Uniform",
    components: {
      CustomButton,
    },
  };
</script>

<style>
</style>