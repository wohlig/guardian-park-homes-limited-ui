<template>
  <section>
    <div class="slider-section">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide v-for="data in products" :key="data.key">
          <div class="swiper-img">
            <b-img :src="data.img" class="img"/>
          </div>
        </swiper-slide>

        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </section>
</template>
<script>
import { Swiper, SwiperSlide } from "vue-awesome-swiper";
import "swiper/css/swiper.css";
import img1 from "~/assets/images/home-banner/s1.jpg";
import img2 from "~/assets/images/home-banner/s2.jpg";


export default {
  name: "swiper-example-multiple-slides-per-biew",
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      products: [
        {
          key: 1,
          img: img1,
        },
        {
          key: 2,
          img: img2,
        },
      ],
      swiperOption: {
        autoplay: { delay: 3000 },
        slidesPerView: 1,
        loop: true,
        slidesPerGroup: 1,
        breakpoints: {
          320: {
            slidesPerView: 1,
            slidesPerGroup: 1
          },
          640: {
            slidesPerView: 1,
            slidesPerGroup: 1
          },
          768: {
            slidesPerView: 1,
            slidesPerGroup: 1
          },
          1024: {
            slidesPerView: 1,
            slidesPerGroup: 1
          }
        },
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        }
      }
    };
  }
};
</script>
<style lang="scss">
@import "~assets/scss/_variable";
.swiper-pagination-bullet {
  width: 12px !important;
  height: 12px !important;
  background: $white !important;
  opacity: 0.4 !important;
}
.swiper-pagination-bullet-active {
  background: $primary !important;
  opacity: 1 !important;
}
.swiper-img {
  img {
    width: 100%;
    height: 100%;
  }
}
// for ipad
@media only screen and (min-device-width: 768px) and (max-device-width: 991px) {
  .slider-section {
    .banner-text {
      font-size: 16px;
    }
  }
}
@media only screen and (max-width: 767px) {
  .slider-section {
    .banner-text {
      font-size: 14px;
      .text-width {
        width: 80%;
      }
    }
  }
}
@media (min-width: 200px) and (max-width: 350px) {
  .slider-section {
    .banner-text {
      font-size: 12px;
    }
  }
}
</style>
