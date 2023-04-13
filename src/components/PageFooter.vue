<script>
export default {
  name: "PageFooter",
  props: {
    links: Array,
  },
};
</script>

<template>
  <footer class="pt-4">
    <div class="container">
      <!-- footer top -->
      <div class="footer_top py-5 d-flex justify-content-between">
        <img
          class="footer_logo"
          src="../../src/assets/images/logotype-2-300x50.png"
          alt="logo Phlox"
        />
        <nav class="main_nav">
          <ul class="d-flex gap-4 mb-0">
            <li v-for="link in links" class="h-100">
              <a href="#">{{ link }}</a>
            </li>
          </ul>
        </nav>
        <div class="footer_icons d-flex gap-3">
          <i class="fa-brands fa-instagram"></i>
          <i class="fa-brands fa-linkedin-in"></i>
          <i class="fa-brands fa-facebook-f"></i>
          <i class="fa-brands fa-twitter"></i>
        </div>
      </div>

      <!-- footer bottom-->
      <div
        class="footer_bottom py-4 d-flex justify-content-between align-items-end"
      >
        <div class="text_box">
          <div>Terms of use</div>
          <div>Privacy Environmental Policy</div>
        </div>
        <div class="text_box">
          Copyright 0 2020 Phlox Consulting. All Rights Reserved.
        </div>
      </div>
    </div>
    <div class="arrow_up">
      <a href="#"><i class="fa-solid fa-arrow-up"></i></a>
    </div>
    <div class="chat"><i class="fa-regular fa-comment"></i></div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

footer {
  background-color: $bg_darkblue;
  position: relative;

  .arrow_up {
    background-color: $bg_white;
    width: 2rem;
    height: 2rem;
    right: 4.5rem;
    bottom: 1.5rem;

    i {
      line-height: 2rem;
      font-size: 0.8rem;
    }
  }

  .footer_top {
    border-bottom: 1px solid $text_transparent_white;

    .footer_logo {
      height: 1rem;
    }

    .main_nav {
      font-size: 0.8rem;
      a {
        color: $text_gray;

        &:hover {
          color: $text_white;
          font-weight: 700;
        }
      }
    }

    .footer_icons {
      color: $text_white;

      i {
        font-size: 0.8rem;
      }
    }
  }

  .footer_bottom {
    .text_box {
      color: $text_gray;
      font-size: 0.8rem;
    }
  }
}
</style>
