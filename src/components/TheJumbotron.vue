<script>
import Subheading from "./Subheading.vue";
export default {
  name: "TheJumbotron",
  components: {
    Subheading,
  },
};
</script>

<template>
  <div class="jumbotron h-100">
    <div class="row h-100">
      <!-- blue col -->
      <div class="blue_col col-4 h-100"></div>

      <!-- red col -->
      <div class="red_img_col col-8"></div>

      <!-- text-jumbotron -->
      <div class="text_jumbotron">
        <div class="container">
          <div class="text_box">
            <Subheading subtitle="Always the best way you need it" />
            <h1 class="main_title display-2 mt-4">
              The best<br />business<br />consulting
            </h1>
            <div class="d-flex gap-4 align-items-center mt-4">
              <button class="ms_btn ms_btn_green">Read More</button>
              <div class="play">
                <i class="fa-solid fa-play"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../src/styles/partials/variables" as *;
@use "../styles/partials/buttons";

.jumbotron {
  .text_jumbotron {
    position: absolute;
    top: 16rem;
    .main_title {
      color: $text_white;
      line-height: 1;
    }

    .play {
      text-align: center;
      width: 2.7rem;
      height: 2.7rem;
      border-radius: 50%;
      border: 2px solid $border_white;

      i {
        color: $bg_darker_green;
        font-size: 0.8rem;
        line-height: 2.4rem;
      }
    }
  }
  .red_img_col {
    background-image: url("../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg");
  }
}
</style>
