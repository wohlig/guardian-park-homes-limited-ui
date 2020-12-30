<template>
  <div class="about-section">
    <div class="about-content">
      <div class="image-section mb-5">
        <div class="for-desk">
          <div class="about-banner">
            <img
              src="~assets/images/about us/about-us.png"
              alt=""
              class="img-fluid"
            />
            <div class="banner-text">
              ABOUT US
            </div>
          </div>
        </div>
        <div class="about-banner">
          <div class="for-mob">
            <img
              src="~assets/images/about us/mob-about-us.png"
              alt=""
              class="img-fluid"
            />
            <div class="banner-text">
              ABOUT US
            </div>
          </div>
        </div>
      </div>
      <b-container>
        <div class="about-para mb-5">
          <div>
            Our homes aren’t supplied fully finished from a factory. We produce
            the timber frame panels in our workshops and assemble the structure
            on-site in accordance with the ‘Caravans Act’. This method of
            construction allows us to access difficult to reach back gardens and
            also enables a higher build quality and lower cost. Each home is
            uniquely designed and finished to the requirements of the customer,
            in terms of style and budget. From external finishes like cladding,
            windows, roofs tiles and internal finishes like flooring, kitchens,
            you can have practically anything you want. The key aspect of our
            service is that we offer homes that are built to conform to
            regulations of a ‘mobile home’ but have the insulation values, wall
            thickness and finishes of a conventional building regulation house.
            Designed for long-term year-round use.
          </div>
        </div>
      </b-container>
      <div class="bg-lightblue about-us-img mb-5">
        <b-container>
          <b-row>
            <b-col lg="3" md="3" sm="12">
              <div class="margin-mob">
                <img
                  src="@/assets/images/home-product/p1.png"
                  alt=""
                  width="100%"
                />
              </div>
            </b-col>

            <b-col lg="3" md="3" sm="12">
              <div class="margin-mob">
                <img
                  src="@/assets/images/home-product/p2.png"
                  alt=""
                  width="100%"
                />
              </div>
            </b-col>

            <b-col lg="3" md="3" sm="12">
              <div class="margin-mob">
                <img
                  src="@/assets/images/home-product/p3.png"
                  alt=""
                  width="100%"
                />
              </div>
            </b-col>

            <b-col lg="3" md="3" sm="12">
              <div class="margin-mob">
                <img
                  src="@/assets/images/home-product/p7.png"
                  alt=""
                  width="100%"
                />
              </div>
            </b-col>
          </b-row>
        </b-container>
      </div>
      <b-container>
        <div>
          <div class="main-heading mb-3">QUICK POINTS</div>
          <p>
            Homes can be supplied fully finished or as kit builds for
            self-builders, developers and DIY enthusiasts.
          </p>
          <p>
            We make structures that conform to the definition of a ‘caravan’.
            Although transportable they often will not require wheels.
          </p>
          <p>
            They look and feel just like normal houses both inside and out.
          </p>
          <p>
            Our operation is essentially that of a timber frame builder and
            main-contraction service. We have a carpentry workshop and admin
            offices.
          </p>
          <p>
            We’re a flexible manufacturing company who welcome each opportunity
            to build a new and exciting home.
          </p>
        </div>
      </b-container>
      <div>
        <img
          src="~assets/images/home-banner/slider2.png"
          alt=""
          class="img-fluid"
        />
      </div>
    </div>
  </div>
</template>
<style lang="scss">
@import "~assets/scss/_variable";
.about-content {
  .about-para {
    line-height: 200%;
  }
}
.about-banner {
  position: relative;
  .banner-text {
    font-size: 28px;
    font-weight: bold;
    color: $white;
    margin: 0;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: black;
    opacity: 0.6;
    padding: 10px 20px;
  }
}

.about-us-img {
  padding: 30px 0px;
}
@media only screen and (max-width: 767px) {
  .image-section {
    .banner-text {
      font-size: 1.6rem;
    }
  }
  .margin-mob{
    margin-bottom: 15px;
  }
}
</style>
