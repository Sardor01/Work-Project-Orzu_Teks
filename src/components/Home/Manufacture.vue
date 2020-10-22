<template>
  <div id="manufacture" class="py-5">
    <div class="container">
      <h1 class="text-center text-uppercase section__title">
        Контактное Производство
      </h1>

      <div class="models my-5 d-flex justify-content-center flex-wrap">
        <div class="fashion d-flex flex-lg-column">
          <div class="manufacture__models">
            <img
              src="../../assets/manufacture/gloriaJeansModels.png"
              alt="models"
            />
          </div>
          <div class="manufacture__img">
            <img
              src="../../assets/manufacture/fashionBlueBox.png"
              alt="fashion"
            />

            <div class="fashion__text">
              <div class="fashion__name">Gloria Jeans</div>

              <div class="line"></div>

              <img src="../../assets/manufacture/gloriaJeans.png" alt="" />
            </div>
          </div>
        </div>

        <div class="fashion d-flex flex-lg-column align-items-stretch">
          <div class="manufacture__img">
            <img
              src="../../assets/manufacture/fashionBlueBox.png"
              alt="fashion"
            />

            <div class="fashion__text">
              <div class="fashion__name">Zara</div>

              <div class="line"></div>

              <img src="../../assets/manufacture/zara.png" alt="" />
            </div>
          </div>
          <div class="manufacture__models">
            <img src="../../assets/manufacture/zaraModels.png" alt="models" />
          </div>
        </div>

        <div class="fashion d-flex flex-lg-column">
          <div class="manufacture__models">
            <img
              src="../../assets/manufacture/tommyHillModel.png"
              alt="models"
            />
          </div>
          <div class="manufacture__img">
            <img
              src="../../assets/manufacture/fashionBlueBox.png"
              alt="fashion"
            />

            <div class="fashion__text">
              <div class="fashion__name">Tommy Hilfiger</div>

              <div class="line"></div>

              <img src="../../assets/manufacture/tommyHill.png" alt="" />
            </div>
          </div>
        </div>
      </div>

      <div class="d-flex justify-content-center">
        <CustomButton
          className="text-center d-inline-block"
          text="Посмотреть все"
        />
      </div>
    </div>
  </div>
</template>

<script>
  import CustomButton from "@/components/CustomButton";

  export default {
    name: "Manufacture",
    components: {
      CustomButton,
    },
  };
</script>

<style lang="scss" scoped>
</style>