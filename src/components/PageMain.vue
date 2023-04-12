<script>
import ConsultantsCard from "../components/ConsultantsCard.vue";

export default {
  name: "PageMain",
  components: {
    ConsultantsCard,
  },
  data() {
    return {
      consultants: [
        {
          title: "Statistical consulting",
          icon: "fa-chart-line",
        },
        {
          title: "Digital consulting",
          icon: "fa-bullhorn",
        },
        {
          title: "Banking consulting",
          icon: "fa-piggy-bank",
        },
        {
          title: "Enterprise consulting",
          icon: "fa-bullseye",
        },
      ],
    };
  },
};
</script>

<template>
  <!-- consultants section -->
  <section id="consultants">
    <div class="row justify-content-center">
      <div class="col-8">
        <h5 class="flex-shrink-0">Our consultants con help you</h5>
        <div class="row flex-wrap justify-content-between gy-5">
          <div v-for="(consultant, i) in consultants" :key="i" class="col-5">
            <ConsultantsCard :consultant="consultant" />
          </div>
        </div>
      </div>
    </div>
  </section>

  <div class="blue_area">
    <!-- about us section -->
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

#consultants {
  margin: 5rem 0;
  color: $text_dark_gray;
  position: relative;

  h5 {
    text-transform: uppercase;
    font-weight: 700;
    margin-bottom: 4.5rem;
    font-size: 1.4rem;

    &:after {
      content: "";
      background-color: $bg_darker_green;
      height: 2.5px;
      width: 55%;
      position: absolute;
      right: 0;
      top: 1rem;
    }
  }
}
</style>
