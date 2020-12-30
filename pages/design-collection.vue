<template>
  <div>
    <b-container>
      <b-row>
        <b-col lg="6" md="6" sm="12" v-for="data in products"
              :key="data.key">
          <div>
            <div class="pb-2">
              <img
                :src="data.img"
                alt=""
                width="100%"
              />
            </div>
            <div class="pb-3 font-weight-bold">
              {{data.title}}
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import img1 from "~/assets/images/design-collection/bay.png";
import img2 from "~/assets/images/design-collection/Park-Home.png";
import img3 from "~/assets/images/design-collection/Outlook.png";
import img4 from "~/assets/images/design-collection/Feature-Oak.png";
import img5 from "~/assets/images/design-collection/Dune-Zink.png";
import img6 from "~/assets/images/design-collection/Dune-Oak.png";
import img7 from "~/assets/images/design-collection/Mackintosh-Pavilion.png";
import img8 from "~/assets/images/design-collection/Observatory.png";

export default {
  data() {
    return {
      products: [
        {
          key: 1,
          img: img1,
          title: "Bay Feature"
        },
        {
          key: 2,
          img: img2,
          title: "Park Home"
        },
        {
          key: 3,
          img: img3,
          title: "Outlook"
        },
        {
          key: 4,
          img: img4,
          title: "Feature Oak"
        },
        {
          key: 5,
          img: img5,
          title: "Dune Zink"
        },
        {
          key: 6,
          img: img6,
          title: "Dune Oak"
        },
        {
          key: 7,
          img: img7,
          title: "Mackintosh Pavilion"
        },
        {
          key: 8,
          img: img8,
          title: "Observatory"
        }
      ]
    };
  }
};
</script>
