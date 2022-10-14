<template>
  <div>
    <AppHeader />
    <BannerHome />
    <Clients />
    <Specifications />
    <MoreInfo />
    <Services />
    <ShipBanner />
    <CustomSupport />
  </div>
</template>
<script lang="ts" type="module">
import { defineComponent } from "@nuxtjs/composition-api";
import AppHeader from "~/components/AppHeader.vue";
import BannerHome from "~/components/BannerHome.vue";
import Clients from "~/components/Clients.vue";
import Specifications from "~/components/Specifications.vue";
import MoreInfo from "~/components/MoreInfo.vue";
import Services from "~/components/Services.vue";
import ShipBanner from "~/components/ShipBanner.vue";
import CustomSupport from "~/components/CustomSupport.vue";

export default defineComponent({
  name: "HomePage",
  components: { AppHeader, BannerHome, Clients, Specifications, MoreInfo, Services, ShipBanner, CustomSupport,  },

  setup() {},
});
</script>

<style lang="scss" scoped></style>
