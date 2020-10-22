<template>
  <div :class="className" class="PartnersSlider__container">
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide>
        <img
          src="../../assets/partners/partner1.png"
          width="55"
          height="100"
          alt="partner"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../../assets/partners/partner2.png"
          width="55"
          height="100"
          alt="partner"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../../assets/partners/partner3.png"
          width="55"
          height="100"
          alt="partner"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../../assets/partners/partner4.png"
          width="55"
          height="100"
          alt="partner"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../../assets/partners/partner5.png"
          width="55"
          height="100"
          alt="partner"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../../assets/partners/netlify.png"
          width="55"
          height="100"
          alt="partner"
        />
      </swiper-slide>
      <swiper-slide>
        <img
          src="../../assets/partners/firebase.png"
          width="55"
          height="100"
          alt="partner"
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
  import { Swiper, SwiperSlide } from "vue-awesome-swiper";

  import SwiperCore, {
    Navigation,
    Pagination,
    Scrollbar,
    A11y,
    Autoplay,
    EffectFade,
  } from "swiper";

  SwiperCore.use([Navigation, Pagination, Scrollbar, A11y, Autoplay, EffectFade]);

  export default {
    name: "PartnersSlider",
    title: "Responsive breakpoints",
    components: {
      Swiper,
      SwiperSlide,
    },
    props: {
      className: {
        type: String,
      },
    },
    data() {
      return {
        swiperOption: {
          spaceBetween: 50,
          loop: false,
          grabCursor: true,
          pagination: {
            el: ".swiper-pagination",
            clickable: true,
          },
          breakpoints: {
            1024: {
              slidesPerView: 5,
              spaceBetween: 40,
            },
            768: {
              slidesPerView: 4,
              spaceBetween: 30,
            },
            640: {
              slidesPerView: 3,
              spaceBetween: 20,
            },
            320: {
              slidesPerView: 2,
              spaceBetween: 10,
            },
          },
        },
      };
    },
  };
</script>

<style lang="scss" scoped>
  .swiper {
    width: 100%;
    height: auto;
    min-height: 100px;

    .swiper-slide {
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      font-weight: bold;
      font-size: 1.2rem;
    }
  }
</style>