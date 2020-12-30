<template>
  <div>
    <main-header />
    <Nuxt />
    <main-footer />
  </div>
</template>
<script>
import mainHeader from "~/components/header.vue";
import mainFooter from "~/components/footer.vue";

export default {
   components: {
    mainHeader,
    mainFooter
  },
}
</script>
