<script>
import ConsultantsCard from "../components/ConsultantsCard.vue";

export default {
  name: "PageMain",
  components: {
    ConsultantsCard,
  },
  consultantsIcons: [
    "fa-chart-line",
    "fa-bullhorn",
    "fa-piggy-bank",
    "fa-bullseye",
  ],
};
</script>

<template>
  <!-- consultants section -->
  <section id="consultants">
    <div class="row justify-content-center">
      <div class="col-8">
        <h5>Our consultants con help you</h5>
        <div class="row justify-content-between">
          <div class="col-5">
            <ConsultantsCard />
          </div>
          <div class="col-5"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

#consultants {
  height: 50rem;
  margin-top: 5rem;
  color: $text_dark_gray;

  h5 {
    text-transform: uppercase;
    font-weight: 700;
    margin-bottom: 4.5rem;
    font-size: 1.4rem;
  }
}
</style>
