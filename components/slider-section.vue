<template>
  <section>
    <div class="slider-section">
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide v-for="data in products" :key="data.key">
          <div class="swiper-img for-desk">
            <b-img :src="data.img" class="img"></b-img>
            <!-- <div class="overlay"></div>
            <div class="banner-text">
              <div class="container">
                <div class="text-center font-26">
                  <p >
                   We're experts <br> in innovative <br> developments
                  </p>
                </div>
              </div>
            </div> -->
          </div>
          <div class="swiper-img for-mob">
            <b-img :src="data.img2" class="img"></b-img>
            
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
import img1 from "~/assets/images/home-banner/slider1.png";
import img2 from "~/assets/images/home-banner/slider2.png";
import img3 from "~/assets/images/home-banner/slider3.png";
import img5 from "~/assets/images/home-banner/mob-slider1.png";
import img6 from "~/assets/images/home-banner/mob-slider2.png";
import img7 from "~/assets/images/home-banner/mob-slider3.png";


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
          img2: img5
        },
        {
          key: 2,
          img: img2,
          img2: img6
        },
        {
          key: 3,
          img: img3,
          img2: img7
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
.slider-section {
  .overlay {
    background: black;
    position: absolute;
    top: 0px;
    height: 100%;
    width: 100%;
    opacity: 0.4;
  }
  .banner-text {
    width: 100%;
    font-size: 22px;
    font-weight: bold;
    color: $white;
    margin: 0;
    position: absolute;
    top: 50%;
    transform: translate(0, -50%);
    // .text-width {
    //   width: 45%;
    // }
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
