<template>
  <div class="bg-black text-white">
    <div class="img-container"></div>
  </div>
  <div class="container">
    <div class="current-series text-center bg-primary">CURRENT SERIES</div>
    <div class="row flex-wrap justify-content-center g-5 pt-5">
      <div
        v-for="(card, i) in myCards"
        :key="i"
        class="card col-lg-2 col-md-3 col-sm-4 col-xs-6 text-white"
      >
        <div class="hidden-img-card">
          <img :src="card.thumb" class="card-img-top" alt="..." />
        </div>
        <div class="card-body">
          <h5 class="card-title">{{ card.series }}</h5>
        </div>
      </div>
    </div>
    <div class="text-center p-5">
      <button class="btn btn-primary">LOAD MORE</button>
    </div>
  </div>

  <TheMainBannerVue></TheMainBannerVue>
  <div class="jumbotron">
    <div class="container d-flex justify-content-between">
      <div class="d-flex links-container gap-5 py-4 background-jumpotron">
        <div>
          <div v-for="(link, i) in el1">
            <div :class="i === 0 ? 'bold-text' : 'small-text'">
              <a href="">{{ link }}</a>
            </div>
          </div>
          <div v-for="(link2, i) in el2">
            <div :class="i === 0 ? 'bold-text' : 'small-text'">
              <a href="">{{ link2 }}</a>
            </div>
          </div>
        </div>
        <div>
          <div v-for="(link3, i) in el3">
            <div :class="i === 0 ? 'bold-text' : 'small-text'">
              <a href="">{{ link3 }}</a>
            </div>
          </div>
        </div>
        <div>
          <div v-for="(link4, i) in el4">
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
import { listCards } from "../composables/myCards";
import { elementList1 } from "../composables/linkMain";
import { elementList2 } from "../composables/linkMain";
import { elementList3 } from "../composables/linkMain";
import { elementList4 } from "../composables/linkMain";
import TheMainBannerVue from "./TheMainBanner.vue";
export default {
  components: { TheMainBannerVue },
  data() {
    return {
      el1: elementList1,
      el2: elementList2,
      el3: elementList3,
      el4: elementList4,
      myCards: listCards,
    };
  },
  methods: {},
};
</script>
<style scoped lang="scss">
@use "../../src/styles/variables" as *;

.current-series {
  position: relative;
  bottom: 20px;
  width: 150px;
  color: white;
  padding: 0.5rem 0.5rem;
  font-weight: 450;
}

.hidden-img-card {
  height: 175px;
  overflow: hidden;

  img {
    &:hover {
      cursor: pointer;
      transition: 1s;
      transform: translateY(-5px);
    }
    position: relative;
  }
}
.card {
  border: none;
  background-color: $bg-cards;
}

.btn {
  padding: 0.5rem 4rem;
  border-radius: 0;
  font-size: 0.7rem;
}
.card-title {
  font-size: 0.7rem;
}
.img-container {
  height: 500px;
  overflow: hidden;
  background-image: url(../../public/img/jumbotron.jpg);
  background-size: cover;
}

.a1 {
  width: 100%;
  position: relative;
  bottom: 70px;
  flex-basis: content;
}
.jumbotron {
  max-height: 350px;
  overflow: hidden;
  color: $link-text;
  background-image: url(../../public/img/footer-bg.jpg);
  background-size: cover;
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
