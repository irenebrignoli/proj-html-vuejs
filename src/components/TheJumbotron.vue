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
      <div class="blue_col col-4 h-100">
        <div class="text_box">
          <Subheading subtitle="Always the best way you need it" />
        </div>
      </div>
      <div class="red_img_col col-8"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.jumbotron {
  .blue_col {
    position: relative;

    .text_box {
      position: absolute;
      right: 0;
      top: 12rem;
    }
  }
  .red_img_col {
    background-image: url("../assets/images/portrait-of-young-architect-woman-on-meeting-KFZCE3A.jpg");
  }
}
</style>
