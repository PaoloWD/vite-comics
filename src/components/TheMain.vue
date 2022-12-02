<template>
  <div class="bg-black text-white py-4"><h2>--> Content goes here</h2></div>
  <TheMainBannerVue></TheMainBannerVue>
  <div class="jumbotron">
    <div class="d-flex links-container gap-5 py-4 background-jumpotron">
      <div>
        <div v-for="(link, i) in elementList1">
          <div v-if="link[i] === 0" class="text-danger">{{ link }}</div>
          <div v-else>{{ link }}</div>
        </div>
        <div v-for="(link2, i) in elementList2">
          <div v-if="link2[i] === 0" class="text-danger">{{ link2 }}</div>
          <div v-else>{{ link2 }}</div>
        </div>
      </div>
      <div>
        <div v-for="(link3, i) in elementList3">
          <div v-if="link3[i] === 0" class="text-danger">{{ link3 }}</div>
          <div v-else>{{ link3 }}</div>
        </div>
      </div>
      <div>
        <div v-for="(link4, i) in elementList4">
          <div v-if="link4[i] === 0" class="text-danger">{{ link4 }}</div>
          <div v-else>{{ link4 }}</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import TheMainBannerVue from "./TheMainBanner.vue";
export default {
  components: { TheMainBannerVue },
  data() {
    return {
      elementList1: [
        "DC COMICS",
        "Characters",
        "Comics",
        "Movies",
        "TV",
        "Games",
        "Videos",
        "News",
      ],
      elementList2: ["SHOP", "Shop Dc", "Shop Dc Collectibles"],
      elementList3: [
        "DC",
        "Term Of Use",
        "Privacy policy (new)",
        "Ad choise",
        "Adversting",
        "Jobs",
        "Subscriptions",
        "Talent Workshops",
        "CPSC Certificateds",
        "Rating",
        "Shop Help",
        "Contact Us",
      ],
      elementList4: [
        "SITES",
        "DC",
        "MAD Magazine",
        "DC Kids",
        "DC Universe",
        "DC Power Visa",
      ],
    };
  },
  methods: {},
};
</script>
<style scoped>
a1 {
  font-size: 0.5rem;
}
.background-jumpotron {
  color: white;
  background-image: url(../../public/img/footer-bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
