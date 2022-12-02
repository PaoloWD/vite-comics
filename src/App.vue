<template>
  <div class="bg-white">
    <div><NavbarVue></NavbarVue></div>
  </div>
  <TheMainVue></TheMainVue>
  <div class="bg-black">
    <TheFooterVue></TheFooterVue>
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
<style></style>
