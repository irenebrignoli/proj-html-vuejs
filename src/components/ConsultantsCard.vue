<script>
export default {
  name: "ConsultantCard",
  props: {
    consultant: Object,
  },
};
</script>

<template>
  <div class="d-flex gap-5">
    <div class="ms_icon flex-shrink-0">
      <i :class="`fa-solid ${consultant.icon}`"></i>
    </div>
    <div>
      <h6 class="main_title mb-3">{{ consultant.title }}</h6>
      <p class="text_section">
        When, while lovely valley teems with vapour around meand eridian sun
        strikes the upper impenetrable foliage of my trees, and but a
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.ms_icon {
  width: 3rem;
  height: 3rem;
  border-radius: 50%;
  background-color: $bg_lighter_red;
  text-align: center;

  i {
    color: $text-white;
    line-height: 3rem;
    font-size: 1.5rem;
  }
}

.main_title {
  font-size: 1.1rem;
}
</style>
