<template>
  <div class="contact-section">
    <div class="map mb-5">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2397.2430276738723!2d-2.0310672491233843!3d53.06990750298434!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487a407d9d01bc21%3A0x8d008b999b69de3f!2sGlencote%20Caravan%20Park!5e0!3m2!1sen!2sin!4v1609246795163!5m2!1sen!2sin"
        width="100%"
        height="450"
        frameborder="0"
        style="border:0;"
        allowfullscreen=""
        aria-hidden="false"
        tabindex="0"
      ></iframe>
    </div>
    <b-container>
      <div class="contact-content mb-5 text-dark">
        <div class="main-heading pb-4 secondary">
          <span class="head-border">BUSINESS INFO</span>
        </div>
        <div class="row pb-5">
          <div class="col-md-4">
            <div class="mb-3">
              <div class="font-18 font-weight-bold">
                <img
                  src="~assets/images/icons/address.svg"
                  alt=""
                  width="20px"
                />
                <span class="secondary">Address:</span>
              </div>
              <div class="font-16">
                Guardian Park Homes Limited <br />Glencote Station Road,<br />
                Cheddleton,<br />
                Leek, <br />ST13 7EE
              </div>
            </div>
          </div>
          <div>
            <b-col>
              <div>
                <div>
                  <div class="font-18 font-weight-bold">
                    <img
                      src="~assets/images/icons/mail.svg"
                      alt=""
                      width="20px"
                    />
                    <span class="secondary">Email:</span>
                  </div>
                  <div class="font-16">
                    <a
                      href="mailto:info@guardianparkhomes.co.uk"
                      class="text-dark"
                    >
                      info@guardianparkhomes.co.uk</a
                    >
                  </div>
                </div>
                <div class="mt-3">
                  <div class="font-18 font-weight-bold">
                    <img
                      src="~assets/images/icons/phone.svg"
                      alt=""
                      width="20px"
                    />

                    <span class="secondary">Phone:</span>
                  </div>
                  <div class="font-16 mb-4">
                    <a href="tel:+44 7310 314017" class="text-dark">
                      +44 7310 314017</a
                    >
                  </div>
                </div>
              </div>
            </b-col>
          </div>
        </div>
      </div>
    </b-container>
  </div>
</template>
<style lang="scss">
@import "~assets/scss/_variable";
.contact-banner {
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
    background: $black;
    opacity: 0.6;
    padding: 10px 20px;
  }
}
@media only screen and (max-width: 767px) {
  .contact-banner {
    .banner-text {
      font-size: 1.4rem;
    }
  }
}
</style>
