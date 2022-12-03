<template>
  <div class="bg-black text-white py-4">
    <div class="container">
      <h2>--&#62; Content goes here &#60;--</h2>
    </div>
  </div>

  <TheMainBannerVue></TheMainBannerVue>
  <div class="jumbotron">
    <div class="container d-flex justify-content-between">
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
      <div class="a1"><img src="../../public/img/dc-logo-bg.png" alt="" /></div>
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
<style scoped lang="scss">
@use "../../src/styles/variables" as *;
img {
  width: 550px;
}
.a1 {
  position: relative;
  bottom: 70px;
}
.jumbotron {
  max-height: 45vh;
  overflow: hidden;
  color: $link-text;
  background-image: url(../../public/img/footer-bg.jpg);
  background-size: cover;
  background-repeat: no-repeat;
}

.bold-text {
  padding: 1rem 0;
  font-weight: bold;
  font-size: 1.5rem;
  color: $link-text;
  a {
    text-decoration: none;
    color: $link-text;
  }
}

.small-text {
  font-size: 0.7rem;
}
.small-text {
  a {
    text-decoration: none;
    color: lightgray;
  }
}
</style>
