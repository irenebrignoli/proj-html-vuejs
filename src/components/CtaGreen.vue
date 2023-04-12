<script>
export default {
  name: "CtaGreen",
};
</script>

<template>
  <div class="cta_green">
    <div class="d-flex justify-content-center align-items-center h-100">
      <h5 class="main_title fs-4 text-center">
        We help to deliver<br />the business case
      </h5>
      <p class="text_section">
        When, while lovely valley teems with vapour around meand meridian sun
        strikes the upper impenetrable foliage of my trees, and but a thousand
        unknown
      </p>
    </div>
    <button class="ms_btn ms_btn_red">Get started</button>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/buttons" as *;

.cta_green {
  background-color: $bg_lighter_green;
  height: 16rem;
  width: 90%;
  color: $text_dark_violet;
  position: relative;

  .text_section {
    width: 22rem;
    margin-left: 10rem;
  }

  .ms_btn {
    bottom: 0;
    right: 0;
    position: absolute;
  }
}
</style>
