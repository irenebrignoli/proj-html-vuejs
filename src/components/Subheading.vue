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
  background-color: $bg_darker_green;
  height: 2.5px;
  width: 40px;
  margin-bottom: 5px;
}
.subheading {
  color: $text_dirty_white;
  font-size: 0.8rem;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}
</style>
