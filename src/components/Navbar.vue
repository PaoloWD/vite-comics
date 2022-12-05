<template>
  <div class="container">
    <div class="d-flex justify-content-around align-items-center py-3">
      <nav>
        <img src="../../public/img/favicon.ico" alt="" />
      </nav>
      <div class="d-flex justify-content-between">
        <div v-for="item in link">
          <div class="navbar navbar-expand-lg">
            <div class="container-fluid">
              <button
                class="navbar-toggler"
                type="button"
                data-bs-toggle="collapse"
                aria-expanded="false"
                aria-label="Toggle navigation"
              >
                <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarNavDarkDropdown">
                <ul class="navbar-nav">
                  <li class="nav-item dropdown">
                    <a
                      class="nav-link dropdown-toggle"
                      href="#"
                      role="button"
                      data-bs-toggle="dropdown"
                      aria-expanded="false"
                    >
                      {{ item }}
                    </a>
                    <ul class="dropdown-menu">
                      <li><a class="dropdown-item px-3" href="#">Action</a></li>
                      <li>
                        <a class="dropdown-item px-3" href="#"
                          >Another action</a
                        >
                      </li>
                      <li>
                        <a class="dropdown-item px-3" href="#"
                          >Something else here</a
                        >
                      </li>
                    </ul>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { items } from "../composables/linkNav";
export default {
  data() {
    return {
      link: items,
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
.dropdown-toggle::after {
  display: none;
}
a {
  font-size: 0.7rem;
  padding: 1rem 0;
  text-decoration: none;
  border-radius: 0;
  border-bottom: 5px solid white;

  &:hover {
    border-bottom: 5px solid blue;
  }
}
</style>
