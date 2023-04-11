<script>
import TheJumbotron from "../components/TheJumbotron.vue";

export default {
  name: "PageHeader",
  components: {
    TheJumbotron,
  },
};
</script>

<template>
  <header>
    <div class="header_top">
      <div class="container h-100">
        <div class="h-100 d-flex justify-content-between align-items-center">
          <div class="header_logo">
            <img
              class="img-fluid"
              src="../assets/images/logotype.png"
              alt="logo Phlox"
            />
          </div>
          <nav class="main_nav">
            <ul class="d-flex gap-2 mb-0">
              <li>link</li>
              <li>link</li>
              <li>link</li>
            </ul>
          </nav>
        </div>
      </div>
    </div>

    <div class="header_bottom">
      <TheJumbotron />
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../../src/styles/partials/variables" as *;

header {
  position: relative;
  .header_top {
    height: 4.5rem;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;

    .header_logo {
      img {
        height: 1rem;
      }
    }

    .main_nav {
      font-size: 0.75rem;

      li {
        color: $text_dirty_white;
      }
    }
  }

  .header_bottom {
    height: 50rem;
    background-color: red;
  }
}
</style>
