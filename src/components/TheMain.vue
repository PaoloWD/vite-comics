<template>
  <div class="bg-black text-white py-4"><h2>--> Content goes here</h2></div>
  <TheMainBannerVue></TheMainBannerVue>
</template>
<script>
import TheMainBannerVue from "./TheMainBanner.vue";
export default {
  components: { TheMainBannerVue },
  data() {
    return {
      elementList1: [{}],
      elementList2: [{}],
      elementList3: [{}],
      elementList4: [{}],
    };
  },
  methods: {},
};
</script>
<style scoped></style>
