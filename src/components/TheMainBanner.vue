<template>
  <div class="d-flex justify-content-center bg-primary gap-4">
    <div
      class="d-flex align-items-center gap-3 py-4"
      v-for="itemMain in itemsBannerMain"
    >
      <div class="icon"><img :src="itemMain.icon" alt="" /></div>
      <div class="text-white">
        <a href="">{{ itemMain.name }}</a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      itemsBannerMain: [
        {
          icon: "../../public/img/buy-comics-digital-comics.png",
          name: "DIGITAL COMICS",
        },
        {
          icon: "../../public/img/buy-comics-merchandise.png",
          name: "DC MERCHANDISE",
        },
        {
          icon: "../../public/img/buy-comics-subscriptions.png",
          name: "SUBSCRIPTION",
        },
        {
          icon: "../../public/img/buy-comics-shop-locator.png",
          name: "COMIC SHOP LOCATOR",
        },
        {
          icon: "../../public/img/buy-dc-power-visa.svg",
          name: "DC POWER VISA",
        },
      ],
    };
  },
  methods: {},
};
</script>
<style scoped>
a {
  color: white;
  text-decoration: none;
}
img {
  width: 50px;
}
</style>
