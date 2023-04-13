<script>
export default {
  name: "CtaRed",
};
</script>

<template>
  <div
    class="cta_red d-flex align-items-center justify-content-center text-center"
  >
    <div class="text_box">
      <h3 class="main_title_repeat">Let's talk about work</h3>
      <p class="text_section">
        A wonderful serenity has taken possession Far far<br />
        away, behind the word mountains.
      </p>
      <button class="ms_btn ms_btn_blue">Get started</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/buttons" as *;

.cta_red {
  background-image: url("../../src/assets/images/business-people-working-together-on-project-and-B3MZ4TX.jpg");
  background-size: cover;
  height: 23rem;

  .text_section {
    color: $text_transparent_white;
  }
}
</style>
