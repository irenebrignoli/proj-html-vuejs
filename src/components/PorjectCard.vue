<script>
export default {
  name: "ProjectCard",
  props: {
    project: Object,
  },
  methods: {
    getImageUrl(name) {
      return new URL(
        `../assets/images/project-section/${name}.jpg`,
        import.meta.url
      ).href;
    },
  },
};
</script>

<template>
  <div
    class="project_card"
    @mouseover="project.hover = true"
    @mouseleave="project.hover = false"
  >
    <img :src="getImageUrl(project.image)" alt="" class="img-fluid" />
    <div
      v-if="project.hover == true"
      class="hover d-flex p-3 align-items-end justify-content-between"
    >
      <div class="text_box">
        <div class="project_title">{{ project.title }}</div>
        <div class="project-subtitle">uncategorized</div>
      </div>
      <div class="add"><i class="fa-solid fa-plus"></i></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;
@use "../styles/partials/buttons" as *;

.project_card {
  position: relative;

  .hover {
    position: absolute;
    background-color: $bg_transparent_red;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;

    .project_title {
      color: $text-white;
      font-weight: 700;
      letter-spacing: 0.1rem;
    }

    .project-subtitle {
      color: $text_transparent_white;
    }

    .add {
      background-color: $bg_darkblue;
      width: 3rem;
      height: 3rem;
      text-align: center;
      cursor: pointer;

      i {
        color: $text-white;
        line-height: 3rem;
      }
    }
  }
}
</style>
