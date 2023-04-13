<script>
export default {
  name: "TestimonialCard",
  props: {
    testimonial: Object,
  },
  methods: {
    getImageUrl(name) {
      return new URL(
        `../assets/images/testimonial-section/${name}.jpg`,
        import.meta.url
      ).href;
    },
  },
};
</script>

<template>
  <div
    class="testimonial_card"
    @mouseover="testimonial.hover = true"
    @mouseleave="testimonial.hover = false"
  >
    <div class="text_box p-5">
      <p class="text_section">
        When, while lovely valley teems with vapour around meand eridian sun
        strikes the upper impenetrable foliage of my trees, and but a thousand
        unknown plants are noticed by when I hear the buzz of the little .
      </p>
      <h6>{{ testimonial.name }}</h6>
      <small>Amazon Inc.</small>
    </div>

    <!-- on hover -->
    <div v-if="testimonial.hover == true" class="hover">
      <img :src="getImageUrl(testimonial.image)" alt="testimonial.name" />
      <div class="text_box p-5">
        <p class="text_section">
          When, while lovely valley teems with vapour around meand eridian sun
          strikes the upper impenetrable foliage of my trees, and but a thousand
          unknown plants are noticed by when I hear the buzz of the little .
        </p>
        <h6>{{ testimonial.name }}</h6>
        <small>Amazon Inc.</small>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.testimonial_card {
  position: relative;
  height: 100%;

  .text_box {
    height: 100%;
    .text_section,
    small {
      color: $text_gray;
    }

    h6 {
      font-weight: 700;
      font-size: 1.2rem;
      color: $text_dark_violet;
    }
  }

  .hover {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;

    img {
      object-fit: cover;
      height: 100%;
      width: 100%;
    }

    .text_box {
      height: 100%;
      position: absolute;
      top: 0;
      left: 0;

      .text_section,
      small {
        color: $text_transparent_white;
      }

      h6 {
        color: $text-white;
      }
    }
  }
}
</style>
