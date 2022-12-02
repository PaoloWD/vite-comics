<template>
  <div class="container">
    <div class="d-flex justify-content-around align-items-center pt-3">
      <nav>
        <img src="../../public/img/favicon.ico" alt="" />
      </nav>
      <div class="d-flex justify-content-between gap-3">
        <div v-for="item in items">
          <a href="">{{ item }}</a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        "CHARACTERS",
        "COMICS",
        "MOVIES",
        "TV",
        "GAMES",
        "COLLECTIBLES",
        "VIDEOS",
        "FANS",
        "NEWS",
        "SHOP",
      ],
    };
  },
  methods: {},
};
</script>
<style scoped>
img {
  width: 40px;
}
a {
  font-size: 0.7rem;
  text-decoration: none;
}
</style>
