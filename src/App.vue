<template>
  <div class="bg-white">
    <div><NavbarVue></NavbarVue></div>
  </div>

  <div><TheMainVue></TheMainVue></div>
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
