<template>
  <section class="home-page">
    <div class="slider-section">
      <slider-section />
    </div>
    <div class="mobile-design-strip mb-5">
     <b-container>
        <div class="strip-content">
          <div class="strip-title">MOBILE HOME DESIGN COLLECTIONS</div>
         <div class="strip-link"> 
           <a href="/design-collection">View More...</a>
         </div>
        </div>
     </b-container>
    </div>
    <b-container>
      <div class="our-service-section mb-5">
        <div class="text-center main-heading pb-4 ">
          <span class="head-border">DESIGN COLLECTIONS</span>
        </div>
        <div class="our-service-types">
          <b-row class="m-0 p-0">
            <b-col
              lg="4"
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
                 <div class="pt-3 font-weight-bold text-center">
              {{data.title}}
            </div>
              </div>
            </b-col>
          </b-row>
        </div>
      </div>
    </b-container>
    <div class="about-us-section mb-5">
      <b-container>
        <div class="py-5" >
          <div class="title main-heading pb-4">
            <span class="head-border">We Have Story Of Us For You To Discover</span>
          </div>
          <div class="des">
            <p>
             Our homes aren’t supplied fully finished from a factory. We produce
            the timber frame panels in our workshops and assemble the structure
            on-site in accordance with the ‘Caravans Act’.
            </p>
            <p class="m-0">
             Each home is
            uniquely designed and finished to the requirements of the customer,
            in terms of style and budget.
             
            </p>
            <div class="mt-4"> <a href="/about-us"><span class="read-btn">Read More...</span></a></div>
          </div>
        </div>
      </b-container>
  <div class="overlay"></div>
    </div>
  </section>
</template>

<script>
import sliderSection from "~/components/slider-section.vue";
import img1 from "~/assets/images/design-collection/Feature-Oak.png";
import img2 from "~/assets/images/design-collection/Dune-Zink.png";
import img3 from "~/assets/images/design-collection/Park-Home.png";

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
          title: "Feature Oak"
        },
        {
          key: 2,
          img: img2,
          title: "Dune Zink"
        },
        {
          key: 3,
          img: img3,
          title: "Park Home"
        },
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
    // &:hover {
    //   transform: scale(1.015);
    //   transition: transform 0.3s;
    // }
  }
  .card {
    border: 0px;
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
.about-us-section {
  background: url("~assets/images/home-banner/about-banner.png");
  color: white;
}

.mobile-design-strip{
  background-color: $primary;
.strip-content{
  display: flex;
  justify-content: space-between;
}
.strip-link{
  margin: auto 0px;
 a{
   color: $white;
 }
}
  .strip-title{
        color: white;
    padding: 20px 0px;
    font-size: 20px;
  }
}
.read-btn{
      background: white;
    padding: 8px 15px;
    border-radius: 4px;
    color: black;
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
  .mobile-design-strip{
    .strip-title{
    font-size: 12px;
  }
  }
  
}

</style>
