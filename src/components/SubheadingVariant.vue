<script>
export default {
  name: "SubheadingVariant",
  props: {
    subtitle: String,
  },
};
</script>

<template>
  <div class="row gap-3 justify-content-end">
    <div class="col-7 d-flex align-items-end justify-content-between">
      <div class="subheading">{{ subtitle }}</div>
      <div class="line_azur"></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../../src/styles/partials/variables" as *;

.line_azur {
  width: 40px;
}
.subheading {
  color: $text_dirty_white;
  line-height: 0.6;
  font-size: 0.9rem;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}
</style>
