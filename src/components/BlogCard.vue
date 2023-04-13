<script>
export default {
  name: "BlogCard",
  props: {
    blog: Object,
  },
  methods: {
    getImageUrl(name) {
      return new URL(
        `../assets/images/blog-section/${name}.jpg`,
        import.meta.url
      ).href;
    },
  },
};
</script>

<template>
  <div class="blog_card">
    <img :src="getImageUrl(blog.image)" alt="blog.title" />
    <div class="box_white py-4 px-5">
      <span class="me-4">{{ blog.date }}</span
      ><span>by {{ blog.writer }}</span>
      <h4 class="my-3">{{ blog.title }}</h4>
      <p class="text_section">{{ blog.text }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.blog_card {
  height: 28rem;
  position: relative;
  img {
    object-fit: cover;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }

  .box_white {
    background-color: $bg_white;
    position: absolute;
    right: 0;
    bottom: -5rem;
    width: 80%;
    height: 15rem;

    span {
      color: $text_red;
      font-size: 0.9rem;
      font-weight: 500;
    }

    h4 {
      font-weight: 700;
      color: $text_dark_violet;
    }

    p {
      color: $text_gray;
    }
  }
}
</style>
