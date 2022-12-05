<template>
  <div class="container text-white py-4">
    <div class="d-flex justify-content-between align-items-center">
      <button class="btn btn-footer text-white">SING-UP NOW!</button>
      <div class="d-flex gap-3 align-items-center">
        <div class="text-primary">FOLLOW US</div>

        <div class="d-flex" v-for="link in iconsList">
          <div><img :src="link.link" alt="" /></div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { iconsList } from "../composables/footerIcons";
export default {
  data() {
    return {
      iconsList: iconsList,
    };
  },
  methods: {},
};
</script>
<style scoped lang="scss">
@use "../../src/styles/variables" as *;
img {
  width: 30px;
}
a {
  text-decoration: none;
  font-weight: bold;
}
.btn-footer {
  border: 1px solid blue;
  border-radius: 0;
  &:hover {
    border: 1px solid blue;
    transform: scale(1.1);
  }
}
</style>
