<template>
  <div class="container">
    <div><NavbarVue></NavbarVue></div>
  </div>
</template>
<script>
import NavbarVue from "./components/Navbar.vue";
import TheFooterVue from "./components/TheFooter.vue";
import TheMainVue from "./components/TheMainBanner.vue";
export default {
  components: { NavbarVue, TheFooterVue, TheMainVue },
  data() {
    return {};
  },
  methods: {},
};
</script>
<style></style>
