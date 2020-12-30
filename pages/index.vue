<template>
  <section class="home-page">
    <div class="slider-section mb-5">
      <slider-section />
    </div>
    <b-container>
      <div class="our-service-section mb-5">
        <div class="text-center main-heading pb-4 ">
          <span class="head-border">
WORK WE DO</span>
        </div>
        <div class="our-service-types">
          <b-row class="m-0 p-0">
            <b-col
              lg="3"
              md="4"
              sm="12"
              class="mb-3"
              v-for="data in products"
              :key="data.key"
            >
              <div class="mb-2 rel card our-service-contains relative">
                <div class="service-img">
                  <img :src="data.img" alt="" width="100%" />
                </div>
                <!-- <div class="type-name text-center sub-heading">
                  {{ data.title }}
                </div> -->
              </div>
            </b-col>
          </b-row>
        </div>
      </div>
    </b-container>
  <div class="about-us-section mb-5 p-4">
      <b-container>
      <div>
        <div class="title text-center main-heading pb-4">
          <span class="head-border">ABOUT US</span>
        </div>
        <div class="des text-center">
          <p>
             Our portfolio is diverse in both scale and character,
                        from luxury apartments to exceptional townhouses and the
                        sympathetic conversion of heritage buildings, with all
                        of our thoughtfully designed schemes being reflective of
                        our desire to produce innovative homes that act as
                        harmonious spaces, in which people can thrive.
          </p>
          <p class="m-0">
           The properties we build combine a creative, considered,
                        intelligent design philosophy with exceptional attention
                        to detail and commitment to both innovation and the
                        environment.
            <a href="/about-us">Read More...</a>
          </p>
        </div>
      </div>
    </b-container>
  </div>
  </section>
</template>

<script>
import sliderSection from "~/components/slider-section.vue";
import img1 from "~/assets/images/home-product/p1.png";
import img2 from "~/assets/images/home-product/p2.png";
import img3 from "~/assets/images/home-product/p3.png";
import img4 from "~/assets/images/home-product/p4.png";
import img5 from "~/assets/images/home-product/p5.png";
import img6 from "~/assets/images/home-product/p6.png";
import img7 from "~/assets/images/home-product/p7.png";
import img8 from "~/assets/images/home-product/p8.png";

export default {
  components: {
    sliderSection
  },
  data() {
    return {
      products: [
        {
          key: 1,
          img: img1,
          title: "Solid wood"
        },
        {
          key: 2,
          img: img2,
          title: "Engineered"
        },
        {
          key: 3,
          img: img3,
          title: "Laminated Flooring"
        },
        {
          key: 4,
          img: img4,
          title: "Exotic Bamboo"
        },
        {
          key: 5,
          img: img5,
          title: "KAINDL Venner"
        },
        {
          key: 6,
          img: img6,
          title: "Exterior Deck Tile"
        },
        {
          key: 7,
          img: img7,
          title: "Exterior Deck Tile"
        },
        {
          key: 8,
          img: img8,
          title: "Exterior Deck Tile"
        }
      ]
    };
  }
};
</script>
<style lang="scss">
@import "~assets/scss/_variable";
.our-service-types {
  .our-service-contains {
    .service-img {
      height: 300px;
      img {
        height: 100%;
      }
    }
    &:hover {
      transform: scale(1.015);
      transition: transform 0.3s;
    }
  }
  .card {
    border: 1px solid $primary;
    cursor: pointer;
    &:hover {
      .type-name {
        display: block;
      }
    }

    .type-name {
      padding: 5px;
      position: absolute;
      bottom: 0px;
      color: white;
      width: 100%;
      background: #0000005e;
      display: none;
    }
    .type-des {
      padding: 10px;
    }
  }
}
.about-us-section{
  background-color: #362d663d;
}
// for ipad
@media only screen and (min-device-width: 768px) and (max-device-width: 991px) {
  .contact-us-section {
    .title {
      font-size: 20px;
    }
  }
}
@media only screen and (max-width: 767px) {
  .contact-us-section {
    .title {
      font-size: 20px;
    }
    .btn-lg {
      font-size: 18px;
    }
  }
}
</style>
