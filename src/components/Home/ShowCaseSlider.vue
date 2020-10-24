<template>
  <swiper class="swiper showCaseSlider__container" :options="swiperOption">
    <swiper-slide>
      <div class="position-relative">
        <img
          class="slider__img"
          src="../../assets/sliderBackground.png"
          alt=""
        />

        <div class="slider__info">
          <h1 class="slider__title text-uppercase">Осенняя</h1>
          <p class="slider__text">Коллекция женской одежды</p>

          <div class="d-flex justify-content-center mt-4">
            <CustomLink
              link="#"
              className="text-center d-inline-block"
              text="Подробнее"
            />
          </div>
        </div>
        <div class="slider__opacity"></div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <img
        class="w-100 slider__img"
        src="https://images.unsplash.com/photo-1602425957633-b062a1908844?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=1288&ixlib=rb-1.2.1&q=80&w=1933"
        alt=""
      />
    </swiper-slide>
    <swiper-slide>
      <img
        src="https://images.unsplash.com/photo-1600836428343-c366d36fb109?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=1288&ixlib=rb-1.2.1&q=80&w=1933"
        alt=""
        class="w-100 slider__img"
      />
    </swiper-slide>
    <swiper-slide>
      <img
        src="https://images.unsplash.com/photo-1601387322984-3b54115157f7?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=1288&ixlib=rb-1.2.1&q=80&w=1933"
        alt=""
        class="w-100 slider__img"
      />
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
    <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div>
  </swiper>
</template>

<script>
  import CustomLink from "@/components/CustomLink";

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
    name: "ShowCaseSlider",
    title: "Autoplay",
    components: {
      CustomLink,
      Swiper,
      SwiperSlide,
    },
    data() {
      return {
        swiperOption: {
          spaceBetween: 20,
          centeredSlides: true,
          loop: false,
          grabCursor: true,
          effect: "fade",
          // autoplay: {
          //   delay: 4000,
          //   disableOnInteraction: false,
          // },
          pagination: {
            el: ".swiper-pagination",
            clickable: true,
          },
          navigation: {
            nextEl: ".swiper-button-next",
            prevEl: ".swiper-button-prev",
          },
        },
      };
    },
  };
</script>

<style lang="scss" scoped>
  .swiper {
    max-height: 550px;
    width: 100%;

    .swiper-slide {
      overflow: hidden;
      position: relative;
      text-align: center;
      color: #fff;
    }
  }

  .slider__img {
    width: 100%;
    max-height: 550px;
    object-fit: cover;
    object-position: 0 0;
  }

  .swiper-button-prev:after,
  .swiper-button-next:after {
    color: #ccc;
    font-size: 1.1rem;
    font-weight: 700;
  }

  .slider__info {
    position: absolute;
    z-index: 1;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .slider__title {
    font-weight: 600;
    font-size: 3.2rem;
    letter-spacing: 1px;
  }

  .slider__opacity {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 550px;
    background-color: rgba(0, 0, 0, 0.5);
    transition: background-color 0.25s ease-in-out;
  }

  @media only screen and (min-width: 992px) {
    .swiper-button-prev {
      margin-left: 2rem;
    }

    .swiper-button-next {
      margin-right: 2rem;
    }

    .swiper-button-prev:after {
      margin-left: 4.2rem;
    }

    .swiper-button-next:after {
      margin-right: 4.5rem;
    }

    .swiper-button-prev::before {
      content: "назад";
      text-transform: uppercase;
      color: #ccc;
      font-size: 0.65rem;
      font-weight: 600;
      margin-left: 0.5rem;
      position: absolute;
    }

    .swiper-button-next::before {
      content: "вперед";
      text-transform: uppercase;
      color: #ccc;
      font-size: 0.65rem;
      margin-right: 0.5rem;
      font-weight: 600;

      position: absolute;
    }
  }
</style>