<script>
export default {
  name: "Subheading",
  props: {
    subtitle: String,
  },
};
</script>

<template>
  <div class="d-flex gap-3 align-items-end">
    <div class="line_azur"></div>
    <div class="subheading">{{ subtitle }}</div>
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
