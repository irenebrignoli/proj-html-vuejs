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
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.cta_green {
  background-color: $bg_lighter_green;
  height: 16rem;
  width: 90%;

  .text_section {
    width: 20rem;
    margin-left: 10rem;
  }
}
</style>
