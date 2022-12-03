<template>
  <div class="container">
    <div class="d-flex justify-content-around align-items-center py-3">
      <nav>
        <img src="../../public/img/favicon.ico" alt="" />
      </nav>
      <div class="d-flex justify-content-between gap-3">
        <div v-for="item in items">
          <div class="dropdown">
            <button
              class="btn dropdown-toggle"
              type="button"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              {{ item }}
            </button>
            <ul class="dropdown-menu">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </div>
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
  methods: {
    OnclickDrop() {},
  },
};
</script>
<style scoped lang="scss">
@use "../../src/styles/variables" as *;
img {
  width: 40px;
}
button {
  font-size: 0.7rem;
  padding: 1rem 0;
  text-decoration: none;
  border-radius: 0;

  &:hover {
    border-bottom: 5px solid blue;
  }
}
</style>
