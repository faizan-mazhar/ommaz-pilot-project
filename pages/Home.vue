<template>
  <div>
    <AppHeader />
    <BannerHome />
  </div>
</template>
<script lang="ts" type="module">
import { defineComponent } from "@nuxtjs/composition-api";
import AppHeader from "~/components/AppHeader.vue";
import BannerHome from "~/components/BannerHome.vue";

export default defineComponent({
  name: "HomePage",
  components: { AppHeader, BannerHome },

  setup() {},
});
</script>

<style lang="scss" scoped></style>
