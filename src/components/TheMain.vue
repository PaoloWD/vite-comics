<template>
  <div class="bg-black text-white py-4"><h2>--> Content goes here</h2></div>

  <TheMainBannerVue></TheMainBannerVue>
  <div class="jumbotron">
    <div class="d-flex links-container gap-5 py-4 background-jumpotron">
      <div>
        <div v-for="(link, i) in elementList1">
          <div :class="i === 0 ? 'bold-text' : 'small-text'">
            <a href="">{{ link }}</a>
          </div>
        </div>
        <div v-for="(link2, i) in elementList2">
          <div :class="i === 0 ? 'bold-text' : 'small-text'">
            <a href="">{{ link2 }}</a>
          </div>
        </div>
      </div>
      <div>
        <div v-for="(link3, i) in elementList3">
          <div :class="i === 0 ? 'bold-text' : 'small-text'">
            <a href="">{{ link3 }}</a>
          </div>
        </div>
      </div>
      <div>
        <div v-for="(link4, i) in elementList4">
          <div :class="i === 0 ? 'bold-text' : 'small-text'">
            <a href="">{{ link4 }}</a>
          </div>
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
.background-jumpotron {
  color: white;
  background-image: url(../../public/img/footer-bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
}

.bold-text {
  padding: 1rem 0;
  font-weight: bold;
  font-size: 1.5rem;
}

.small-text {
  font-size: 0.7rem;
}
a {
  text-decoration: none;
  color: lightgray;
}
</style>
