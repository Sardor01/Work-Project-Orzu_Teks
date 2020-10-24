<template>
  <div :class="className" class="PartnersSlider__container">
    <swiper class="swiper" :options="swiperOption">
      <swiper-slide
        :key="partner.id"
        v-for="partner in partners"
        class="d-flex justify-content-center align-items-center py-3"
      >
        <a :href="partner.partnerUrl">
          <img
            :src="partner.partnerImg"
            width="120"
            :alt="partner.partnerName"
          />
        </a>
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
          autoplay: {
            delay: 4000,
            disableOnInteraction: false,
          },
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
        partners: [
          {
            id: 1,
            partnerImg: "https://vuejs.org/images/vuejobs.png",
            partnerUrl: "https://vuejobs.com",
            partnerName: "Vue Jobs",
          },
          {
            id: 2,
            partnerImg: "https://vuejs.org/images/laravel.png",
            partnerUrl: "https://laravel.com",
            partnerName: "Laravel",
          },
          {
            id: 3,
            partnerImg: "https://vuejs.org/images/vehikl.png",
            partnerUrl: "https://vehikl.com",
            partnerName: "Vehikl",
          },
          {
            id: 4,
            partnerImg: "https://vuejs.org/images/neds.png",
            partnerUrl: "https://neds.com.au",
            partnerName: "Neds",
          },
          {
            id: 5,
            partnerImg: "https://vuejs.org/images/vpnranks.png",
            partnerUrl: "https://www.vpnranks.com",
            partnerName: "VPNRanks",
          },
          {
            id: 6,
            partnerImg: "https://vuejs.org/images/usave.png",
            partnerUrl: "https://usave.co.uk/utilities/broadband",
            partnerName: "usave",
          },
          {
            id: 7,
            partnerImg: "https://vuejs.org/images/tendermint.png",
            partnerUrl: "https://cosmos.network",
            partnerName: "Vue Jobs",
          },
        ],
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