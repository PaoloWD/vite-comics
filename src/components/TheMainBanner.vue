<template>
  <div class="d-flex justify-content-center bg-primary gap-4">
    <div
      class="d-flex align-items-center gap-3 py-4"
      v-for="itemMain in linkBanner"
    >
      <div class="icon"><img :src="itemMain.icon" alt="" /></div>
      <div class="text-white">
        <a href="">{{ itemMain.name }}</a>
      </div>
    </div>
  </div>
</template>
<script>
import { itemsBannerMain } from "../composables/linkMainBanner";

export default {
  data() {
    return {
      linkBanner: itemsBannerMain,
    };
  },
  methods: {},
};
</script>
<style scoped lang="scss">
@use "../../src/styles/variables" as *;
a {
  color: $link-text;
  text-decoration: none;
  &:hover {
    color: $link-text;
  }
}
img {
  width: 50px;
}
</style>
