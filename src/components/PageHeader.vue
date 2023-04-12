<script>
import TheJumbotron from "../components/TheJumbotron.vue";

export default {
  name: "PageHeader",
  components: {
    TheJumbotron,
  },
  props: {
    links: Array,
  },
};
</script>

<template>
  <header>
    <!-- hedaer top -->
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
          <nav class="main_nav h-100">
            <ul class="d-flex gap-4 mb-0 h-100">
              <li v-for="link in links" class="h-100">
                <a href="#">{{ link }}</a>
              </li>
            </ul>
          </nav>
        </div>
      </div>
    </div>

    <!-- hedaer bottom-->
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
    z-index: 99;

    .header_logo {
      img {
        height: 1rem;
      }
    }

    .main_nav {
      font-size: 0.75rem;

      li {
        position: relative;
        line-height: 4.5rem;

        a {
          color: $text_transparent_white;

          &:hover {
            color: $text_white;
            font-weight: 600;
          }
        }

        &:first-child {
          a {
            color: $text_white;
            font-weight: 600;
          }

          a:before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background-color: $bg_white;
          }
        }
      }
    }
  }

  .header_bottom {
    height: 48rem;
    background-color: red;
  }
}
</style>
