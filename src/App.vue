<template>
  <div class="main-container">
    <div class="bg-white">
      <div><NavbarVue></NavbarVue></div>
    </div>
    <div class="container-main">
      <TheMainVue></TheMainVue>
    </div>
    <div class="bg-black">
      <TheFooterVue></TheFooterVue>
    </div>
  </div>
</template>
<script>
import NavbarVue from "./components/Navbar.vue";
import TheFooterVue from "./components/TheFooter.vue";
import TheMainVue from "./components/TheMain.vue";
export default {
  components: { NavbarVue, TheFooterVue, TheMainVue },
  data() {
    return {};
  },
  methods: {},
};
</script>
<style lang="scss">
@use "../src/styles/variables" as *;
.container-main {
  background-color: $bg-cards;
  .main-container {
    height: 100vh;
  }
}
</style>
